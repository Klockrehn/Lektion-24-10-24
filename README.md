# Lektion-24-10-24
Lektion 24-10-24
We start with the foundations when it comes to JS. Data types, variables, user-input and output, operators och if-statements.
# Lektion-24-10-24
Lektion 24-10-24

### String
 string is just a collection of characters with in quotes. It can be both double quotes and single quote. But there also exist a third way of writing strings.
 
 ```js 
"Johan" // valid string
'Johan' // valid string
`Johan` // valid string
 ```
 
 These above are all equal, but the backticks-version have some extra functionality.

 For instance, backtics allows multiline strings. The other two dont't.

 ```js
 "My name
 is Johan" // This wont work in a js file.

 `My name
 is Johan" // This works just fine.
 ```

 Another example of added funtionality with backtics is the avility to inject variables inside the string, if it is defined woth backtics. 

 ```js
 const name = "Johan";
 const lastName = "Rehn";

 `Hello, my name is ${name} ${lastName}!`
``` 

This is also called a string literal.

If we want to do the same thing with regular quation marks, we need to concatinate _(add)_,

```js
const name = "Johan";
const lastName = "Rehn";
"Hello, my name is " + name + lastName + ".";
``` 

### Number
Represents number, both integers and decimal values. Just remember that decimal values are written with a perios and not a coma.

```js
35 // valid number
45.3 // valid number
```

### Boolean

A boolean represent either true or false.

### Date
A date is just a value that represents a date or time.

```js 
const now = new Date();
```

This 'new date()' returns a date object that we can manipulate in many ways, and use in our applications.  

### Variables
Variables is a way of storing values in reuseable packages so to speak.

| Feature |
`var`
`let`
`const`

Scope - vart variables är tillängliga.

### Var 

`var` is a key word that is used to create variables. And the key word is always paired with a variables name and a value. And the values can of course be of different data types.

```js 
var firstName = "Johan"; 
console.log(firstName);
```

`var` has some special characteristics, one of them is that it is re-declarable that means we can declare the same variable again with a new value.

```js 
var firstName = "Johan"; 
console.log(firstName);

var firstName = "Jerry";
console.log(firstName); // Jerry
```

You can also re-assign the value on a var.

```js 
var firstName = "Jerry";
console.log(firstName); // Jerry

firstName = "Sebbe"; // Re-assignment, its valid
console.log(firstName); // Sebbe 
```

`Var` also has the Function scoop, what is that? If a `var` is declared inside a function, only lives inside the function. But if `var` is declared on the top level of a JS-file, it gets a "global scoop" which means is accesable inside the entired JS-file. 

Because of this, DON'T use `var` at all! Use the newer ones `let` and `const`. 

### Const 

`const` os also a key word for creating variables. It stands for 'constant' which means it is supposed to be constent. It means we souldn't change this variable after it has been created. 

```js
const age = "22"; 
console.log(age); // 22

age = 45 // Wont work, VSC will sometimes complain and browser will ALWAYS complain. 
```

We can not re-declare a `const`. 

```js
const age = 22;
const age = 45; // Won't work, VSC will complain.
```

`const` has a block scoop, which means if it's created inside of a pair of brackets, it only lives in there. If it's created at the top os a JS-file it lives inside the entire file. 

```js 
const name = "Johan"; 

if(true) {
    
    const lastName = "Rehn";
    console.log(name); //Johan
}
    console.log(name); // Exists
    console.log(lastName); // Doesn't exist in this scope.
