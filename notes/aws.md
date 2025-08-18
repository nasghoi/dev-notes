
# Deploying Laravel on AWS

## 1. Set up an EC2 instance

1. Log in to your AWS Management Console.
2. Navigate to the EC2 Dashboard.
3. Click on "Launch Instance."
4. Choose an Amazon Machine Image (AMI) - select an Ubuntu Server 22.04 LTS (HVM), SSD Volume Type.
5. Choose an Instance Type - select t3.small.
6. Key pair (Login) - select an existing key pair or create a new one.
7. Network settings - tick all boxes.
8. Configure storage - leave defaults.
9. Launch instance.

## 2. Connect to EC2 instance

### Open your terminal.

### Connect to your instance using SSH:

   ```bash
   ssh -i /path/to/your-key.pem ubuntu@your-ec2-public-dns
   ```
> Replace `/path/to/your-key.pem` with the path to your key pair file and `your-ec2-public-dns` with the public DNS of your EC2 instance

### Update your package manager:
   
   ```bash
   sudo apt update
   ```

## 3. Adds PHP repository

- adds a new software source (repository) to Ubuntu
- `ppa:ondrej/php` is a Personal Package Archive (PPA) that provides newer PHP versions than the default Ubuntu repositories

```bash
sudo add-apt-repository ppa:ondrej/php
```

## 4. Install PHP and required extensions

### Install PHP 8.3 and commonly used extensions
    
```bash
sudo apt install php8.3 php8.3-cli php8.3-{bz2,curl,mbstring,intl,xml,zip} unzip
```

### Install PHP 8.3 FPM (FastCGI Process Manager)
- more efficient, and scalable because it runs PHP as *separate worker processes* instead of inside Apache
- a service that lets your web server (Apache/Nginx) *run PHP apps more efficiently*
    
```bash
sudo apt install php8.3-fpm
```

### Enable PHP 8.3 FPM configuration
- enables the PHP 8.3 FPM configuration for Apache

```bash
sudo a2enconf php8.3-fpm
```

### Reload/Restart Apache to apply changes
- reloads Apache configuration files *without fully stopping the server*

```bash
sudo systemctl reload apache2
```

- stops and starts Apache completely
```bash
sudo systemctl restart apache2
```

### Install additional PHP extensions
- installs a bunch of core PHP extensions that *are not always bundled by default*

```bash
sudo apt install php8.3-{calendar,ctype,exif,ffi,fileinfo,ftp,gettext,iconv,pdo,phar,posix,shmop,sockets,sysvmsg,sysvsem,sysvshm,tokenizer}
```

### List installed PHP packages
- lists all installed PHP packages and *saves the output* to a file named `packages.txt`

```bash
dpkg -l | grep php | tee packages.txt
```

### Check PHP version
- verifies the installed PHP version

```bash
php -v
```

### Check Apache version
- verifies the installed Apache version

```bash
apache2 -v
```

## 5. Install Composer

### Download and install Composer
- installs Composer, a dependency manager for PHP

```bash
curl -sS https://getcomposer.org/installer | php
```

### Move Composer to a global location
- moves the Composer binary to `/usr/local/bin` so you can run it from anywhere

```bash
sudo mv composer.phar /usr/local/bin/composer
```

### Set permissions for Composer
- sets the appropriate permissions for the Composer binary

```bash
sudo chmod +x /usr/local/bin/composer
```

### Check Composer version
- verifies the installed Composer version

```bash
composer -v
```

## 6. Install Git

### Check Git version
- verifies the installed Git version

```bash
git --version
```

### Install Git (if not installed)
- installs Git, a version control system

```bash
sudo apt install git -y
```

## 7. Install MySQL

### Install MySQL Server
- installs the MySQL server package

```bash
sudo apt install mysql-server -y
```

### Check MySQL version
- verifies the installed MySQL version

```bash
mysql -V
```

### Start MySQL
- starts the MySQL service

```bash
sudo systemctl start mysql
```

### Enable MySQL autostart
- enables MySQL to *start on boot*

```bash
sudo systemctl enable mysql
```

### Check MySQL status
- checks if MySQL is running

```bash
sudo systemctl status mysql
```

## 8. Configure MySQL

### Allowing remote connections
- disables the bind-address setting to allow remote connections

```bash
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```
> Change bind-address to 0.0.0.0

- restarts MySQL to apply changes
```bash
sudo systemctl restart mysql
```

### Log into MySQL
- log into the MySQL server as the root user *to manage databases and users*

```bash
sudo mysql -u root -p
```

### Create a new MySQL user
- creates a new user with privileges
```bash
CREATE USER '<your_name>'@'%' IDENTIFIED BY '<your_password>';
```
> Replace `<your_name>` and `<your_password>` with your desired username and password

### Grant privileges to the new user
- grants the new user permissions to create, alter, drop, insert, update, delete, select, and reference databases and tables

```bash
GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on *.* TO '<your_name>'@'%' WITH GRANT OPTION;
```
> Replace `<your_name>` with the username you created earlier

### Grant privileges to database
- grants privileges on all databases and tables

```bash
GRANT ALL PRIVILEGES ON *.* TO '<your_name>'@'%';
```
> Replace `<your_name>` with the username you created earlier

### Apply changes
- applies the changes made to user privileges

```bash
FLUSH PRIVILEGES;
```

### Exit MySQL bash

```bash
exit
```

## 9. Firewall configuration

### Check UFW status
- verifies if UFW (Uncomplicated Firewall) is active

```bash
sudo ufw status
```

### Enable UFW
- enables UFW to *start on boot*

```bash
sudo ufw enable
```

### Allow port 22 / 80 / 3306
- allows incoming traffic on ports 22 (SSH), 80 (HTTP), and 3306 (MySQL)
- Do NOT open `port 3306` unless you really *need remote DB access*
- allow `port 443` if you *need HTTPS access*

```bash
sudo ufw allow 22
```

```bash
sudo ufw allow 80
```

```bash

sudo ufw allow 3306
```

## 10. Check connection to database

### Add inbound rules in your instance
1. Open instance
2. Click security -> security groups
3. Click Edit inbound rule
4. Add rule -> select Type: MySQL/Aurora and CIDR Blocks: 0.0.0.0/0
5. Click on save rules

### Add database in DBeaver
1. Open DBeaver
2. Create new connection
3. Select MySQL
4. Enter Server Host: your-ec2-public-dns
5. Enter Username and Password based on MySQL Details you created before
6. Click Finish 

## 11. Laravel Setup

### Access the default document root
- navigates to the default document root for Apache

```bash
cd /var/www/html
```

### Set web server ownership
- Gives Apache (`www-data`) full access to the project folder

```bash
sudo chown -R www-data:www-data .
```

### Clone your Laravel project
- clones your Laravel project from a Git repository

```bash
sudo git clone <your-repo-url>
```
> Replace `<your-repo-url>` with the URL of your Git repository

### Access your project directory
- navigates into the project directory

```bash
cd <your-repo-name>
```
> Replace `<your-repo-name>` with the name of your cloned repository

- Change the owner of your Laravel project folder (root->user)

```bash
sudo chown -R $(whoami) /var/www/html/<your-repo-name>
```
> Replace `<your-repo-name>` with the name of your cloned repository

### Add Git repository to safe directory
- allows Git to operate on the repository without permission issues

```bash
git config --global --add safe.directory /var/www/html/<your-repo-name>
```

### Install PHP dependencies
- installs the PHP dependencies defined in the `composer.json` file

```bash
composer install
```

### Copy `.env.example` to `.env`
- creates a *copy* of the example environment file

```bash
sudo cp .env.example .env
```

### Generate application key
- generates a new application key for your Laravel project

```bash
php artisan key:generate
```

### Edit `.env`
- configures the environment variables for your Laravel project

```bash
nano .env
```

```dotenv
DB_CONNECTION=mysql
DB_HOST=your_database_host
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```
> Replace `your_database_host`, `your_database`, `your_username`, and `your_password` with your MySQL details

### Migrate the database
- runs the database migrations

```bash
php artisan migrate
```

## 11. Configure Apache for Laravel


### Enable Apache Rewrite Module
- enables the Apache rewrite module, which is required for Laravel's URL routing

```bash
sudo a2enmod rewrite
```

### Set permissions for storage and bootstrap/cache
- gives the web server (Apache) ownership of the storage and bootstrap/cache directories

```bash
sudo chown -R www-data:www-data storage bootstrap/cache
```

```bash
sudo chmod -R 775 storage bootstrap/cache
```

### Access Apache sites-available
- navigates to the Apache sites-available directory

```bash
cd /etc/apache2/sites-available
```

### Create New Configuration File
- creates a new configuration file for your Laravel project

```bash
sudo nano /etc/apache2/sites-available/<your-project>.conf
```
> Replace `<your-project>` with the name of your project

```apache
<VirtualHost *:80>
    ServerName <your-domain.com-or-ip>
    DocumentRoot /var/www/html/<your-repo-name>/public

    <Directory /var/www/html/<your-repo-name>>
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
> Replace `<your-domain.com-or-ip>` with your domain name or public IP address and `<your-repo-name>` with the name of your cloned repository

### Disable the default site configuration
- disables the default Apache site configuration
```bash
sudo a2dissite 000-default.conf
```

### Enable the new site configuration
- enables the new site configuration

```bash
sudo a2ensite <your-project>.conf
```
> Replace `<your-project>` with the name of your conf file that has been created before

```bash
sudo systemctl reload apache2
```

## 12. Access your website
- browse on your web browser

```bash
http://<your-domain.com-or-ip>
```
> Replace `<your-domain.com-or-ip>` with your domain name or public IP address