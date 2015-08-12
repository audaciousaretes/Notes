# Thursday, August 7, 2015

## jQuery

jQuery can be accessed in the browser as `$` and will almost always be used with the Sizzle Selector Engine.

When caching jQuery values in variables, it's a good idea to start the variable name with a `$` so it's easily discernable as a jQuery object.

To access an element by `id`, you can access it like this:

```
// with jQuery
var $myEl = $("#myElement");

// is the same as using this vanilla javascript
var myEl = document.getElementById("myElement");
```

To access an element by `class`, you can access it like this:

```
var $myActiveEls = $(".active");
```

This will return a list of Document Nodes matching `active` classes.

You can also access elements by element name:

```
var $myForms = $("form");
```

You can also use multiple selectors separated by `,`:

```
var $myVariousEls = $("form, .active, #myElement");
```

which will select all elements that are either `form` elements, elements with the class of `active` and the element with the id of `myElement`.

This will return a list of Document Nodes matching the `form` element.

### `.addClass();`

To add a class to an existing element, you use `addClass`. This javascript will add a class "aNewClass" the following HTML elements:

```
<div class="addToMe"></div>
<div class="dontAddToMe"></div>
<div class="addToMe"></div>
```

```
$(".addToMe").addClass("aNewClass");
```

Will change the `html` to:

```
<div class="addToMe aNewClass"></div>
<div class="dontAddToMe"></div>
<div class="addToMe aNewClass"></div>
```

### `.removeClass();`

To remove a class to an existing element you use `removeClass`. This javascript will remove a class "aNewClass" the following HTML elements:

```
<div class="addToMe aNewClass"></div>
<div class="dontAddToMe"></div>
<div class="addToMe aNewClass"></div>
```

```
$(".addToMe").removeClass("aNewClass");
```

Will change the `html` to:

```
<div class="addToMe"></div>
<div class="dontAddToMe"></div>
<div class="addToMe"></div>
```

### .toggleClass();

To toggle a class to an existing element you use `toggleClass`. This javascript will toggle a class "aNewClass" the following HTML elements:

```
<div class="addToMe aNewClass"></div>
<div class="dontAddToMe"></div>
<div class="addToMe aNewClass"></div>
```

```
$(".addToMe, .dontAddToMe").toggleClassClass("aNewClass");
```

Will change the `html` to:

```
<div class="addToMe"></div>
<div class="dontAddToMe aNewClass"></div>
<div class="addToMe"></div>
```

### `.text();`

To get the text inside of an element, you use `text`:

```
<!-- html -->
<div id="myElement">this is the <a href="#">text inside</a></div>
```

```
$("myElement").text() // => "this is the <a href="#">text inside</a>"
```

Note that it's not actually getting the `_html_`, but the text string including your `html`.

### `.append();`

To append something to an element, you use the `append` method. For example, to append `hello world` to `#myElement`, we would write:

```
<!-- html -->
<div id="myElement">this is the <a href="#">text inside</a></div>
```

```
$("myElement").append("hello world");
```

And the resulting `html` would be:

```
<!-- html -->
<div id="myElement">this is the <a href="#">text inside</a> hello world</div>
```

### `.prepend();`

To put something at hte beginning of an element, you would use `prepend`.


```
<!-- html -->
<div id="myElement">this is the <a href="#">text inside</a></div>
```

```
$("myElement").prepend("hello world ");
```

And the resulting `html` would be:

```
<!-- html -->
<div id="myElement">hello world this is the <a href="#">text inside</a></div>
```

### `.on();`

Often, you'll need to add an event listener to an element, and you do so by using `on`. As an example, if you wanted to add an event listener for a form with the id of `myForm` submission, you'd write something like this:

```
$("#myForm").on("submit", function(e) {
    e.preventDefault();
    // do some stuff
});

The first argument is an event (in this case it was "submit") and the second argument is the `callback` to fire when the event fires.

`e.preventDefault()` is a special method on events that will keep them from doing what they would normally do (in this case the page would normally do a hard refresh but won't because we're preventing the default)
