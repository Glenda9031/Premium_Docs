# Datalist

The `<datalist>` element contains a set of `<option>` elements that represent the values available for other controls. They are similar to select boxes except, in addition to being displayed in a drop-down list, they can be used to provide a list of suggested values for other controls.

Let's create a basic datalist element:

```html
<label for="favLanguage">Favorite Programming Language:</label>
<input list="lanuages" id="favLanguage" name="favLanguage" />
<datalist id="lanuages">
  <option value="JavaScript"></option>
  <option value="PHP"></option>
  <option value="Python"></option>
  <option value="C"></option>
  <option value="C#"></option>
  <option value="Java"></option>
  <option value="Ruby"></option>
</datalist>
```

As you can see, it is very simlar to a select list, but we can also add a custom value in addition to the options.

The `list` attribute of the `<input>` element should be equal to the `id` of the `<datalist>` element.

## Times

Let's create a time select with some popular times:

```html
<input type="time" list="popularHours" />
<datalist id="popularHours">
  <option value="12:00"></option>
  <option value="13:00"></option>
  <option value="14:00"></option>
</datalist>
```

## Range Ticks

We can use the range input with a datalist to create a slider with custom ticks:

```html
<label for="tick">Tip amount:</label>
<input type="range" list="tickmarks" min="0" max="100" id="tick" name="tick" />
<datalist id="tickmarks">
  <option value="0"></option>
  <option value="10"></option>
  <option value="20"></option>
  <option value="30"></option>
  <option value="40"></option>
  <option value="50"></option>
  <option value="60"></option>
  <option value="70"></option>
  <option value="80"></option>
  <option value="90"></option>
  <option value="100"></option>
</datalist>
```

## Colors

We can even use a color picker with some pre-defined options:

```html
<label for="colors">Pick a color (preferably a red tone):</label>
<input type="color" list="redColors" id="colors" />
<datalist id="redColors">
  <option value="#800000"></option>
  <option value="#8B0000"></option>
  <option value="#A52A2A"></option>
  <option value="#DC143C"></option>
</datalist>
```
