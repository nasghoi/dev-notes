# JavaScript course
by **Smoljames** on [YouTube](https://www.youtube.com/watch?v=-ihpNX0EODc) and [Udemy](https://www.udemy.com/course/the-complete-javascript-course-zero-to-hero)
> Learn Repo - [Basic](https://github.com/nasghoi/javascript-for-beginner) & [Complete](https://github.com/nasghoi/the-complete-javascript-course)

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

## Data Manipulation
- every character is **index** (starts with 0)
    - plus (+) to combine string (string concatenation)
    - ```indexOf()``` method to access the *index* of the character (position) -> return -1 if the char doesnt exist
    - ```split()``` method does a lot of actions -> return in *array* format
        - split('') - no space for separate per character
        - split(' ') - single space for separate per word
        - split('i') - remove any 'i' character
        ```
        let example_sentence = 'this is string'
        const split_sentence = example_sentence.split('i')
        console.log(split_sentence)
        ```
        > output: [ 'th', 's ', 's str', 'ng' ]
    - ```includes()``` method to check either exist or not -> return true/false (boolean)
    - ```replaceAll()``` method to replace all char with new char
    ```
    let example_u_sentence = 'this_is_a_string'
    const replace = example_u_sentence.replaceAll('_', ' ')
    console.log(replace)
    ```
    - ```slice()``` method to slice out the strings based on the *index* position
    ```
    const slice = example_u_sentence.slice(4)
    console.log(slice)
    ```
    > output: _is_a_string
    ```
    const slice = example_u_sentence.slice(4, 9)
    console.log(slice)
    ```
    > output: _is_a
    - and [many more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects) built-in javascript method
- REGEX -> pattern check to validate the input
    - use chatgpt and type the prompt `write some password regex in javascript`
    - next prompt `show me how to implement the regex check for a password in javascript`
    ```
    function validatePassword(password) {
        // Strong password have min 8 chars, upper, lower, number, special
        const regex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[\W_])[A-Za-z\d\W_]{8,}$/;
        return regex.test(password);
    }

    const password = "StrongPass1!";
    if (validatePassword(password)) {
        console.log("✅ Password is valid");
    } else {
        console.log("❌ Password is invalid");
    }
    ```
    > output: ✅ Password is valid (since the pw is follow all the pattern required)

## Array and Lists
- the item of the array can be accessed by index location -> return *undefined* if the item of the index number doesnt exist
```
let simple_array = ['nasr', 'is', 'cool']
console.log(simple_array[2])
```
> output: cool
- manipulate an array
    - replace/add new item by index location
    ```
    simple_array[1] = 'was'
    simple_array[3] = 'and'
    console.log(simple_array)
    ```
    > output: [ 'nasr', 'was', 'cool', 'and' ]
    - built in js array method()
        - push() ->  add new item at **the end** of the array
        ```
        simple_array.push('right?')
        console.log(simple_array)
        ```
        > output: [ 'nasr', 'is', 'cool', 'right?' ]
        - pop() -> remove **the last** item from the array
        ```
        simple_array.pop()
        console.log(simple_array)
        ```
        > output: [ 'nasr', 'is' ]
        - join() -> joining all the items in array into a string, seperate by anything we put in the parentheses
        ```
        let joined_string = simple_array.join('_')
        console.log(joined_string)
        ```
        > output: nasr_is_cool
        - reverse() -> inverting the items in the array
        ```
        let reversed_array = simple_array.reverse()
        console.log(reversed_array)
        ```
        > output: [ 'cool', 'is', 'nasr' ]
        - sort() -> arrange string in array based on their UTF-16 code units
        - slice() but in *array* term
        ```
            let number_array = [1, 2, 3, 4, 5]
        ``` 
        
        one argument (start/end) -> automatically the *end* == undefined -> the slice extends to the end of the array / if *start* undefined, than the slice starts from index 0
        ```
        let end_array = number_array.slice(2)
        console.log(end_array)
        ```
        > output: [ 3, 4, 5 ]

        two arguments (start, end) -> pick the range in the argument
        ```
        let start_array = number_array.slice(0, 2)
        console.log(start_array)
        ```
        > output: [ 1, 2 ]

## Object aka Dictionary
- key can be wrapped in a string quotes (more preffered) or just use underscore to connect each words
> hobbies_or_interests / 'hobbies or interests'

- access the value of the key
    - using **square bracket** notation ```[]``` (must wrap with string quote) -> [] for dynamic (especially)
    ```
    const bio = {
        name: 'nasr',
        age: 25,
        hobbies: ['coding', 'gaming', 'gym'],
    }

    let name_key = 'name'
    let name = bio[name_key]
    console.log(name)
    ```
    > output: nasr
    - using **dot** notation ```.``` -> . for non-dynamic
    ```
    bio.age = 26 // update using dot notation
    console.log(bio.age)
    ```
    > output: 26
    - for access in array
    ```
    console.log(bio['hobbies'][0], bio.hobbies[1])
    ```
    > output: coding gaming
    
- update the value (can use dot ```.``` too like above example)
```
bio[name_key] = 'nasrul'
let name = bio[name_key]
console.log(name)
```
> output: nasrul

- add new key to dictionary
```
bio['number_of_friends'] = 2
console.log(bio)
```
> output: { name: 'nasrul', age: 25, hobbies: [ 'coding', 'gaming', 'gym' ], number_of_friends: 2 }

- check the key exist in dictionary or not - use (key in object) -> return boolean (true/false)
```
if ('age' in bio) {
    console.log('age exists')
} else {
    bio['age'] = null
    console.log('age does not exist')
}
console.log(bio)
```
- delete the key
```
delete bio.age // or delete bio['age']
console.log(bio)
```
> output: {  name: 'nasrul', hobbies: [ 'coding', 'gaming', 'gym' ] }

- access dimensional dictionary (object)
```
// let say updated dictionary
const bio = {
    name: 'nasr',
    age: 25,
    hobbies: ['coding', 'gaming', 'gym'],
    friends: {
        'nab': {
            description: 'pretty',
        }
    }
}

console.log(bio.friends.nab.description, bio.friends['nab'].description, bio['friends']['nab']['description'])
```
> output: pretty pretty pretty

- ```Object.keys()``` -> access list of dictionary **keys**
```
const keys_in_object = Object.keys(bio)
console.log(keys_in_object)
```
> output: [ 'name', 'hobbies', 'friends', 'number_of_friends' ]

- ```Object.values()``` -> access list of dictionary **values**
```
const values_in_object = Object.values(bio)
console.log(values_in_object)
```
> output: [ 'nasrul', [ 'coding', 'gaming', 'gym' ], { nab: { description: 'pretty' } }, 0 ]

- ```Object.entries()``` -> return **to array (keys and associated value)** from dictionary
```
const entries_in_object = Object.entries(bio)
console.log(entries_in_object)
```
> output:
> [
>   [ 'name', 'nasrul' ],
>   [ 'hobbies', [ 'coding', 'gaming', 'gym' ] ],
>   [ 'friends', { nab: [Object] } ],
>   [ 'number_of_friends', 0 ]
> ]
- ```undefined``` -> access non-exist keys or values
```
console.log(bio.joke, 'joke' in bio)
```
> output: undefined false

## Scope and Closure
- **Global** scope: the highest level of the folder
- **Closure**: function is defined in *another* function
```
function counter() {
    let count = 0

    return function() {
        count++
        console.log(count)
    }
}

let increment = counter()
increment()
increment()
```
> output:
> 1
> 2

## Modular and Reusable code
- seperate javasript to numerous file where each file is modular
    1. add export syntax at the file that we want to export
    ```
    // chap-2.js
    let quotes = {
        nas: 'is cool',
        nab: 'isn\'t cool, she\'s hot', // use backslash before the single quote to escape it
        number_of_our_child: 3,
        is_we_happily_married: true,
    }

    function addStrings(string1 = 'default1', string2 = 'default2') {
        let concatString = string1 + ' ' + string2
        console.log(concatString)
        return concatString
    }

    module.exports = {
        addStrings,
        quotes,
    }
    ```
    2. add import syntax at the that we want to use the functions
    ```
    // chap-3.js
    const { addStrings, quotes } = require("./chap-2");
    ```
    3. And now, its already can be use
    ```
    // chap-3.js
    addStrings('hello', 'world')
    console.log(quotes.nas)
    ```
    > output:
    > hello world
    > is cool

## Error Handling Techniques and Debugging Tools
- **Try Catch** block -> if try block is error(breaks), its run catch block
```
const brokenObject = {
    word: 'nice',
}

function problematicCodeBlock() {
    try {
        console.log('test') // debugging
        const sub_object = brokenObject.hello.world
        console.log(sub_object)
    } catch (err) {
        console.error(err.message)
    }
}

problematicCodeBlock()
console.log('code continues')
```
> output:
> test
> Cannot read properties of undefined (reading 'world')
> code continues
- custom throw error
```
throw new Error('custom error message')
```
> output: (typical throw error messages)
- debugging tools? -> **JUST USE ```console.log()``` !!**