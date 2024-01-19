# JavaScript Notes

- [JavaScript Notes](#javascript-notes)
  - [Variables in JS](#variables-in-js)
    - [Declaring constants in JavaScript](#declaring-constants-in-javascript)

JavaScript is a language used along with HTML and CSS to communicate with the user.

- `console.log("text")` is used to print something to the developer console in the browser
- Link a **JS** script file to the html file by using command `<script src="javascript.js"></script>`

---

## Variables in JS

`let message;`

Now, put some data into the variable by using assignment operator `=` :

```js
let message;

message = "Hello"; //store the string 'Hello' in the variable message
```

Access the stored variable **message** using the variable name :

`alert(message); // shows the variable content`

Variable declaration and printing its content in a more precise way as :

```js
let message = "Hello";
alert(message);
```

Declare multiple variables in single line (not recommended, use multi-lines or multiline style, where after comma each variable lies in a new line for readability) :

```js
let user = "John",
  age = 25,
  message = "Hello";
```

> [!NOTE]
> In older scripts, `var` is used inplace of `let`  
> **Eg:** `var message = 'Ciao';`

> [!IMPORTANT]
> 
> 1. The name must only contain letters, digits or symbols **$** and **\_**.
> 2. The first character must not be digit.
> 3. Case matters. **apple** and **APPLE** are differnet variables.
> 4. Do not draw variables from [reserved words](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#reserved_words)

> When the name contains multiple words, <b>camelCase</b> is commonly used. That is: words go one after another, each word except first starting with a capital letter: **myVeryLongName**

### Declaring constants in JavaScript

`const myBirthday = '18.04.1982;`

Any attempt to reassign value would result in error.

1. We generally use upper case for constants that we "hard-coded" i.e., when the value is known prior to execution and directly written into the code.
   **Eg :** birthday, planet count etc.

---

## String Literals  & Multi-line Strings

Use backtick (`) in place of ' ' or " "

```js
const firstName = "stranger";
const firstJob = "writer";
const birthYear = 1901;

desc = `I'm ${firstName} and my first job was ${firstJob}.`;
console.log(desc);
// I am stranger and I was born in 1901 and my first job was writer
```

**Multi-line Strings**

Strarting from 2015, thanks to ES6, multi-line strings can be written like below :

```js
console.log(`
I'm a party worker
from Sevastopol.
I came here yesterday.`);
```

**Note :** Don't forget to use backticks (`) instead of ' or " for the string.

------------------------------------------

## Type Conversion and Coercion

```js
const inputYear = "1991";
console.log(typeof inputYear); // 1991
console.log(Number(inputYear) + 18); // 2009
console.log(Number('Jonas')); //NaN
console.log(typeof NaN); // number

// Type Coercion
console.log("24" + 2); // 242
console.log("12" * "12"); // 144
```

---------------------------------------------------------------------------------------------------------------------

## Truthy & Falsy Values

```js
// Truthy and Falsy Values

console.log(Boolean(0)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean({})); //true
console.log(Boolean("")); // false

const money = 0;
if (money) {
  console.log("Don't spend it all!");
} else {
  console.log("Earn money First!");
} // Earn money First !!!

let height;
if (height) {
  console.log("Good! Height is defined!");
} else {
  console.log("Please define height!!!");
} // Please define Height!!!
```

--------------------------------------

## Operators

### Equality Operators

`===` and `==` are equality operators.

```js
// Equality Operators
const age = 18;

if (age === 18) console.log("You are an adult!!!! (strict)");
// You are an adult !!!! (strict) === > Comparison Operator
if (age == 18) console.log("You are an adult!!!! (strict)");
// You are an adult !!!! (loose) == > Comparison Operator

// Always use strict equality operator (===) over loose equality operator (==)
```

```js
const favNum = Number(prompt("What's your favorite Number ?"));
console.log(`Your favorite number is ${favNum}`);

if (favNum === 23) {
  console.log(`23 is a favorite number`);
}
//  === strictly treats the variable as a string.
// Thus the if condition is not true
else if (favNum === 16) {
  console.log(`16 is the second fav number`);
} else if (favNum !== 16) {
  console.log(`16 is not the second fav number`);
} else {
  console.log(`Not a favorite number`);
}
```

```js
// Boolean Logic Basics
let isIsland = false;
let isPeninsula = true;

console.log(`AND result for the statements : ${isIsland && isPeninsula}`); // false
console.log(`OR result for the statements : ${isIsland || isPeninsula}`); // true
console.log(`NOT result for the statements : ${!isIsland || !isPeninsula}`); //true
```

### Ternary (Conditional) Operator

```js
// Conditional Operator

const age = 25;
age >= 18
  ? console.log(`I like to drink wine 🍷 (❁´◡\`❁)`)
  : console.log(`I had to drink water 💧 
😒`); // `I had to drink water 💧 😒`
```

```js
// Conditional Operator
let age = 15;
const drink = age >= 18 ? "wine 🍷" : "water 💧";
console.log(drink); // water 💧

let drink2;
if (age >= 18) {
  drink2 = "wine 🍷";
} else {
  drink2 = "water 💧";
}
console.log(drink2); // water 💧
console.log(`I like to drink ${age >= 18 ? "wine 🍷" : "water 💧"}`); // water 💧
```

## Switch Statements

```js
// Switch Statements
const day = "thursday";

switch (day) {
  case "monday":
    console.log("Plan my course");
    console.log("Go to coding meetup");
    break;
  case "tuesday":
    console.log("Prepare course material");
    console.log("Sheen the roof");
    break;
  case "wednesday":
    console.log("Record Vids");
    break;
  case "thursday":
    console.log("Upload the vids");
    break;
  default:
    console.log("Not a valid day.");
}
```

## JavaScript Releases

**Brief History of JS:**

- Brendan Eich creates the first version of JavaScript in 10 days. Initially called **Mocha**

- EcmaScript 1 released in 1997

- **ES5** released in 2015 with lots of great new features.

- **ES6** brought biggest updates to the language. **ECMAScript* * changes to yearly releases.

- Modern JavaScript Engine is backwards compatible.

## Strict Mode

```js
"use strict"; // Activates strict mode for the entire script file
```

- Avoids accidental bugs and errors in the code.

- Prefer to turn on Strict Mode while coding.



## Functions

```js
// Functions
function logger() {
  // Function Definition
  console.log("My Name is John");
}
logger(); // Function Calling/ invoking / running

function fruitProcessor(apples, oranges) {
  console.log(apples, oranges);
  const juice = `Juice with ${apples} apples and ${oranges} oranges.`;
  return juice;
}

const appleJuice = fruitProcessor(5, 6);
console.log(appleJuice);
// My Name is John
// 5 6
// Juice with 5 appleas and 6 oranges
```
