# Attribute Selectors

We have gone over the basic selectors and two of the most common are IDs and classes, which have their own selector character (# and .) IDs and classes are attributes, but you can also select elements by other attributes. These are called attribute selectors.

Let's use the following HTML as an example:

```html
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="https://www.traversymedia.com">Traversy Media</a></li>
  </ul>
</nav>
<div class="container">
  <form>
    <div class="form-group">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required />
    </div>
    <div class="form-group">
      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required />
    </div>
    <div class="form-group">
      <label for="message">Message:</label>
      <textarea id="message" name="message" required></textarea>
    </div>
    <div class="form-group">
      <button type="submit">Submit</button>
    </div>
  </form>
</div>
```

And the following CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
}

nav {
  background-color: #007bff;
  color: #fff;
  padding: 10px;
}

ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

li {
  display: inline;
  margin-right: 20px;
}

a {
  color: #fff;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

/* Form Styles */
.container {
  max-width: 400px;
  margin: 20px auto;
  padding: 20px;
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  font-weight: bold;
}

input,
input,
textarea {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #007bff;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
```

This gives us a navbar and a form.

## Input Types

One of the most useful cases for this is with input elements. You can select input elements by their type, name, or value.

We have an email input in our form. Let's say we want to select all email inputs. We can do this by using the following selector:

```css
input[type='email'] {
  border-color: green;
}
```

That selects the input by the type attribute. We can also select by name:

```css
input[name='name'] {
  border-color: blue;
}
```

Let's say we want to select all input elements that are required. We can do this by using the following selector:

```css
input[required] {
  border-color: red;
}
```

## Attribute Value Patterns

You can also select elements by attribute value patterns. For example, let's say we want to select all links that start with `#`. We can do this by using the following selector:

```css
a[href^='#'] {
  color: yellow;
}
```

If we want all links that end with `.com`, we can use the following selector:

```css
a[href$='.com'] {
  color: lightgreen;
}
```

If we want all links that contain `traversy`, we can use the following selector:

```css
a[href*='traversy'] {
  text-decoration: underline;
}
```

Attribute selectors are very useful and can help you style elements based on their attributes. You can select elements by type, name, value, and even patterns.
