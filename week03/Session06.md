## Sass

#### Installing Sass

Documentation - http://sass-lang.com/

```sh
$ gem install sass
$ sass -v
```

## Sass Demo

#### Processing Sass

```sh
# Compile once
$ sass input.scss output.css

# Or Watch your files
$ sass --watch input.scss:output.css
```

#### Variables
```css
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

#### Nesting

```css
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

#### Mixins

```css
@mixin border-radius($radius) {
  border-radius: $radius;
}

.box { @include border-radius(10px); }
```

## Responsive Web Design

* Sam Kapila's Checklist [RWD Handy Checklist](http://samkap.github.io/projects/tiy-rwd/)

#### HTML Setup

1. Add a `meta` `viewport` in your head (`index.html` already had that)
2. Add a link to your stylesheet like usual
3. Create a container element... will be useful later.
        * Generally, I set a `max-width` on it.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link href="style.css" type="text/css" rel="stylesheet">

<div class="container"></div>
```

#### Flexible Layout

* Keep anything `left` or `right` or or `width` related in percents (except max-widths)
* Use pixels or ems for anything `top`, `bottom`, or `height` related.
* Also, as a general rule, all `width` should be in percentages except max-widths (most cases)

#### Mobile First

* Use media queries from smallest to largest (mobile-first approach)
* You also begin with a global CSS that does not need to be in a media query.
* `min-width` vs `max-width`

```css
@media (min-width: 1200px) {

}
```

```css
/*Default styles*/
.col-6 {
  float: left;
  width: 50%;
}

/*Display 3 per row for medium displays (like mobile phones in landscape or smaller tablets)*/
@media (max-width: 600px) {
  .col-6 {
    width: 100%;
  }
}
```

#### Flexible Images (& Videos)

Usually applied globaly

```css
img {max-width:100;}
```

[FitVids](http://fitvidsjs.com/)

## Resources

* [The Article that Started it All](http://alistapart.com/article/responsive-web-design)
* [Mobile First](http://www.html5rocks.com/en/mobile/responsivedesign/)
* [Mobile First (another one)](http://zurb.com/word/mobile-first)
* [Nice Examples](http://mediaqueri.es/)
* [MDN Media Queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)
