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
        - [] to access the alphabet
    - Numbers
    - Arrays - wrap in square bracket ([])
    - Objects - wrap in {} and have key and definition seperate by colon (:)
    - Null (object)
    - Undefined (type)
    - Boolean (true/false)
