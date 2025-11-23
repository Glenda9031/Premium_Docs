# Text Input Attributes

In this lesson, I just want to look at some attributes that we can add to text inputs to make them more user-friendly.

## `placeholder` Attribute

The `placeholder` attribute is used to provide a hint or example of the expected value of an input field. It is displayed in the input field when it is empty and disappears when the user starts typing. Let's add a placeholder to the fields.

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" placeholder="Enter name" />

  <label for="email">Email:</label>
  <input type="email" id="email" placeholder="Enter name" />

  <label for="password">Password:</label>
  <input type="password" id="password" placeholder="Enter name" />

  <button type="submit">Submit</button>
</form>
```

Before the placeholder attribute was available, we would add a value and use JavaScript to clear the input field when the user clicked on it. The placeholder attribute is a much simpler and more user-friendly solution.

## `value` Attribute

Speaking of the `value` attribute, it is used to set the initial value of an input field. This is useful when you want to pre-fill the field with a default value. Let's add a value to the email field.

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" placeholder="Enter name" />

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="Enter email"
    value="test@test.com"
  />

  <label for="password">Password:</label>
  <input type="password" id="password" placeholder="Enter password" />

  <button type="submit">Submit</button>
</form>
```

Now the email is pre-filled.

## `name` Attribute

The `name` attribute is used to identify the input field when the form is submitted. It is sent to the server along with the value of the input field. Let's add a name to the fields.

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" placeholder="Enter name" name="name" />

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="Enter email"
    value="test@test.com"
    name="email"
  />

  <label for="password">Password:</label>
  <input
    type="password"
    id="password"
    placeholder="Enter password"
    name="password"
  />

  <button type="submit">Submit</button>
</form>
```

## `required` Attribute

The `required` attribute is used to specify that an input field must be filled out before submitting the form. If the user tries to submit the form without filling out the required field, the browser will display an error message. Let's add the required attribute to all of the fields.

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" placeholder="Enter name" name="name" required />

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="Enter email"
    value="test@test.com"
    name="email"
    required
  />

  <label for="password">Password:</label>
  <input
    type="password"
    id="password"
    placeholder="Enter password"
    name="password"
    required
  />

  <button type="submit">Submit</button>
</form>
```

Now when you try to submit the form without filling out the fields, the browser will display an error message.

## `minlength` and `maxlength` Attributes

The `minlength` and `maxlength` attributes are used to specify the minimum and maximum number of characters that can be entered. Let's add a minlength of 6 for the password and a maxlength of 10 for the name:

```html
<form>
  <label for="name">Name:</label>
  <input
    type="text"
    id="name"
    placeholder="Enter name"
    name="name"
    required
    maxlength="10"
  />

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="Enter email"
    value="test@test.com"
    name="email"
    required
  />

  <label for="password">Password:</label>
  <input
    type="password"
    id="password"
    placeholder="Enter password"
    name="password"
    required
    minlength="6"
  />

  <button type="submit">Submit</button>
</form>
```

Now the name field will only allow a maximum of 10 characters and the password field will require a minimum of 6 characters.

## `disabled` Attribute

The `disabled` attribute is used to disable an input field. This means that the user cannot interact with the field and it will not be submitted with the form. Let's disable the email field:

```html
<form>
  <label for="name">Name:</label>
  <input
    type="text"
    id="name"
    placeholder="Enter name"
    name="name"
    required
    maxlength="10"
  />

  <label for="email">Email:</label>
  <input
    type="email"
    id="email"
    placeholder="Enter email"
    value="test@test.com"
    name="email"
    required
    disabled
  />

  <label for="password">Password:</label>
  <input
    type="password"
    id="password"
    placeholder="Enter password"
    name="password"
    required
    minlength="6"
  />

  <button type="submit">Submit</button>
</form>
```

This doesn't make much sense in this context, but it can be useful in certain situations.

Those are the most common attributes that you're going to use with inputs.
