# Jupyter Notebook
## Shortcuts
- **Run cell**: `Shift + Enter`
- **Insert cell below**: `B`
- **Insert cell above**: `A`
- **Delete cell**: `D, D`
- **Undo cell deletion**: `Z`
- **Move cell up**: `K`
- **Move cell down**: `J`
- **Copy cell**: `C`
- **Paste cell**: `V`
- **Cut cell**: `X`
- **Select cell**: `Shift + Space`
- **Deselect cell**: `Shift + Space`
- **Edit cell**: `Enter`
- **Save notebook**: `Ctrl + S`
- **Stop cell**: `Ctrl + M, I`
- **Restart kernel**: `0, 0`
- **Interrupt kernel**: `I, I`
- **Change to code cell**: `Y`
- **Change to markdown cell**: `M`
- **Change to raw cell**: `R`

# Python
- case sensitive

## Variables
### Definition
```
x = 5
x
```
> 5
```
y = 4
y
```
> 4
```
x,y = (1,2)
x
```
> 1
```
y
```
> 2

### Types of Data
1. Number and Boolean Values
- Integers = Positive or negative whole numbers
- Floats = Decimal numbers
- Booleans = True or False
```
x1 = 5
type(x1)
```
> int
```
float(2)
```
> 2.0
```
int(5.9)
```
> 5
2. Strings
- sequence of characters
```
'Nasrul'
```
> 'Nasrul'
```
"Nasrul"
```
> 'Nasrul'
```
x4 = 'Nasrul'
```
> 'Nasrul'
```
y = 10
print(str(y) + " " + "Ringgit")
```
> 10 Ringgit

- escape character (\) -> backslash
```
'I\'m fine'
```
> "I'm fine"
- double quotes ("")
```
"I'm fine"
```
> 'I'm fine'
```
print(3,5)
```
> 3 5
```
3, 5, 6.9, 'car'
```
> 3 5 6.9 'car'

## Basic Syntax
### Arithmetic Operators
- Addition: `+`
```
1+2
```
> 3
- Subtraction: `-`
```
5-3
```
> 2
- Multiplication: `*`
```
2*3
```
> 6
- Division: `/`
```
6/3
```
> 2.0
```
7/3
```
> 2.3333333333333335
- Modulus: `%`
```
6%3
```
> 0
- Double Exponentiation: `**`
```
5 ** 3
```
> 125

### Double Equality Sign
- `==` means "equals"
```
y == 125
```
> True
```
y == 126
```
> False

### Reassign Values
```
q = 1
q
```
> 1
```
q = 2
q
```
> 2
```
q + 5
```
> 7

### Add Comments
- Comments are sentences NOT executed by the computer
```
# This is a comment
```

### Line continuation
- If a statement is too long, split it into multiple lines using a backslash (`\`)
```
2.0 * 1.5 + \
5
```

### Indexing elements
```
"Bingo!"[0]
```
> 'B'

### Indentation
- indentation is used to define the structure of the code
```
# block code 1
def five(x):
    return x
# block code 2
print(five(7))
```
> 7

## Operators
### Comparison Operators
- Not equal: `!=`
```
10 != 15
```
> True
```
10 != 10
```
> False
- Greater than: `>`
```
100 > 50
```
> True
```
100 > 150
```
> False
- Less than: `<`
```
100 < 50
```
> False
```
100 < 150
```
> True
- Greater than or equal to: `>=`
```
100 >= 50
```
> True
```
100 >= 150
```
> False
- Less than or equal to: `<=`
```
100 <= 50
```
> False
```
100 <= 150
```
> True

### Logical and Identity Operators  
![logical-operator](/images/logical-operator.png)  
- Not: `not`
```
not True
```
> False
```
not False
```
> True
- And: `and`
```
True and False
```
> False
```
True and True
```
> True
```
3 > 5 and 10 <= 20
```
> False
- Or: `or`
```
False or False
```
> False
```
False or True
```
> True
- Identity: `is`
```
x is y
```
> True
```
x is not y
```
> False

## Conditional Statements
### If Statements
```
if 15 / 5 == 3:
    print('iyee')
```
> iyee
### Else Statements
```
if 15 / 5 == 4:
    print('iyee')
else:
    print('tidak')
```
> tidak

### Elif Statements
```
if 15 / 5 == 4:
    print('iyee')
elif 15 / 5 == 3:
    print('tidak')
else:
    print('entah')
```

## Functions
- def is a keyword used to define a function
### Define a Function
```
def simple():
    print("Hi, this is first function")

simple()
```
> Hi, this is first function

### Define a Function with Parameter
```
def greet(name):
    print("Hello, " + name + "!")
greet("Nasrul")
```
> Hello, Nasrul!

### Another way to define a function
```
def plus_ten(a):
    result = a + 10
    print(result)
    return result

plus_ten(2)
```
> 12

### Using Function in Another Function
```
def wage(w_hours):
    return w_hours * 25

def with_bonus(w_hours):
    return wage(w_hours) + 50

wage(8), with_bonus(8)
```
> 200, 250

### Combining Conditional Statements and Functions
```
def add_10(m):
    if m >= 100:
        m = m + 10
        return m
    else:
        return "Save more"

add_10(110)
```
> 120

### Functions Containing a Few Arguments
```
def subtract_bc(a,b,c):
    result = a - b * c
    print('Parameter a: ', a)
    print('Parameter b: ', b)
    print('Parameter c: ', c)
    return result

subtract_bc(10,3,2)
```
> Parameter a:  10  
> Parameter b:  3  
> Parameter c:  2  
> 4
```
# other ways to assign values
subtract_bc(b=3,a=10,c=2)
```
> Parameter a:  10  
> Parameter b:  3  
> Parameter c:  2  
> 4

### Notable Built-In Functions in Python

#### type
- Returns the type of an object
```
type(10)
```
> int

#### int
- Converts a value to an integer
```
int(5.0)
```
> 5

#### float
- Converts a value to a floating-point number
```
float(3)
```
> 3.0

#### str
- Converts a value to a string
```
str(500)
```
> '500'

#### max
- Returns the largest of the input values
```
max(10, 20, 30)
```
> 30

#### min
- Returns the smallest of the input values
```
min(10, 20, 30)
```
> 10

#### abs
- Returns the absolute value of a number
```
z = -20
abs(z)
```
> 20

#### sum
- Returns the sum of all items in an iterable
```
list_1 = [1,2,3,4]
sum(list_1)
```
> 10

#### round
- Rounds a floating-point number to a specified number of decimal places
```
round(3.555,2)
```
> 3.56
```
round(3.2)
```
> 3

#### pow
- Returns the value of a number raised to the power of another number
```
2 ** 10
```
> 1024
```
pow(2,10)
```
> 1024

#### len
- Returns the number of elements in an object
```
len('Mathematics')
```
> 11

## Sequences

### Lists
#### Define lists
```
Participants = ['John', 'Leila', 'Gregory', 'Cate']
print(Participants)
```
> ['John', 'Leila', 'Gregory', 'Cate']
#### Accessing Elements
```
print(Participants[0])
```
> John
#### Accessing Elements with Negative Index
```
Participants[-2]
```
> Gregory
#### Modifying Elements
```
Participants[3] = 'Nasr'
print(Participants)
```
> ['John', 'Leila', 'Gregory', 'Nasr']
#### Deleting Elements
```
del Participants[1]
print(Participants)
```
> ['John', 'Gregory', 'Nasr']

### Using Methods
#### Append  
- tambah data dekat belakang
```
Participants.append('Alice')
print(Participants)
```
> ['John', 'Gregory', 'Nasr', 'Alice']
#### Extends
- tambah data dari list lain
```
Participants.extend(['Bob', 'Charlie'])
print(Participants)
```
> ['John', 'Gregory', 'Nasr', 'Alice', 'Bob', 'Charlie']

### List Slicing
#### Using Colon(`:`)
```
print(Participants[1:4])
```
> ['Gregory', 'Nasr', 'Alice']
```
print(Participants[:4])
```
> ['John', 'Gregory', 'Nasr', 'Alice']
```
print(Participants[2:])
```
> ['Nasr', 'Alice', 'Bob', 'Charlie']

#### Index
```
print(Participants.index('Alice'))
```
> 3
```
NewPart = ['Aman', 'Amin']
BigPart = [Participants, NewPart]
print(BigPart)
```
> [['John', 'Gregory', 'Nasr', 'Alice', 'Bob', 'Charlie'], ['Aman', 'Amin']]

#### Sort - in alphabetical order
```
Participants.sort()
print(Participants)
```
> ['Alice', 'Bob', 'Charlie', 'Gregory', 'Nasr']
```
Participants.sort(reverse=True)
print(Participants)
```
> ['Nasr', 'Gregory', 'Charlie', 'Bob', 'Alice']

### Tuples
- Tuples are *similar to lists*, but they are immutable (cannot be changed)
```
x = (40, 41, 42)
print(x)
```
> (40, 41, 42)
```
y = 50, 51, 52
print(y)
```
> (50, 51, 52)
```
a, b, c = 1, 4, 6
print(a, b, c)
```
> 1 4 6
```
x[1]
```
> 41
```
List_1 = [x, y]
print(List_1)
```
> [(40, 41, 42), (50, 51, 52)]
```
(age, years_of_school) = "30, 17".split(',')
print(age)
```
> 30
```
def square_info(x):
    A = x ** 2
    P = 4 * x
    print('Area and Perimeter')
    return A, P

square_info(3)
```
> Area and Perimeter  
> 9 12  

### Dictionaries
- objects
- use curly braces `{}`
```
dict = {'k1':'cat', 'k2':'dog', 'k3':'mouse', 'k4': 'fish'}
print(dict)
```
> {'k1': 'cat', 'k2': 'dog', 'k3': 'mouse', 'k4': 'fish'}
```
dict['k1']
```
> 'cat'
```
dict['k5'] = 'parrot'
print(dict)
```
> {'k1': 'cat', 'k2': 'dog', 'k3': 'mouse', 'k4': 'fish', 'k5': 'parrot'}
```
dict['k2'] = 'squirrel'
print(dict)
```
> {'k1': 'cat', 'k2': 'squirrel', 'k3': 'mouse', 'k4': 'fish', 'k5': 'parrot'}
```
dep_workers = {'dep_1': 'Peter', 'dep_2': ['Jennifer', 'Michael', 'Tommy']}
print(dep_workers)
```
> {'dep_1': 'Peter', 'dep_2': ['Jennifer', 'Michael', 'Tommy']}
```
Team = {}
Team['Point Guard'] = 'Dirk'
Team['Shooting Guard'] = 'Steve'
Team['Small Forward'] = 'James'
Team['Power Forward'] = 'Kevin'
Team['Center'] = 'Shaquille'
print(Team)
```
> {'Point Guard': 'Dirk', 'Shooting Guard': 'Steve', 'Small Forward': 'James', 'Power Forward': 'Kevin', 'Center': 'Shaquille'}
```
print(Team['Center'])
```
> Shaquille
```
print(Team.get('Center'))
```
> Shaquille
```
print(Team.get('Coach'))
```
> None

## Iteration
### For Loops
#### Basic Loop
```
even = [0,2,4,6,8,10,12,14,16,18,20]
for n in even:
    print(n)
```
> 0  
> 2  
> 4  
> 6  
> 8  
> 10  
> 12  
> 14  
> 16  
> 18  
> 20
#### Print with Space
```
for n in even:
    print(n, end = " ")
```
> 0 2 4 6 8 10 12 14 16 18 20

#### While Loops and Incrementing
```
x = 0
while x <= 20:
    print(x, end = ' ')
    x += 2
```
> 0 2 4 6 8 10 12 14 16 18 20

### Create Lists with range()
- range(start, stop, step)
  - start: the first number in the list
  - stop: the last value +1
  - step: the distance between each two consecutive values
```
range(10)
```
> range(0, 10)
```
list(range(10))
```
> [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```python
list(range(1,20,2))
```
> [1, 3, 5, 7, 9, 11, 13, 15, 17, 19]

### Use Conditional Statements and Loops Together
```
for x in range(20):
    if x % 2 == 0:
        print(x, end = " ")
    else:
        print("Odd", end = " ")
```
> 0 Odd 2 Odd 4 Odd 6 Odd 8 Odd 10 Odd 12 Odd 14 Odd 16 Odd 18 Odd
```
x = [0,1,2]
for item in x:
    print(item, end = " ")
```
> 0 1 2
```
for item in range(len(x)):
    print(x[item], end = " ")
```
> 0 1 2

### Conditional Statements, Functions and Loops
```
def count(x):
    c = 0
    for item in x:
        if item < 20:
            c += 1
    return c

x = [2,7,9,12,21,3,6,19,22,20]
print(count(x))
```
> 7

#### using Numpy
```
import numpy as np

x = np.array([2, 7, 9, 12, 21, 3, 6, 19, 22, 20])
count = np.sum(x < 20)

print(count)
```
> 7

#### Iterating over Dictionaries
- multiple dictionaries that contains same keys

```python
prices = {
    "spaghetti": 4,
    "lasagna": 5,
    "burger": 2
}
quantity = {
    "spaghetti": 6,
    "burger": 0,
    "lasagna": 10
}

money_spent = 0

for i in prices:
    money_spent += (prices[i] * quantity[i])

print(money_spent)
```
> 74


