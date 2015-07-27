# Functions
A function is a group of statements that can be called multiple times, and can be stored in a variable or passed around.

To put it another way: A function is an object that contains JavaScript code that is run when I call the function.

## Function declaration
A function declaration is a complete statement that can stand on its own. It creates a function with the name you specify.

```js
function coolFunction(thing) {
  alert(thing);
}
```

## Function expression
A function expression cannot stand on its own, but we can assign it to a variable or pass it to another function.

```js
var aFunction = function(thing) {
  alert(thing);
}

document.getElementById(id).addEventListener('click', function(){
  alert("Hay");
});
```

## IIFE

> Immediately Invoked Function Expression

> An IIFE protects a module’s scope from the environment in which it is placed.

```js
(function(){
  // my special code
}());
```

> By wrapping the anonymous function inside of parentheses, the JavaScript parser knows to treat the anonymous function as a function expression instead of a function declaration. A function expression can be called (invoked) immediately by using a set of parentheses, but a function declaration cannot be.


* Function Expression - `var test = function() {};`
* Function Declaration - `function test() {};`

#### Benefits

* Reduces the objects added to the window object
* Reduce scope lookups

  ```js
  (function(window, document, $){
    // my special code
  }(window, document, window.jQuery));
  ```

  > Note: JavaScript first looks for a property in the local scope, and then it goes all the way up the chain, last stopping at the global scope. Being able to place global objects in the local scope provides faster internal lookup speeds and performance.

## JavaScript `this`

A function's `this` keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.

We use `this` similar to how we use pronouns in the English language.

> Chase is a teacher at The Iron Yard, he really enjoys it.

In the above sentence, _he_ is referring to _Tim_

In JavaScript, `this` can refer to many different things depending on the context in which it is used.

# Arrays
A type that is an ordered list of values.

## Creating an array with literal syntax
- `var theArray = ['hay', 123]`

## Getting values out of an array
- `0` is the first index
- `var hay = theArray[0]`
- `var num = theArray[1]`

## Changing an array
- `theArray[1] = 321`
- `theArray[2] = "cool"`

## Array length
- `var length = theArray.length`


# Iteration Functions
## [forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

The reason to use forEach is have side effects for each item in an array.

### Examples
- Log each item
- Add something to an array or string for each item

```js
[1, 2, 3].forEach(function(num) {
  console.log(num);
});

// => 1
// => 2
// => 3
```

## map
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
The reason to use map is to transform *each* item in the array and get a new
array.

Etiquette says that map should never have side effect, though this isn't
enforced in any way.

```js
[1, 2, 3].map(function(num) {
  return num * 2;
});

// => [2, 4, 6]
```

## filter
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter

The reason to use filter is to get a new array that only contains items that
match the criteria you're looking for.

The internal function must return `true` or `false`.

Etiquette says that filter should never have side effect, though this isn't
enforced in any way.

```js
[1, 2, 3].filter(function(num) {
  return num >= 3;
});
// => [3]
```

## reduce
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

```js
[1, 2, 3].reduce(function(total, current) {
  return total + current;
});
// => 6
```
