# JavaScript course
by **Smoljames** on [YouTube](https://www.youtube.com/watch?v=-ihpNX0EODc)
> Learn Repo - https://github.com/nasghoi/javascript-for-beginner

## Intro
- JavaScript is like recipe that have instructions
- The recipe is read by the computer (JavaScript runtime)
- Computer execute the instructions and produce the output
- JavaScript runtime known as *NodeJS*

## NodeJS
- enter command ```node -v``` for checking the version of the NodeJS
- run javascript file ```node <file_name>```
- kill javascript file ```ctrl + c```

## Variables
- console.log() to output to the console
- variable cannot have *space*
- use camelCase, snake_case
- type of assign
    - let (allow to reassign a new value)
    - const (not allowed to assign new value)

## Comments
- use // for one line
- use /*  */ for wrap up line

## Assignment by Reference
- assign value to a new variable from another variable
```
numberOfPeople = 6;
let newNumberOfPeople = numberOfPeople;
```
> now, newNumberOfPeople have value 6

## Data Types
- *cannot* declare same variable name TWICE
- init, read, write
    - Strings - wrap in single ('') or double quotes ("")
        - concat using plus (+) 
        - square bracket [] to access the alphabet
        - backslash ( \ ) to escape the (eg. single quote)
         ``` let her = 'isn\'t cool, she\'s hot' ```
    - Numbers
    - Arrays - wrap in square bracket ([])
    - Objects - wrap in {} and have key and definition seperate by colon (:)
    - Null (object)
    - Undefined (type)
    - Boolean (true/false)

## Operators
- to do mathematical operation
- add (+), substract (-), multiply (x), divide (/), remainder (%)
- remainder always use to know the number is odd or even
```
const isEven = 12 % 2 === 0;
const isOdd = 12 % 2 !== 0;
```

## Logical Operators
- to make double condition (see below if else block example)
    - && (AND) -> ALL condition need to be TRUE
    - || (OR) -> AT LEAST ONE condition need to be TRUE
    - ! (NOT) -> to INVERSE the boolean value

## Conditional Statements
- if else
```
const x = 21
if (x > 10 && x < 20) {
    // Whatever code is written here is conditionally executed
    console.log('The value is greater than 10, and also less than 20');
} else {
    console.log('The value is not greater than 10, or it is greater than 20');
}

if (x > 10 || x < 20) {
    // Whatever code is written here is conditionally executed
    console.log('The value is greater than 10, or also less than 20');
} else {
    console.log('The value is not greater than 10, or it is greater than 20');
}
```

## Type Of
- use to know what is the data type of the value
```
const randomNumber = 101;
console.log(typeof randomNumber, typeof 'string', typeof true, typeof null, typeof undefined); 
``` 
> output: number string boolean object undefined

## Loops
- powerful to run tasks in infinite numbers
- scope in loop is just in loop (const)
    - while
    ```
    let i = 0;
    while (i < 20) {
        console.log('The value of i is:', i);
        i = i + 1; //increment
    }
    ```
    - for -> takes three (3) arguments (tracking variable; condition; increment)
    ```
    for (let j = 0; j < 20; j++) {
        // this is repeateble code
        console.log('The value of j is:', j);
    }
    ```
    - continue -> skip the loop
    ```
    const animals = ['cat', 'dog', 'fish', 'bird'];

    for (let k = 0; k < animals.length; k++) {
        const currentAnimal = animals[k];
        if (currentAnimal === 'dog') {
            continue;
        }
        console.log('The animal at index ' + k + ' is ' + currentAnimal);
    }
    ```
    > output: The animal at index 0 is cat, The animal at index 2 is fish, The animal at index 3 is bird
    - break -> stop the loop
    ```
    const animals = ['cat', 'dog', 'fish', 'bird'];

    for (let k = 0; k < animals.length; k++) {
        const currentAnimal = animals[k];
        if (currentAnimal === 'dog') {
            break;
        }
        console.log('The animal at index ' + k + ' is ' + currentAnimal);
    }
    ```
    > output: The animal at index 0 is cat
- ```.length``` -> get the **count** of element in array
```
const animals = ['cat', 'dog', 'fish', 'bird'];

for (let k = 0; k < animals.length; k++) {
    console.log('The animal at index ' + k + ' is ' + animals[k]);
}
```

## Functions
- use ```function``` keyword
```
function printSquare() {
    // This function prints out the square of a number
    console.log(4 * 4)
}
printSquare(); // invoke (call) a function
```
- circular the parentheses to wrap the *arguements*
```
function printRectangle(y, z) {
    console.log(y * z)
}
printRectangle(4, 6); // enter the value in the parentheses
```
- use ```return``` to return the value and exit the function block
```
function addStrings(str1, str2) {
    // This function adds two strings together
    strings = str1 + str2;
    if(typeof str1 !== 'string' || typeof str2 !== 'string') {
        return 'Nothing to show';
    }
    return strings;
}
const result = addStrings('hello', 'world');
console.log(result);
```
- default values
``` function addStrings(str1 = 'hello', str2 = 'world') {} ```
- arrow function -> modern js syntax
> () => {}
```
const arrowFunction = (arg) => {
    console.log('ARG: ' + arg);
}
arrowFunction('oyasumi');
``` 