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
```

### Let

This is the last key word we can ues in order to create variables. It is very similar to `const` but we are allowed to re-assign a `let`-variable.

```js
let streetName = "Jerrys Biceps Vägen"; 
streetName = "Jerrys Biceps Vägen"; // This is totally fine
```

This is fine, but we can also change the data type if we would like to.

```js 
let id = "dadadad"; 
id = "asdf"; // Works just fine, fine datatype doesn't exist. 
```

Even though this is allowed it's not recommended. Keep it clean, only one data type per variable. 

### If Statements

A `if` statement is just a way for the application to decide which way to go. Simply put. Depending on ceratin condisions that we define, the application can do one thing or the other. Usually an application consists of hundreds of condition in different combinations, so it's a essential/fundamental tool to know about when coding. 

What a statement means is also a good thing to know. It just means a set of instrucions that the computer follows.

### Basic if-syntax

```js 

if(condition) {
    // code to be executed if the condition is true.

}
```

`if` is the key word that tells the compiler that an if check is declared. The condition is a value that can be evaluated to either `true` or `false`. The code block contains the code that is execuded when the condition is `true`.

```js 
const age = 20; 

if (age>18) {
    console.log("You are an adult");
}
``` 

This is fine, if we just want to check if the conditions is `true`, but what if it's `false`, maybe we want to handle that cae as well. Let's look at the `else` key word. 

In this case and example, we want to console.log something, if we are nt above the age of 18.

```js
const age = 20; 

if (age>18) {
    console.log("You are an adult"); // If true write this.
}

else (age<18) {
    console.log("You are younger then the size of Jerrys biceps.") // If false write this.
}
```

This is called an if-else statement. It is very common of course. 

### Comparison operators

In order to evaluate our conditions we need tools for that, and they are called comparison operators. It's the characters that we use to compare the variables or whatever it is we are comparing. 

### >, <, -- greatar than, or less than

Operator to check if something is greater then, or less then. It's very straight forward. 

### >=, <= -- greater than or equal, less than or equal

Same as above but with the added possibility for the "terms". (In lack of a better word), to be equal to eachother

### == -- equal (but NOT strict)

The compare the two things to see if they are equal but no strict equal. It means that we can compare to calues of different data types, and still get a `true`value. This is called equal with cohersion. It means that the editor or browser will try to convert one of the values to the other data type. 

```js 
"10" == 10 // => Will be true
"100" == "Hundred" // => Will be false, since they don't have the same kind of value. 
```
### === -- equal (AND strict)

Same as above but the values must be of the same data type. 

```js 
"10" === 10; // Will be false due to different data types. 
10 === 10; // True.
```

In the majority of cases, always go for the strict equal comparison. 

### != -- NOT equal (NOT strict)

### !== -- NOT equal (AND strict)

### If-else-if statements
So if we want to do more specific checks it original one was ecaluated `false`, we can always do more if checks or we can chain it in a if-else-if  chain. 

The difference is that if we have a chain of if-else-if, only one of the checks will run, which means, if on of the checks in the chain is true, the rest will be ignored.

If we just do a number of if checks after each other, every if check will still run even though one of them was evaluated to `true`. 

Here is a simple syntax. 

```js 
const age = 16;
if (age >= 18) {
    console.log("Great, you can take your driver's license.")
} 
else if (age <= 16>) {
console.log ("Sorry, you are not old enough for a driver's license, but you can start practising." );
} 
else {
    console.log("Sorry, you will have to take the bike... Or Jerrys biceps");
}
```

### Nested if-statements

If you want to do a check that is dependent on another check you can always nest if statements. But beaware, it often leads to messy code that is hard to read. But it's totally fine to do it. 

```js
if (condition) {
    if (condition based on earlier condition) {
        // code to run if nested check is true
    }
    // code that always run if original condition is true
}
```

Färre indenteringar - lättare att läsa! 

### Truly and falsy values

Sometimes we just want to evaluate variables directly, for instance, we want to see if a variable is defined or not.

```js 
const name = "Johan"{
    if (name) {
        console.log (`Cool name, Mr $ {name}!`);
    }
}
```

### Logical operators
If you want to compare severall conditiosn at the same time you can use `logical operators`. 

### && - Logical AND 
Used to check conditions and all of them must be true in order for the entire condition to be true as well.

```js
const isAnAdult = true
const isCool = true;

if (isAnAdult && isCool) {
    console.log("Wow, you are both an adult and cool!") // Will run because all is true. 
}
```
In the above case all the smaller conditions must be true in order for the entire if check to be evaluated to `true`. 

### || Logical OR
Is used to evalute a if check to true if either one of the "smaller" conditions is true. 
```js
const isAnAdult = false
const isCool = true;

if (isAnAdult || isCool) {
    console.log("Wow, you are both an adult and cool!") // Will run because one of them is true. 
}
```

Remember the conditions is evaluated from left to right. If we have a "||", it only needs to check the first condition if thats true in order to evaluat the entire expression to true.

Same with "&&", left to right. If the first is `true` it must check the second one. If one of them is false it ignore the rest and evaluate everything to `false`

### ! Logical NOT 
If you put an exclemationmark before and variable or condition it will be inverted. So if oyu write !true, it will be !false. And !false will be !true

```js 
firstName = ""; 
if (name){
    //some code, wont run since it falsy.
}

if (!name){
    // this will run because of the exclemationmark inverts the result of the evaluation. 
}
```

