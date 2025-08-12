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