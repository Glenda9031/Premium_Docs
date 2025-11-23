# Other Input Types

There are a few other input types that you can use in forms. These include:

- `color`
- `date`
- `time`
- `month`
- `week`
- `range`
- `url`

Let's create a form with these input types:

```html
<form>
  <label for="color">Color:</label>
  <input type="color" id="color" name="color" />

  <label for="date">Date:</label>
  <input type="date" id="date" name="date" />

  <label for="time">Time:</label>
  <input type="time" id="time" name="time" />

  <label for="month">Month:</label>
  <input type="month" id="month" name="month" />

  <label for="week">Week:</label>
  <input type="week" id="week" name="week" />

  <label for="range">Range:</label>
  <input type="range" id="range" name="range" min="0" max="100" />

  <label for="url">URL:</label>
  <input type="url" id="url" name="url" />

  <button type="submit">Submit</button>
</form>
```

These input types provide different ways for users to input data. For example, the `color` input type allows users to select a color from a color picker, the `date` input type allows users to select a date from a calendar, and the `range` input type allows users to select a value from a range.
