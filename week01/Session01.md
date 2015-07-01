# HTML 101
- HTML is a language used to describe the structure of web pages.
- CSS is a language used to describe the appearance of web pages.
- An element is composed of three parts: an opening tag, content, and a closing
  tag. There are a few elements, like `<img>`, that are an exception to this rule.
- All html documents should have tags for `<html>`, `<head>`, and `<body>`.
- `<head>` is information *about* the document.
- `<body>` is the content of the document.
- Elements can have attributes as well. Attributes are written inside the
  opening tag of an element, e.g. the 'src' in `<img src="image.jpg">`
  - The ones you'll use the most are 'src', 'id' and 'class' [reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes)
  - `id` will always be unique and `class` names you can reuse.
- Most whitespace (tabs, returns, spaces) is ignored by the browser, but you can
  use it to make your HTML more readable.

# Links
- You can create a link element with the `<a>` tag. You specify the location to
  link to in the `href` attribute of the tag and the title in the content, e.g.
  `<a href="http://theironyard.com">The Iron Yard</a>`
- You can use words or an image as the content for a link.

# Paths (for src and href)
- A relative path points to another file on your website, relative to the page
  that you are typing the link in.
- In a path, `..` indicates the parent directory.
- The parts of the path should be separated with the `/` character.
- Links that are pointed to an incorrect page will show an error when you click
  on them, images that are pointed to an incorrect path will show a little
  broken image icon.
- You shouldn't use spaces in the names you give to files or folders you'll be
  using in paths.

# Block vs inline
- Block level elements like `<p>` ol, ul, li and `<blockquote>` appear on their
  own line and expand all the way to the left and right of their container.

# Semantics
- You should always use the element that is closest to meaning to the type of
  your content, even if the appearance is incorrect. You can adjust the
  appearance with CSS.

# Void elements
- Some elements are "void", meaning they don't have a closing tag. The most
  common examples are `<img>` and `<link>`

# Lists
- If you are creating a list of items, like a navigation bar or a list of links,
  it would not be best practice to create a list manually in a `<p>`, etc.
  Instead you should always use a list element (.e.g. `<ol>`, `<ul>`) and the
  items should be contained by a list item tag (`<li>`).

# Images
- Use the `<img>` tag to add an image to your page. You specify the source of
  the image with the `src` attribute. The source can be a file on your site, or
  an external URL.

# Validation
- The validator at http://html5.validator.nu is a free online service that
  checks pages for compliance with standards.

# CSS 101


* [The Ah-Ha Moment](http://css-tricks.com/the-css-ah-ha-moment/)
* Every page element is a box.
* I can control the size and position of those boxes.
* I can give those boxes background images.


## CSS Rules
- A block of CSS code that applies properties to a selection of elements is
  called a "rule".
- A rule is made up of a "selector" and one or more property declarations.
- The selector specifies the set of elements the rule applies to.
- A property declaration is made up of a property name and one or more property
  values.
- Each property declaration ends with a semicolon
- The list of property declarations goes between curly braces (i.e. `{ }`)

### Example

```css
div > a // selector
{
  border-color: red;
  // property: value;
  // Also, the whole line is a "rule"
}

::before { } // pseudoelement
:hover { } // pseudoclass

// Muliple selectors for a group of rules

a:hover,
a:active {
   color: chartreuse;
}
```

## Other Notes
- CSS can be written inside a `<style>` tag inside the `<head>`, but it's best
  practice to put CSS in an external file and link to it using `
- To select the elements of a certain HTML tag, the selector is just the tag
  name (e.g. `p { }`)
- Many CSS properties are inherited. For example, if I set `font-size: 62.5%;`
  on the `<body>` element, then all the elements on the page that don't override
  `font-size` will inherit that font size.
- To find out whether a property is inherited by its children, look up the
  property on MDN (or Dash.app)

## CSS inheritance and specificity
- CSS can be overriden by declaring a property farther down the "cascade".
- The highest priority rules are "inline", i.e. defined on the `style` attribute
  of a element. This is almost never a good practice to do in your HTML, but is
  often useful when manipulating styles from JavaScript.
- Styles in a `<style>` tag have lower priority than inline styles.
- Styles in an external CSS file have lower priority than `<style>` rules
- You can also override properties by writing a more specific rule. E.g.
  `.my-link` is more specific than `a`, and `a.my-link` is most specific.
- The article [CSS Specificity: Things You Should
  Know](http://www.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/)
  gives an overview of specificity rules.
- A class can be added to an element with the `class` attribute.
- Use a `.` between the element name and the class name to select the elements
  of that tag and class.
- Use `.classname` to select all elements of that class.

## Bonus Material

This is an _exhaustive_ list of properties you can "tinker" with. Try them out to see
what they do.

[CSS Properties Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)
[HTML attribute reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
