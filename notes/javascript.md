# JavaScript course
by **Smoljames** on [YouTube](https://www.youtube.com/watch?v=-ihpNX0EODc) and [Udemy](https://www.udemy.com/course/the-complete-javascript-course-zero-to-hero)
> Learning Repo - [Basic](https://github.com/nasghoi/javascript-for-beginner) & [Complete](https://github.com/nasghoi/the-complete-javascript-course)

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

## Document Object Model (DOM), Event Handling
- JavaScript interactive version in web browser works with HTML, CSS
- log the output in console
```
<!-- before close the body -->
<script>
    console.log('hello')
</script>
```
> output: hello
- ```getElementById()``` to access/update the element in html by the id value
```
<body>
    <button id="open-modal-btn">Open Modal</button>
    <script>
        let modalBtn = document.getElementById('open-modal-btn')
        modalBtn.innerText = 'hi mom'
        // console.log(modalBtn.innerText)
    </script>
</body>
```
> output: the button text change to 'hi mom'
- ```addEventListener()``` -> interact with the element
```
<body>
    <button id="open-modal-btn">Open Modal</button>
    <script>
        let modalBtn = document.getElementById('open-modal-btn')
        function handleOpenModal() {
            console.log(modalBtn.innerText)
        }
        modalBtn.addEventListener('click', handleOpenModal)
    </script>
</body>
```
> output: the console output the 'Open Modal' when we click that button
- ```querySelector()``` -> select the class name of the element
```
<body>
    <div id="modal" class="modal" style="display: flex;">
        <div class="modal-content">
            <span class="close" style="cursor: pointer;">&times;</span>
            <p>Some text in the Modal..</p>
            <button id="close-modal-btn">Close Modal</button>
        </div>
    </div>
    <script>
        let modal = document.getElementById('modal')
        let xBtn = document.querySelector('.close')
        // style with query selector
        let newHTML = document.querySelector('#content-area h1').style.background = 'yellow'      

        function handleCloseModal() {
            modal.style.display = 'none'
        }

        xBtn.addEventListener('click', handleCloseModal) // use mouseover for hover action
    </script>
</body>
```
- ```element.innerText``` -> access the **text** on the element
```
let modalBtn = document.getElementById('open-modal-btn')
modalBtn.innerText = 'hi mom'
```
- ```element.style``` -> access the **style** of the element
```
let modal = document.getElementById('modal')
modal.style.display = 'flex'
```
- ```element.value``` -> access the **value** of the element
```
let textArea = document.getElementById('text-area')
textArea.value = 'this is me'
```
- ```element.innerHTML``` -> access the **HTML** of the element
```
<body>
    <div id="content-area">
        <h1>Hi mom</h1>
    </div>
    <script>
        let contentArea = document.getElementById('content-area')
        console.log(contentArea.innerHTML)
    </script>
</body>
```
> output:         <h1>Hi mom</h1>
- ```<script>``` in ```<head>``` -> import script from another file, add the source of the js file
```
<html>
    <head>
        <script src="chap-2.js" defer></script>
    </head>
    <body>

    </body>
</html>
```
> The ```defer``` attribute on a ```<script>``` tag tells the browser to download the script in *parallel* with parsing the HTML, but to execute the script ONLY AFTER the HTML document has been fully parsed and loaded.
- ```createElement()``` -> create an element to html
```
// create a new <li> element, set its text content to "New Item", and append it to an existing <ul> with the ID list-container
let newItem = document.createElement('li')
newItem.innerText = 'New Item'
```
- ```appendChild()``` -> adds a node to the end of the list of children of a specified parent node.
```
// continue from above
let listContainer = document.getElementById('list-container')
listContainer.appendChild(newItem)
```
- ```e.stopPropogation()```
- ```removeEventListener()```
- ```setAttribute()```
- ```classList.toggle()```

## Object Oriented Programming
- define template to use it again and again
- ```constructor()``` -> create property
```
class Person {
    // class body
    constructor(name, age) {
        this.name = name // name is property of the class
        this.age = age
    }
}

const you = new Person('Jaey', 24)
const them = new Person('Raf', 17)

console.log(you, them)
```
> output: Person { name: 'Jaey', age: 24 } Person { name: 'Raf', age: 17 }
- ```method()``` -> behaviour of the object
```
class Person {
    // class body
    constructor(name, age) {
        this.name = name // name is property of the class
        this.age = age
    }

    greet() {
        console.log('Hello, I am ' + this.name + ' and I am ' + this.age + ' years old')
    }
}
const you = new Person('Jaey', 24)
you.greet()
```
> output: Hello, I am Jaey and I am 24 years old
- ```this``` inside method *refers* to the object itself.
    - Accessing instance-specific data: When you say this.name, you're referring to the name property of this particular object instance.
    - Calling other methods on the same instance: this.someOtherMethod().
    - Creating and initializing new instances: Within constructors (new keyword or class constructor).
    
- **Inheritance** -> use ```extends``` &  ```super()```
```
class Gamer extends Person {
    constructor(name, age, games) {
        super(name, age) // just like import the property from parent
        this.games = games
    }
}

const guy = new Gamer('Man', 23, 'EA')

console.log(guy)
```
> output: Gamer { name: 'Man', age: 23, games: 'EA' }
- **Getters** & **Setters** -> to get or set the information
> actually, we can update the value without using s/g (direct property access), but with s/g could acts as an "interceptor".
```
class MyClass {
    constructor(name) {
        this._name = name
    }

    get name() {
        console.log('Fetch current name') // we can console this with s/g
        return this._name
    }

    set name(value) {
        this._name = value
    }
}

const obj = new MyClass('nab')
console.log(obj.name)
obj.name = 'nas'
console.log(obj.name)
```
> output: nab nas

## Asynchronous Programming
- synchronous -> execute line by line (in order)
- async -> cant run in sequential order
- HTTP -> server in point
- API -> communication
- Promise -> i promise i'll return value
- ```await```
    - wait the promise to complete
    - only can be use in ```async``` function block 
- use ```try catch``` block to handle fetch error
```
async function fetchData() {
    try {
        const res = await fetch('https://dummyjson.com/products/1')
        const data = await res.json()
        console.log(data)
    } catch (err) {
        console.error(err.message)
    }
}

fetchData()
```
- use ```options``` for use RESTful method (POST, PUT, DELETE)
```
async function postUserData() {
    try {
        const options = {
            method: 'POST',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({ name: 'james'})
        }
        const res = await fetch('https://api.example.com/users', options)
        const data = await res.json()
    } catch (err) {
        console.error(err.message)
    }
}

postUserData()
```

## Modern ES6+
- arrow function ```=>```
```
const myFunction = (input) => {
  console.log("executed function");
};
```
- ternary operator ```?```
```
let friends = ['nasr', 'nab', 'fah']

// old if else
// if (friends.includes('nasr')) {
//     isNabFriend = true
// } else {
//     isNabFriend = true
// }
        
let isNabFriend = friends.includes('nasr') ? true : false

console.log(isNabFriend)
```
- optional chaining ```?``` -> undefined safe operator
```
const nasr = {
    hobbies: {
        skiing: {
            pairs_of_skis: 1
        }
    }
}

console.log(nasr?.hobbies?.yeke.yeke)
console.log(nasr?.['hobbies']?.yeke.yeke)
```
> output: undefined
- object destructuring -> ease the define
```
let person = {
    name: 'nasr',
    age: 25
}
// let name = person.name
// let age = person.age

const { name: person_name, age } = person

console.log(person_name, age)
```
> output: nasr 25
- array destructuring -> ease to define
```
let oldArray = [4, 5]

// let value1 = oldArray[0]
// let value2 = oldArray[1]

let [value1, value2] = oldArray

console.log(value1)
```
> output: 4
- template literal string -> simplify the string concat
```
let my_name = 'nasr'
// console.log('my name is ' + my_name + ' and i like the 3/8 is ' + 3/8)
console.log(`hello my name is ${my_name} and i like the 3/8 is ${3/8}`)
```
- short circuits
    - ```AND (&&)``` returns the value of the *second operand* if first operand is **truthy**
    ```
    let person_dict = { name: 'nas' }
    let person_name_2 = person_dict.name && 'nab'
    console.log(person_name_2)
    ```
    > output: nab
    - ```OR (||)``` returns the value of the *second operand* if first operand is **falsy**
    ```
    let person_name_3 = person_dict.name || 'default name'
    console.log(person_name_3)
    ```
    > output: nas
- enhanced object literals
```
let breed = 'mazda'
let animal = 'car'

const animal_info = {
    breed,
    animal
}
console.log(animal_info)
```
> output: { breed: 'mazda', animal: 'car' }
- spread operator ```...``` -> take all the value and spread them out like we write it new
    - array
    ```
    let demo_array = [1, 2, 3, 4, 5]
    let demo_array_2 = [...demo_array, 6, 7, 8]
    console.log(demo_array_2)
    ```
    > output: [ 1, 2, 3, 4, 5, 6, 7, 8 ]
    - object
    ```
    let demo_object = {
        fav_color: 'blue'
    }

    let demo_object_2 = {
        ...demo_object,
        fav_food: 'oat'
    }
    console.log(demo_object_2)
    ```
    > output: { fav_color: 'blue', fav_food: 'oat' }
- array methods
```
let my_cool_array = [6, 9, 54, 74, 33, 76]
```

1. foreach
```
my_cool_array.forEach((value, index) => {
    console.log(`the current value is ${value} and the index is ${index}`)
})
```
> output:  
> the current value is 6 and the index is 0
> the current value is 9 and the index is 1
> the current value is 54 and the index is 2
> the current value is 74 and the index is 3
> the current value is 33 and the index is 4
> the current value is 76 and the index is 5

2. map
```
let my_new_array = my_cool_array.map((value, index) => {
    return value * 2
})

console.log(my_new_array)
```
> output: [ 12, 18, 108, 148, 66, 152 ]

3. filter
```
let filtered_array = my_cool_array.filter((value, index) => {
    let is_even = value % 2 === 0 
    return !is_even
})

console.log(filtered_array)
```
> output: [ 9, 33 ]

4. reduce
```
let reduced_array = my_cool_array.reduce((accumulator, value, index) => {
    return accumulator + `, [${index}]${value}`
}, '')

console.log(reduced_array)
```
> output: , [0]6, [1]9, [2]54, [3]74, [4]33, [5]76

- ```npm init -y``` -> to generate **package.json** file
    - everything is double quotes (```""```)
    - add scripts in package.json to run the command
    ```
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "console": "node notes/chap-7.js"
    },
    // run in terminal -> npm run console
    ```
- ```npm install [package_name]``` -> install package
```
// import to use the package
const express = require('express')
import { Express } from "express" // destructure style if use module type in package.json
```

## JavaScript Best Practices

### Better Performance & Efficiency
- Minimise DOM manipulations
- Efficient event listeners
- Optimize loops (continue, break)
- Choose correct data structure (objects, arrays)
    - need label? -> objects
    - doesnt need label, just list? -> arrays
- caching data -> speed up reloading (memorization)
- monitor performance 
- web apis & libraries (network request, latency)
### Coding best practices, write clean and maintainable code
- use *best naming* for variable, function (to others read, to revisit after a number of months)
- code *commenting* (to easily understand the code)
- avoid *convoluted statement* (hard to understand)
### Big O notation
![big-o-notation](/images/big-o-notation.png)
- **meaning**: systems that allow to describe the complexity of the task
- O -> *operation*
- Use ```for...in``` when you need to access the **keys** (property names) of an object.
- Use ```for...of``` when you need to access the **values** of an array or any other iterable collection.

## Project Findings
### Project 1 (Compound Interest Calculator)
```npm install prompt-sync``` -> for installing prompt-sync package  
```const prompt = require('prompt-sync')()``` -> to use in js file
```
// how to use it
let user_input = prompt('Enter your message ');
```
> output: Enter your message [enter input here]
### Project 2 (AI Chatbot)
get access to OPENAI API Key
```
import OpenAI from "openai";
import { createRequire } from "module"; // to use require
const require = createRequire(import.meta.url);
import "dotenv/config";
const OPENAI_SECRET_KEY = process.env.OPENAI_SECRET_KEY; // to get from .env
```
### Project 3 (Todo App)
save data in **local storage**
```
// define
let todo_list = localStorage.getItem("todo-list") ? JSON.parse(localStorage.getItem("todo-list")) : []

// persist all information in localStorage
function saveData() {
    localStorage.setItem("todo-list", JSON.stringify(todo_list));
}
```
### Project 4 (JSON Database)
```npm init -y``` -> to use require() in file  
1. use filesystems(fs) for saving data in local file
```const fs = require("fs");```
2. read JSON object from file
```const data = fs.readFileSync(dbName, "utf-8");```
3. parse JSON (JSON -> Object)
```const convertedData = JSON.parse(data);```
4. convert object to JSON (Object -> JSON) **must send in object format
```let convertedData = JSON.stringify(obj)```
5. write to the file (dbName is a json file name. eg. 'db.json')
```fs.writeFileSync(dbName, convertedData)```
6. export function to use in other js file
```module.exports = { readDb, writeDb }```
