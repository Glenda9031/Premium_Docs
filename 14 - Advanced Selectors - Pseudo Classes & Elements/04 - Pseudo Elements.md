# Pseudo Elements

In CSS, we have something called pseudo elements. These are used to style a part of an element using certain keywords. They are prefixed with `::` and are used to style things like the first letter of a paragraph or the first line of a paragraph. There are more intricate pseudo elements like `::before` and `::after` but we'll get to those in a bit. Let's look at some simple ones first.

Let's use the following HTML:

```html
<div class="container">
  <p>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequatur
    cupiditate cum sed corrupti eveniet officiis impedit ducimus reprehenderit
    fuga, id eos quasi maiores itaque voluptate? Ea ut dolorum ipsum quasi?
  </p>

  <form>
    <label for="email">Email</label>
    <input type="email" name="email" id="email" placeholder="Enter Email" />
    <input type="file" name="file" id="file" />
  </form>

  <ul>
    <li>Item One</li>
    <li>Item Two</li>
    <li>Item Three</li>
    <li>Item Four</li>
  </ul>
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
  line-height: 1.6;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  padding: 0 20px;
}

p {
  margin-bottom: 1rem;
}

input {
  width: 100%;
  padding: 5px;
}
```

## The `::first-letter` Selector

The `::first-letter` selector allows us to target the first letter of a block-level element. This is useful when we want to style the first letter of a paragraph or heading.

Let's style the first letter of the paragraph:

```css
p::first-letter {
  font-size: 2rem;
  color: red;
  padding-right: 2px;
}
```

This will make the first letter of the paragraph red, increase the font size, and add some padding to the right.

## The `::first-line` Selector

The `::first-line` selector allows us to target the first line of a block-level element. This is useful when we want to style the first line of a paragraph or heading.

Let's style the first line of the paragraph:

```css
p::first-line {
  font-size: 1.2rem;
  color: blue;
}
```

This will make the first line of the paragraph blue and increase the font size.

## The `::selection` Selector

The `::selection` selector allows us to style the text that is selected by the user. This is useful when we want to style the selected text in a different way.

Let's style the selected text:

```css
p::selection {
  color: red;
  background-color: yellow;
}
```

This will make the selected text red with a yellow background.

## the `:required` Selector

The `:required` selector allows us to style an input field that is required. This is useful when we want to style required fields differently from non-required fields. This is a pseudo-class, not a pseudo-element so it doesn't have the `::` prefix.

Let's style the required input field:

```css
input:required {
  border: 1px solid red;
}
```

This will add a red border to the required input field.

## The `::placeholder` Selector

The `::placeholder` selector allows us to style the placeholder text in an input field. This is useful when we want to style the placeholder text differently from the input text.

Let's style the placeholder text:

```css
input::placeholder {
  color: purple;
  font-weight: bold;
}
```

This will make the placeholder text in the input field purple and bold.

## The `::file-selector-button` Selector

The `::file-selector-button` selector allows us to style the button that opens the file selector dialog in an input field with the type `file`. This used to be a pain in the neck because you couldn't style it with just `button` or `input[type="file"]`. Now you can style it with the `file-selector-button` selector.

Let's style the file selector button:

```css
input::file-selector-button {
  font-weight: bold;
  color: dodgerblue;
  background: #fff;
  padding: 0.5em;
  border: thin solid grey;
  border-radius: 3px;
}
```

This will style the file selector button with a bold font, dodger blue color, white background, some padding, a thin solid grey border, and a border radius of 3px.

## The `::marker` Selector

The `::marker` selector allows us to style the marker/bullet points of a list item. This is useful when we want to style the marker of a list item differently from the list item itself.

Let's style the marker of the list items:

```css
li::marker {
  content: '👉';
  color: red;
}
```

This will change the marker of the list items to a pointing hand emoji and make it red.
