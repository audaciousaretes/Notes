# Thursday, July 30, 2015

## Objects
Objects are containers of values, including functions, arrays, and other objects.

## Literal syntax
```js
var theObject = {
  someProperty: "cool",
  anotherProperty: ['things', 'another thing']
};
```

## Properties
Properties are like variables on objects.

```js
var theObject = {
  someProperty: "cool",
  someOtherProperty: ["hay", "guyz"]
}

// New properties are created automatically when you assign to them
theObject.thirdThing = 123;

// Access properties with the dot (.)
var num = theObject.thirdThing;

// Or with brackets and strings
var cool = thirdThing['cool']
```

[Eloquent Javascript: The Secret Life of Objects](http://eloquentjavascript.net/06_object.html)
