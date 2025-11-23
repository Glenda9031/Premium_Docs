# Child & Sibling Combinators

We are going to look at the child and sibling combinators in CSS.

## Child Combinator

The child combinator is represented by the `>` symbol. It selects only the direct children of an element.

Let's use this HTML as an example:

```html
<div class="container">
  <h1>Welcome</h1>
  <a href="#">Link 1</a>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus,
    quibusdam?
  </p>
  <ul>
    <li>Item One</li>
    <li>Item Two</li>
    <li>
      Item Three
      <ul>
        <li><p>Item Three One</p></li>
        <li><p>Item Three Two</p></li>
        <li><p>Item Three Three</p></li>
      </ul>
    </li>
    <li>Item Four</li>
    <li>Item Five</li>
  </ul>
  <div>
    <p>
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta, suscipit?
    </p>
    <a href="#">Link 2</a>
  </div>
  <a href="#">Link 3</a>
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
  line-height: 2;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  padding: 2rem;
}
```

We have a container with some paragraphs and nested items. If I do the following:

```css
.container p {
  font-weight: bold;
  margin-bottom: 10px;
}
```

It applies to all the paragraphs in the container. But if I want to target only the direct children of the container, I can use the child combinator:

```css
.container > p {
  font-weight: bold;
  margin-bottom: 10px;
}
```

Now only the first paragraph will have bold text and margin.

If I add this:

```css
.container ul {
  list-style: none;
}
```

All of the lists will have no bullets. But if I want to target only the direct unordered list of the container, I can use the child combinator:

```css
.container > ul {
  list-style: none;
}
```

Now only the first list will have no bullets.

## Sibling Combinators

There are a couple different sibling combinators in CSS.

### General Sibling Combinator: `~`

The general sibling combinator is represented by the `~` symbol. It selects all the siblings that come after the element.

Let's say we want all of the links that come after `h1`:

```css
.container h1 ~ a {
  color: green;
}
```

Link 1 and 3 will be green because they come after the `h1` and they are siblings. Link 2 is inside a `div` that is a sibling of the `h1`, but it is not a sibling of the `h1`.

### Adjacent Sibling Combinator: `+`

The adjacent sibling combinator is represented by the `+` symbol. It selects the sibling that comes immediately after the element.

Let's say we want to target the `a` that comes immediately after the `h1`:

```css
.container h1 + a {
  color: purple;
}
```

Now only Link 1 will be purple because it is the only link that comes immediately after the `h1`. If you move the link below the `p`, it will no longer be purple because it is not the immediate sibling of the `h1`.
