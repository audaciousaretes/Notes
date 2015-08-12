# Tuesday, August 5, 2015

## setTimeout and setInterval
Ways to do tasks/functions/things asynchronously at a set delay or set interval.

### setTimeout(function, ms)

- This means that 'x' milliseconds from now, place the contained function in the
  execution queue.  The amount of time set will not be exact.
- This can be used to prevent the user interface (UI) from being blocked while a
  browser is processing.  ex: setTimeout (function, 0)

### setInterval(function, ms)

- This means that this function will be repeated every 'x' milliseconds.
- Use clearInterval to stop the call.

## Underscore.js

Underscore is a JavaScript library that provides a lot of functional programming that you would normally see in other languages (like Ruby or Python) and it does all of it without extending any of the built-in JavaScript objects.

Underscore.js is a cool little JavaScript library that brings a ton of functionality at a around 4kb.

> Also, you can checkout [Lodash](http://lodash.com) as an alternative. I'm fine no matter which one you choose.

### Underscore Functions

```js
// Some Data
var people = [
        {
                name: 'Tim',
                location: 'Atlanta'
        },
        {
                name: 'Jeff',
                location: 'Kansas City'
        },
        {
                name: 'Doug',
                location: 'Topeka'
        },
        {
                name: 'Bill',
                location: 'Ft. Myers'
        }
];

// Let's Iterate
_.each(people, function (p) {
        console.log(p);
});

// Let's Map a new array
var greetings = _.map(people, function (p) {
        return "Hi, my name is " + p.name;
});
console.log(greetings); // ["Hi, my name is Tim", "Hi, my name is Jeff", "Hi, my name is Doug", "Hi, my name is Bill"]

// Let's search through our array for one single object
var bill = _.findWhere(people, {name: "Bill"});
console.log(bill); // Object {name: "Bill", location: "Ft. Myers"}

// Let's `pluck` out a specific set of data
var locations = _.pluck(people, 'location');
console.log(locations); // ["Atlanta", "Kansas City", "Topeka", "Ft. Myers"]
```

### Underscore Templates

```html
<script type="text/template" id="item-template">
    <li class="item">
        Item Name: <%= name %>
    </li>
</script>
```

```js
<script type="text/javascript">

    // Grab the template string.
    var templateString = $('#item-template').text();

    // Turn it into a template function.
    var renderTemplate = _.template(templateString);

    // Pass in an object. Return value is a string
    // with the bee stings replaced with object's properties
    var freshHTML = renderTemplate({name: 'Beer Mug'});

    // Inject the fresh html into the page.
    $('.some-container').append(freshHTML);

</script>
```

#### Looping IN template

> Be careful doing this. While you can do this in Underscore/Lodash, be careful not to go too nuts and put too much logic in your templates. I prefer to keep as much logic in my JS file as possible but there is some nice ways this comes in handy.

```js
var string_of_html = $('#animal_template').html();
var rendered_function = _.template(string_of_html);
var final_rendered_html;

$('.hero-unit ul').append(rendered_function(animals));
```

```html
<% _.each(animals, function (a) { %>
  <li>
    <% if (a.name === 'Whale') { %>
    I don't like whales!
    <% } else { %>
    Hi, I am an <%= a.name %> and I live in <%= a.location %>.
    <% } %>
  </li>
<% }); %>
```
