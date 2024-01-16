# JavaScript Notes

- [JavaScript Notes](#javascript-notes)
  - [Variables in JS](#variables-in-js)
    - [Declaring constants in JavaScript](#declaring-constants-in-javascript)


JavaScript is a language used along with HTML and CSS to communicate with the user.

 - `console.log("text")` is used to print something to the developer console in the browser
 - Link a **JS** script file to the html file by using command `<script src="javascript.js"></script>`


--------------------------------------------------


## Variables in JS

`let message;`

Now, put some data into the variable by using assignment operator `=` :

``` js
let message;

message = "Hello"; //store the string 'Hello' in the variable message
```

Access the stored variable **message** using the variable name :

`alert(message); // shows the variable content`

Variable declaration and printing its content in a more precise way as  :

``` js
let message = "Hello";
alert(message);
```

Declare multiple variables in single line (not recommended, use multi-lines or multiline style, where after comma each variable lies in a new line for readability) :

``` js
let user = 'John', age = 25, message = 'Hello'
```

> [!NOTE]
> In older scripts, `var` is used inplace of `let`   
> **Eg:** `var message = 'Ciao';`

> [!IMPORTANT]
>1. The name must only contain letters, digits or symbols **$** and **_**.
>2. The first character must not be digit.
>3. Case matters. **apple** and **APPLE** are differnet variables.
>4. Do not draw variables from [reserved words](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#reserved_words)

> When the name contains multiple words, <b>camelCase</b> is commonly used. That is: words go one after another, each word except first starting with a capital letter: **myVeryLongName**


### Declaring constants in JavaScript

`const myBirthday = '18.04.1982`;`

Any attempt to reassign value would result in error.

1. We generally use upper case for constants that we "hard-coded" i.e.,  when the value is known prior to execution and directly written into the code.
**Eg :** birthday, planet count etc.

-----------------------------------------------