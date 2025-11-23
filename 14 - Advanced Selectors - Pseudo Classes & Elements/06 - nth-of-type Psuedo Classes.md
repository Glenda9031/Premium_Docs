# nth-of-type Pseudo Classes/Selectors

The `nth-of-type` pseudo class is used to select elements based on their position in a group of siblings. It is a powerful selector that can be used to target specific elements in a group. We can do a lot of the same things with `nth-of-type` that we can do with `nth-child`, but it is a bit more flexible.

Let's use the same basic unordered list as the last section. You can use emmet and type `ul>li{Item $}*20` to generate a list with 20 items.:

```html
<div class="container">
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
    <li>Item 5</li>
    <li>Item 6</li>
    <li>Item 7</li>
    <li>Item 8</li>
    <li>Item 9</li>
    <li>Item 10</li>
    <li>Item 11</li>
    <li>Item 12</li>
    <li>Item 13</li>
    <li>Item 14</li>
    <li>Item 15</li>
    <li>Item 16</li>
    <li>Item 17</li>
    <li>Item 18</li>
    <li>Item 19</li>
    <li>Item 20</li>
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
}

li {
  list-style: none;
  padding: 10px;
}

.container {
  max-width: 600px;
  margin: 30px auto;
}
```

## first-of-type

We can target the first element in the list by using `first-of-type`:

```css
li:first-of-type {
  font-weight: bold;
}
```

This will make the first element in the list bold.

## last-of-type

We can target the last element in the list by using `last-of-type`:

```css
li:last-of-type {
  font-weight: bold;
}
```

This will make the last element in the list bold.

## nth-of-type

Targeting a certain element is simple. We just add the number of the element we want to target inside the parentheses. For example, if we want to target the 3rd element, we would use `nth-of-type(3)`. Let's do the 3rd and 6th elements:

```css
li:nth-of-type(3) {
  background-color: lightblue;
}

li:nth-of-type(6) {
  background-color: yellow;
}
```

We can also do even and odd:

```css
li:nth-of-type(even) {
  background-color: lightcoral;
}

li:nth-of-type(odd) {
  background-color: lightgreen;
}
```

And we can also use formulas:

```css
li:nth-of-type(4n) {
  background-color: pink;
}
```

We can also target a range of elements. For example, if we want to target the 3rd through the 6th elements, we would use `nth-of-type(3n+3)`:

```css
li:nth-of-type(3n + 3) {
  background-color: lightpurple;
}
```

## The Difference Between nth-of-type and nth-child

The difference between `nth-of-type` and `nth-child` is that `nth-of-type` selects elements based on their type, while `nth-child` selects elements based on their position in the parent element. This means that `nth-of-type` will only select elements of the specified type, while `nth-child` will select any element that matches the specified position.

Example:

Let's add this HTML below the unordered list:

```html
<div>
  <p>Hello</p>
  <p>World</p>
</div>
```

And this CSS:

```css
p:nth-of-type(2) {
  color: red;
}

p:nth-child(2) {
  font-weight: bold;
}
```

The second paragraph is red and bold. However, if we add an `h1` element above the `p` elements:

```html
<div>
  <h1>Heading</h1>
  <p>Hello</p>
  <p>World</p>
</div>
```

Now the `p` element with "Hello" is bold instead. This is because `nth-child` is selecting the second child of the parent element, which is the `p` element with "Hello". `nth-of-type` is selecting the second `p` element, which is the `p` element with "World". So "World" is still red.

It's up to you on which you want to use. I prefer to use `nth-of-type` because it is more specific and I know exactly what I am targeting.
