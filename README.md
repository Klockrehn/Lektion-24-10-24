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

```js
const 