# Inheritance & Specificity

In this lesson, we will learn about inheritance and specificity in CSS.

## Inheritance

Inheritance is a way to apply styles to an element and all of its children. This means that if you set a style on a parent element, all of its children will inherit that style unless they have a style of their own.

We have already used inheritance. For example, when we set the font size on the `body` element, all of the `p` elements on the page inherit that font size. There are some caveats to inheritance, however. Not all properties are inherited for all elements.

Here is another example. If we have the following HTML:

```html
<div class="container">
  <h1>Heading</h1>
  <p>Text</p>
  <h2>Subheading</h2>
  <p>Some other text</p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</div>
```

And the following CSS:

```css
body {
  font-family: Arial, sans-serif;
}

.container {
  color: green;
}
```

All of the text inside the `.container` element will have the font family `Arial` and the color green. Both of these styles are inherited by the children.

Let's add a border to the `.container` element:

```css
.container {
  color: green;
  border: 1px solid black;
}
```

Notice, only the `.container` element has a border. The border is not inherited by the children. If you look up the `border` property in the [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/border#formal_syntax), you will see that it is not inherited. If you look at the `colors` property in the [MDN documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/color#formal_definition), you will see that it is inherited.

Here are some common properties that are not inherited:

- `border`
- `margin`
- `padding`
- `background`
- `height`
- `width`

Here are some common properties that are inherited:

- `color`
- `font-family`
- `font-size`
- `font-weight`
- `line-height`

## Specificity

Specificity is a way to determine which CSS rule is applied to an element when there are multiple rules that could apply. The rule with the highest specificity is the one that is applied.

Specificity is calculated based on the number of selectors, the type of selectors, and the order of the selectors. Here is the order of specificity from lowest to highest:

1. Type selectors and pseudo-elements
2. Class selectors, attributes selectors, and pseudo-classes
3. ID selectors

Using the HTML from the previous example, the `h1` element has a color of green because it inherits the color from the `.container` element. Let's say we want to change the color of the `h1` element to red. We can add the following CSS:

```css
h1 {
  color: red;
}
```

The `h1` element now has a color of red. This is because the `h1` selector has a higher specificity than the `.container` selector. The `h1` selector has a specificity of 1 (type selector) and the `.container` selector has a specificity of 1 (class selector). Since the `h1` selector comes after the `.container` selector in the CSS file, it is applied to the `h1` element.

If we were to add another style:

```css
.container h1 {
  color: blue;
}
```

The `h1` element would have a color of blue. This is because the `.container h1` is more specific than the `h1` selector.

Even if we were to move the `.container h1` selector above the `h1` selector in the CSS file, the `h1` element would still have a color of blue. This is because the `.container h1` selector still has a higher specificity than the `h1` selector.

If I were to remove the `.container` and just have two styles:

```css
h1 {
  color: blue;
}

h1 {
  color: red;
}
```

The `h1` element would have a color of red. This is because the last style in the CSS file is applied when there are conflicting styles.

## !important

The `!important` keyword is used to override all other styles. It is considered bad practice to use `!important` because it can make it difficult to override styles later on. It is better to use specificity to target the elements you want to style. You should still be aware of `!important` and how it works.

Let's add it to the `h1` selector:

```css
h1 {
  color: red !important;
}
```

Now the `h1` element will have a color of red no matter what other styles are applied to it.

Specificity is a powerful tool in CSS. It allows you to target elements with precision and avoid conflicts with other styles. It is important to understand how specificity works so you can use it effectively in your projects.
