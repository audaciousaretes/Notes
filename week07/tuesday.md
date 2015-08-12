# Tuesday, August 11, 2015

## JSON

Every key should be surrounded in **double quotes** and can have the following types of values:

- `String`
- `Number`
- `Boolean`
- `Array`
- `Object`

```
{
    "name": "Chase Adams",
    "age": 31,
    "attributes": {
        "eye_color": "blue",
        "hair_color": "blonde",
        "height": {
            "feet": 6,
            "inches": 1
        }
    },
    "gender": "male",
    "alive": true,
    "hobbies": [ "wood working", "javascript", "writing"]
}
```

In javascript, you can create a string out of a `JSON object` by using `JSON.stringify`, where `stringify` takes the `JSON object` as its parameter. It converts the previous object into:

```
"{"name":"Chase Adams","age":31,"attributes":{"eye_color":"blue","hair_color":"blonde","height":{"feet":6,"inches":1}},"gender":"male","alive":true,"hobbies":["wood working","javascript","writing"]}"
```

To convert that back into an object, you can use `JSON.parse`, where `parse` takes the `string` as its parameter

## Local Storage

Local Storage is a property on the `window` object that allows you to store and read persisted data stored indefinitely.

To add something to Local Storage, you use `localStorage.<keyname>` where `<keyname>` is the key you want to store it to. For instance, if I wanted to add my name to localStorage, I could do so like this:

```
localStorage.myName = "Chase Adams";
```

And to access it, I can do:

```
console.log(localStorage.myName);
```

## Objective

Using `localStorage` and the `JSON` methods, write functions that access an array of todos stored in localStorage.
