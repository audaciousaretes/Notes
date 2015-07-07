### Floating

* `float: left;`
* `float: right;`
* `float: none'`

[Clearfix Hack](http://learnlayout.com/clearfix.html)

Other ways to clear your floats?


### Positioning

[CSS Positioning](https://developer.mozilla.org/en-US/docs/Web/CSS/position)

* `position:relative;`
* `position:absolute;`

Introduction of `top`, `right`, `bottom`, `left` and `z-index`


### Links / Resources

* [Learn Layout](http://learnlayout.com/)

## Forms

```html
<form action="location.html" method="post">

  <fieldset>

    <p><label for="input_area">Simple Input:</label>
      <input type="text" id="input_area" /></p>


    <p><label for="text_area">Text Area:</label>
        <textarea id="text_area"></textarea></p>

      <p><label for="select_element">Select Element:</label>
        <select name="select_element">
          <optgroup label="Option Group 1">
            <option value="1">Option 1</option>
            <option value="2">Option 2</option>
            <option value="3">Option 3</option>
          </optgroup>
          <optgroup label="Option Group 2">
            <option value="1">Option 1</option>
            <option value="2">Option 2</option>
            <option value="3">Option 3</option>
          </optgroup>
      </select></p>

      <p><label for="radio_buttons">Radio Buttons:</label>
        <label>
          <input type="radio" class="radio" name="radio_button" value="radio_1"> Radio 1
        </label>
        <label>
          <input type="radio" class="radio" name="radio_button" value="radio_2"> Radio 2
        </label>
        <label>
          <input type="radio" class="radio" name="radio_button" value="radio_3"> Radio 3
        </label>
      </p>

      <p><label for="checkboxes">Checkboxes:</label>
        <label>
          <input type="checkbox" class="checkbox" name="checkboxes" value="check_1"> Checkbox 1
        </label>
        <label>
          <input type="checkbox" class="checkbox" name="checkboxes" value="check_2"> Checkbox 2
        </label>
        <label>
          <input type="checkbox" class="checkbox" name="checkboxes" value="check_3"> Checkbox 3
        </label>
      </p>

      <p><label for="password">Password:</label>
        <input id="password" type="password" class="password" name="password">
      </p>

      <p><label for="file">File Input:</label>
        <input type="file" class="file" name="file">
      </p>


      <p><input class="button" type="submit" value="Submit"></p>

  </fieldset>


</form>
```
