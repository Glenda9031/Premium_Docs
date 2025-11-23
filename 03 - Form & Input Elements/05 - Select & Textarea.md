# Select & Textarea

We looked at a few of the common text-based fields in the previous lesson. In this lesson, we will look at the `select` and `textarea` elements.

## Select Element

The `select` element is used to create a dropdown list. It is a great way to present a list of options to the user. The `select` element is made up of `option` elements. Each `option` element represents an item in the dropdown list and has a `value` attribute that is sent to the server when the form is submitted.

Here is an example of a select element:

```html
<h1>Tech Support</h1>
<form>
  <label for="select">Select a product:</label>
  <br />
  <select id="select" name="product">
    <option value="iphone">iPhone</option>
    <option value="imac">iMac</option>
    <option value="macbook">Macbook</option>
    <option value="macbook-pro">Macbook Pro</option>
  </select>
  <br />
  <input type="submit" value="Submit" />
</form>
```

If we selected the `iMac` option and submitted the form, the value `imac` would be sent to the server.

### `multiple` Attribute

You can allow users to select multiple options by adding the `multiple` attribute to the `select` element:

```html
<select id="select" name="product" multiple></select>
```

Now, users can select multiple options by holding down the `Ctrl` key (or `Cmd` key on Mac) while clicking on the options.

### `size` Attribute

You can specify the number of visible options by adding the `size` attribute to the `select` element:

```html
<select id="select" name="product" size="2" multiple></select>
```

This will display two options at a time, and the user can scroll to see more options.

### `selected` Attribute

You can pre-select an option by adding the `selected` attribute to the `option` element:

```html
<select id="select" name="product" size="2" multiple>
  <option value="iphone">iPhone</option>
  <option value="imac" selected>iMac</option>
  <option value="macbook">Macbook</option>
  <option value="macbook-pro">Macbook Pro</option>
</select>
```

In this example, the `iMac` option will be pre-selected.

## Textarea Element

The `textarea` element is used to create a multi-line text input field. It is useful when you want users to enter longer text, such as comments or messages.

Let's add a `textarea` element to our form:

```html
<form>
  <label for="select">Select a product:</label>
  <br />
  <select id="select" name="product" size="2" multiple>
    <option value="iphone">iPhone</option>
    <option value="imac" selected>iMac</option>
    <option value="macbook">Macbook</option>
    <option value="macbook-pro">Macbook Pro</option>
  </select>
  <br />
  <label for="textarea">Enter your message:</label><br />
  <textarea
    id="textarea"
    name="message"
    placeholder="Describe the issue"
  ></textarea>
  <br />
  <input type="submit" value="Submit" />
</form>
```

The `textarea` element has an opening and closing tag, and any text between the tags will be the default value of the textarea. You can also set the number of rows and columns by adding the `rows` and `cols` attributes:

```html
<textarea id="textarea" name="message" rows="4" cols="50"></textarea>
```

Now it looks a little better, but still pretty bad with no CSS.
