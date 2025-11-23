# Styling Forms

There are a few things that I would like to go over when it comes to styling forms. We have pseudo classes like `:placeholder-shown`, `:focus-within`, `:valid`, `:invalid`. There are states and some other general styling that we can do.

Let's use the following HTML:

```html
<div class="container">
  <h2>Contact Us</h2>
  <form>
    <label for="name">Name:</label>
    <input
      type="text"
      id="name"
      name="name"
      placeholder="Enter your name"
      required
    />

    <label for="email">Email:</label>
    <input
      type="email"
      id="email"
      name="email"
      placeholder="Enter your email"
      required
    />

    <label for="message">Message:</label>
    <textarea
      id="message"
      name="message"
      placeholder="Enter your message"
      required
    ></textarea>

    <input type="submit" value="Submit" />
  </form>
</div>
```

And the following base CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.container {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 300px;
}

h2 {
  text-align: center;
  margin-bottom: 20px;
}
```

We have a basic form and everything is placed in the center of the page. Let's style the form.

We will start with the label. Labels are inline by default and you usually want the label on top of the input. We can change the display to block and add some margin to the bottom.

```css
label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}
```

Next, the inputs. Inputs are really ugly by default. SOme of the first things I do to inputs are add some padding, width, and border. I also like to add a border-radius to make them look a bit nicer.

If you remember a few lessons ago, we looked at attribute selectors. We can use those to style the inputs. We can select all inputs and textareas and give them the same styles.

```css
input[type='text'],
input[type='email'],
textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
```

You also usually want to make the textarea a bit taller. We can do that by setting the height.

```css
textarea {
  height: 100px;
}
```

The submit button is also ugly by default. You can also use either a button or an input. In this case, we are using an input, that's one of the reasons that we needed to use the attribute selector to style the inputs above.

Let's style the input button:

```css
input[type='submit'] {
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

input[type='submit']:hover {
  background-color: #0056b3;
}
```

One thing to note is that with buttons, the font-size and font-family are usually inherited from the browser. You can set those if you want to make sure that they are consistent across all browsers.

Let's make sure that the button inherits the font-family and font-size from the body:

```css
input[type='submit'] {
  // ...
  font-family: inherit;
  /* font-size: inherit; */
}
```

I actually prefer the text to be a bit smaller, so I will comment out the font-size line.

Also, notice that the input and textarea placeholder fonts family and size are different. If you look in your devtools and the Elements then Computed tab, you will see the textarea is `monospace` and the inputs are `Arial`. You can change that by setting the font-family and font-size to inherit the body:

```css
input[type='text'],
input[type='email'],
textarea {
  // ...
  font-family: inherit;
  /* font-size: inherit; */
}
```

## `:focus` and Outline

When you click in an input, you will see a blue outline. This is the default focus state. You can remove it by setting the outline to none:

```css
input:focus,
textarea:focus {
  outline: none;
}
```

Or if you want it to be a different color, you can set it to a different color. You can set any other styles that you want when the input is focused:

```css
input:focus,
textarea:focus {
  outline: 2px solid #007bff;
  background: #f4f4f4;
}
```

## `:focus-within`

The `:focus-within` pseudo class is used when any child of the element has focus. This is useful when you have a form and you want to style the form when any of the inputs are focused.

```css
form:focus-within {
  background: #f4f4f4;
  padding: 20px;
}
```

Now when you click in any of the inputs, the form will have a light gray background.

## `::placeholder`

We already looked at the `::placeholder` class, but we can style the placeholder text. It is usually a bit lighter than the input text:

```css
input::placeholder,
textarea::placeholder {
  color: #ccc;
}
```

## `:placeholder-shown`

The `:placeholder-shown` pseudo class is used when the placeholder is shown. This is different than the `::placeholder` pseudo element. The `:placeholder-shown` pseudo class is used to style the entire input when the placeholder is shown and the input is empty.

```css
input:placeholder-shown,
textarea:placeholder-shown {
  height: 50px;
}
```

This will make it so that the input is 50px tall when the placeholder is shown. I'm going to comment it out. I just wanted to show you how it works.

## `:valid` and `:invalid`

The `:valid` and `:invalid` pseudo classes are used to style inputs that are valid or invalid. You can use these to style the inputs when the user enters the correct or incorrect information.

```css
input:invalid,
textarea:invalid {
  border-color: red;
}

input:valid,
textarea:valid {
  border-color: green;
}
```

Enter 'test' in the email input and you will see that the border turns red. Enter 'test@test.com' and you will see that the border turns green.

There are other pseudo classes that you can use to style forms. We already looked at some of them in past lessons. Here is a list:

- `:checked`
- `:disabled`
- `:enabled`
- `:in-range`
- `:out-of-range`
- `:optional`
- `:read-only`
- `:read-write`
- `:required`
