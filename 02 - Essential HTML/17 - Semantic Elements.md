# Semantic Elements

With the introduction of HTML5, the concept of semantic markup has become more important than ever. Semantic markup is the use of HTML tags to reinforce the meaning of the information in webpages rather than merely define its appearance. This is important for search engines, screen readers, and other devices that rely on the HTML structure to determine the meaning of the content.

We have used semantic markup already. For instance, the `<h1>` tag is a semantic tag that represents the main heading of a section. The `<p>` tag represents a paragraph of text. The `<a>` tag represents a hyperlink. These tags are semantic because they describe the content they contain. If we used a `<div>` tag instead of a `<p>` tag for a paragraph, it would not be as descriptive. HTML5 introduced a bunch of new semantic tags/elements to make it even easier to write semantic markup.

There are a bunch of these semantic elements. The most common ones are:

- `<header>`: Represents a group of introductory or navigational aids.
- `<nav>`: Represents a section of a page that links to other pages or to parts within the page.
- `<main>`: Represents the main content of the document.
- `<article>`: Represents a self-contained composition in a document, page, application, or site.
- `<section>`: Represents a generic section of a document or application.
- `<aside>`: Represents a portion of a document whose content is only indirectly related to the document's main content.
- `<footer>`: Represents a footer for its nearest sectioning content or sectioning root element.

Let's use our layout example from the last few lessons, where we learned about divs and spans, and convert it to use semantic markup:

Here is the original layout where we used divs and spans:

```html
<!-- Header -->
<div class="header">
  <h1 class="text-xl">My Website</h1>
  <!-- Navigation -->
  <ul class="nav">
    <li><a href="#">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</div>

<!-- Sections -->
<div class="card text-center" id="about">
  <h2 class="text-lg">Section 1</h2>
  <p>
    This is the first paragraph of
    <span class="primary-text">section 1</span>.
  </p>
  <p>
    This is the second paragraph of
    <span class="primary-text">section 1</span>.
  </p>
</div>

<div class="card text-center" id="contact">
  <h2 class="text-lg">Section 2</h2>
  <p>
    This is the first paragraph of
    <span class="secondary-text">section 2</span>.
  </p>
  <p>
    This is the second paragraph of
    <span class="secondary-text">section 2</span>.
  </p>
</div>

<!-- Footer -->
<div class="footer">@copy; 2024 My Website</div>
```

I would change this to use semantic markup:

```html
<header>
  <h1>My Website</h1>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main>
  <section id="about">
    <h2 class="text-lg">Section 1</h2>
    <p>
      This is the first paragraph of
      <span class="primary-text">section 1</span>.
    </p>
    <p>
      This is the second paragraph of
      <span class="primary-text">section 1</span>.
    </p>
  </section>

  <section id="contact">
    <h2 class="text-lg">Section 2</h2>
    <p>
      This is the first paragraph of
      <span class="secondary-text">section 2</span>.
    </p>
    <p>
      This is the second paragraph of
      <span class="secondary-text">section 2</span>.
    </p>
  </section>
</main>

<footer>@copy; 2024 My Website</footer>
```

This is a more semantic way of writing the HTML. It is easier to understand and maintain. It also helps search engines and screen readers understand the content better. We don't need comments and ids to describe the content. The tags themselves are descriptive enough. You could use the tags themselves for styling as well.
