`is()`, `where()` & `has()` Pseudo Classes

We are going to talk about 3 new pseudo classes that were proposed in the CSS Selectors Level 4 specification. These pseudo classes are `:is()`, `:where()`, and `:has()`.

Let's use the following HTML:

```html
<div class="container">
  <h1>Hello World</h1>
  <h2>Lorem, ipsum dolor.</h2>
  <p>
    Lorem, ipsum dolor sit amet consectetur adipisicing
    <a href="#">elit</a>. Tempora, alias.
  </p>

  <h1><span>Goodbye</span> World</h1>
  <p>
    Lorem ipsum dolor sit <a href="#">amet</a> consectetur, adipisicing elit.
    Sint, culpa.
  </p>
</div>
```

## `is()`

The `:is()` pseudo class is a selector that allows you to select an element if it matches any of the selectors inside the parentheses. It is also a new selector, but it is now supported in all of the major modern browsers.

The syntax for the `:is()` pseudo class is as follows:

```css
:is(selector1, selector2, selector3) {
  /* styles */
}
```

Let's say that we want to target the h1, h2 and p elements that are within the container. Before, we had to do this:

```css
.container h1,
.container h2,
.container p {
  color: red;
}
```

Now, we can make it a bit cleaner by using the `:is()` pseudo class:

```css
.container :is(h1, h2, p) {
  font-weight: 600;
}
```

We can even use it for things like link states:

```css
a:is(:hover, :focus) {
  background-color: pink;
}
```

## `:where()`

The `:where()` pseudo class works the same way as the `:is()` pseudo class except it has a lower specificity. In fact, it doesn't have any specificity at all.

The syntax for the `:where()` pseudo class is as follows:

```css
:where(selector1, selector2, selector3) {
  /* styles */
}
```

Let's say that we want to target all of the container headings. We can do this:

```css
.container :where(h1, h2) {
  font-size: 3rem;
}
```

This works and makes all of the headings in the container 3rem. But if we were to do this even before the `:where()` pseudo class:

```css
.container h1,
.container h2 {
  font-size: 2rem;
}
```

It will override the `:where()` pseudo class because it has a higher specificity.

However, if we do this:

```css
.container h1,
.container h2 {
  font-size: 2rem;
  font-weight: bold;
}
```

It will NOT override the font-weight that we set in the `is()` pseudo class because `is()` has a higher specificity. If you change the `is()` to `where()`, it will be overridden.

When I want to target a group of elements in this way, I generally use `:is()` over `:where()` because it has a higher specificity.

## `:has()`

The `:has()` pseudo class is a selector that allows you to select an element based on its children. It is a new selector, but it is now supported in all of the major modern browsers.

`has()` allows us to style an element if any of the things we’re searching for inside it are found. We used to have to use JavaScript to do this, but now we can do it with CSS.

The syntax for the `:has()` pseudo class is as follows:

```css
parent:has(child) {
  /* styles */
}
```

We will use the same HTML that we have been using.

Let's say that we want to target the `h1` element that has a `span` element inside it. We can use the `:has()` pseudo class to do this.

Add the following CSS:

```css
.container:has(h1 span) {
  color: red;
}
```

Or we could do this:

```css
h1:has(span) {
  color: red;
}
```

Either one will work. Now the `h1` element that has a `span` element inside it will have a red color.

So we are not targeting the span like this:

```css
h1 span {
  color: red;
}
```

We are targeting the `h1` element that has a `span` element inside it.

You can even use things like the comparators `>`, `+`, `~`, etc. inside the `:has()` pseudo class.

Let's say we want to target the `h1` that has an adjacent `h2` element. We can do this:

```css
h1:has(+ h2) {
  color: blue;
}
```

Now the first `h1` element will be blue because it has an adjacent `h2` element.
