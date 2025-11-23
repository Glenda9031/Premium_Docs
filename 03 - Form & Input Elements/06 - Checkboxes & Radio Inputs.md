# Checkboxes & Radio Inputs

Like with select lists, checkboxes and radio inputs are used to collect multiple-choice data from users. Checkboxes allow users to select multiple options, while radio inputs allow users to select only one option.

## Checkboxes

Checkboxes are created using the `<input>` tag with the `type` attribute set to `checkbox`. Each checkbox should have a unique `id` attribute and a corresponding `<label>` element. The `for` attribute of the `<label>` should match the `id` attribute of the `<input>` element to associate the label with the checkbox.

Checkboxes should also have a `name` attribute to group them together as well as a value to specify what that particular checkboxes value is. When the form is submitted, the selected checkboxes will be sent as an array with the same name.

Let's create a simple form with checkboxes for a user's favorite programming languages:

```html
<h2>Favorite Programming Languages</h2>
<form>
  <label for="html">
    <input type="checkbox" id="html" name="languages" value="html" />
    HTML
  </label>

  <label for="css">
    <input type="checkbox" id="css" name="languages" value="css" />
    CSS
  </label>

  <label for="javascript">
    <input
      type="checkbox"
      id="javascript"
      name="languages"
      value="javascript"
    />
    JavaScript
  </label>

  <button type="submit">Submit</button>
</form>
```

As you can see, each checkbox is associated with a label. When the user clicks on the label, the corresponding checkbox will be checked. This makes it easier for users to interact with the form. They all have the same name attribute, which groups them together. When the form is submitted, the selected checkboxes will be sent as an array with the name `languages`.

### `checked` Attribute

You can pre-select checkboxes by adding the `checked` attribute to the `<input>` element. This will automatically check the checkbox when the page loads.

```html
<label for="html">
  <input type="checkbox" id="html" name="languages" value="html" checked />
  HTML
</label>
```

### `disabled` Attribute

You can disable checkboxes by adding the `disabled` attribute to the `<input>` element. This will prevent users from interacting with the checkbox.

```html
<label for="html">
  <input
    type="checkbox"
    id="html"
    name="languages"
    value="html"
    checked
    disabled
  />
  HTML
</label>
```

## Radio Inputs

Radio inputs are created using the `<input>` tag with the `type` attribute set to `radio`. Each radio input should have a unique `id` attribute and a corresponding `<label>` element. The `for` attribute of the `<label>` should match the `id` attribute of the `<input>` element to associate the label with the radio input.

Radio inputs should also have a `name` attribute to group them together. This ensures that only one radio input can be selected at a time. When the form is submitted, the selected radio input will be sent with the same name.

Let's create a simple form with radio inputs for a product's size:

```html
<h2>Product Size</h2>
<form>
  <label for="small">
    <input type="radio" id="small" name="size" value="small" />
    Small
  </label>

  <label for="medium">
    <input type="radio" id="medium" name="size" value="medium" />
    Medium
  </label>

  <label for="large">
    <input type="radio" id="large" name="size" value="large" />
    Large
  </label>

  <button type="submit">Submit</button>
</form>
```

Just like with checkboxes, each radio input is associated with a label. They all have the same name attribute, which groups them together. When the form is submitted, the selected radio input will be sent with the name `size`.
