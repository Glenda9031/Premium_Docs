# Divs & Spans

## Divs

`<div>` is a block-level element that is used to group together other elements. It is used to create sections in a document. It is a container that divides the content into sections.

```html
<div>
  <h1>Heading</h1>
  <p>Paragraph</p>
</div>
```

## Spans

`<span>` is an inline element that is used to apply styles to a specific part of the text. It is used to group inline elements together. It is a container that divides the content into smaller parts.

```html
<p>This is a <span>red</span> text.</p>
```

I can put a span around the word "red" to apply a specific style to it. It will not put the word on a new line like a div would because it is an inline element.

The `<div>` and `<span>` elements do not have any semantic meaning. They are used to group elements together for styling purposes.

Here is a super simple layout using divs and spans:

```html
<!-- Header -->
<div>
  <h1>My Website</h1>
  <!-- Navigation -->
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Contact</a></li>
  </ul>
</div>

<!-- Sections -->
<div>
  <h2>Section 1</h2>
  <p>This is the first paragraph of <span>section 1</span>.</p>
  <p>This is the second paragraph of <span>section 1</span>.</p>
</div>

<div>
  <h2>Section 2</h2>
  <p>This is the first paragraph of <span>section 2</span>.</p>
  <p>This is the second paragraph of<span>section 2</span>.</p>
</div>

<!-- Footer -->
<div>@copy; 2024 My Website</div>
```

In this example, I have used divs to group the header, navigation, sections, and footer. I have used spans to apply styles to specific parts of the text. There are really two purposes for doing this. One is for styling and the other is for structure. In reality, there are two things I would do to make this better. I would use semantic HTML elements like `<header>`, `<nav>`, `<section>`, and `<footer>`. I would also use classes and IDs to target specific elements for styling. In the next lesson, we will look at classes and ids.
