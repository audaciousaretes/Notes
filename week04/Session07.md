## Sass

#### Partials & Imports

`_reset.scss` - Normalize?

```css
@import 'reset';

body {
  font-size: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

#### Operators

```css
.container { width: 100%; }

article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complimentary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```

# JS 101

## JavaScript Syntax

```js
document.getElementById('header');
```

- `document`: object
- `.`: property accessor
- `getElementById`: property (in this case, a function)
- `()`: function call
- `'header'`: parameter (in this case, a String)
- `;`: end of the statement

## Statement
Like a sentence, a statement is one coherent "thought" or instruction.
- It should appear on its own line.
- It should end with a semicolon (a semicolon means "this instruction is over, move to the next one.")

## Comments
A comment is ignored by the JS engine.
- `//` starts a single line comment.
- `/*` starts a multiple line comment, `*/` ends the comment:
```js
// This is a single line comment.
console.log("Cool"); // It can be at the end too
/* This is a multiple line comment.
Cool right? */
```

## Types
There are two types of "things" in JavaScript:
### Primitives
Primitives are simple values that can be passed around and referenced directly. They are kind of like cash. If you give someone a $5 bill, they have the money and they can use it immediately.

### Objects
Objects are more abstract "things". They are like checks. They're too complex to be passed around or referenced directly, you have to know how to use them to actually get the value out of them.

## Primitives
### Numbers
```js
1;
3.14;
-20;
4.5e7;
```

### String
```js
'Cool';
"Cool";
"That was 'cool'";
"That was \"cool\"";
```

### Booleans
A boolean represents something that is true or false.
```js
true;
false;
10 > 5;
```

## Variable
Label for a value.

### Declare a variable
```js
var age;
```

### Assign a value to a variable

```js
age = 47;
```

A single equal sign is the "assignment operator".

### Shorthand

Declare and assign:
```js
var age = 47;
```

Declare multiple variables:
```js
var age, favoriteColor, name;
```

Declare and assign multiple:

```js
var age = 37, favoriteColor = "green", name = "Jake";
```

### Naming
- First character a-z, A-Z, $, `_`
- Variables starting with $ are often used for DOM objects
- Variables starting with `_` are often used for things that are not meant to be used by the developer
- The other characters can be letters, $, `_`, numbers
- They are case sensitive.
- The convention, but not rule, is to capitalize each word after the first:

```js
var someCoolVariable;
```

## Operators
- = (assignment)
- Number operators (+, -, /, *, ++, --, %)
- Compound assignments (+=, -=, *=, /*)
- String operator (+)

See https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators

# [Arithmetic
Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)

```js
4 + 3 // => 7
4 - 3 // => 1
4 * 3 // => 12
12 / 5 // => 2.4
12 % 5 // => 2
```

# [Comparison Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)
## Loose (they coerce the type)

```js
"cool" == "cool" // => true
"cool" != "dumb" // => true
1 == "1" // => true (it coerces the number into a string)
0 != false // => false (it coerces the number into a boolean)
12 > 5 // => true
12 >= 12 // => true
12 < 36 // => true
12 <= 12 // => true
```

## Strict (do not coerce the type)

```js
"cool" === "cool" // => true
"1" === 1 // => false
0 !== false // => true
```

# [Logical Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_Operators)

```js
!true // => false
!(10 > 5) // => false

true && true // => true
true && false // => false
(10 > 5) && (10 < 100) // => true
(10 > 5) && (10 < 10) // => false

true || true // => true
true || false // => true
false || false // => false
(10 > 5) || (10 < 100) // => true
(10 > 5) || (10 < 10) // => true
```

# [Assignment Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Assignment_Operators)
There are many available, but a couple of examples:

```js
var x;

x = 2;
x // => 2

x += 2;
x // => 4
```
# Conditionals

## if

```
if (true) {
  console.log("this is true!");
}
```

## if / else

```
if (isTrue) {
  console.log("isTrue is equal to true!");
} else {
  console.log("isTrue is equal to false!");
}
```

## ternary

```
var isTrue = 10 > 5 ? "is true!" : "is false!";
```

# Falsy
- `""`
- `0`
- `false`
- `undefined`
- `null`
- `NaN`

# Truthy
Everything else

```js
var name = "";
if(name){
  // this will not happen
  alert(name);
}
```

# for loop

```
for (var i = 1; i <= 100; i++) {
    console.log(i); // i = 1
}
```

first expression: initialized variables (var i = 0 to start the loop)
second expression: conditional to test (is i less than or equal to 100?)
third expression: code to execute after the loop has been evaluated. In this case, increment i by 1
