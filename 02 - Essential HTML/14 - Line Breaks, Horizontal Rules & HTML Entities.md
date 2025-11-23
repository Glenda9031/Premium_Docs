# Line Breaks, Horizontal Rules & HTML Entities

In this lesson, we will learn about line breaks, horizontal rules, and HTML entities. We will also look at the `<pre>` tag, which is used to display preformatted text as well as the `<code>` tag, which is used to display code snippets.

## Line Breaks

A line break is used to create a new line in the text. In HTML, you can use the `<br>` tag to create a line break. The `<br>` tag is an empty tag, which means it does not have a closing tag. Here is an example of how to use the `<br>` tag:

```html
<p>This is the first line<br />This is the second line.</p>
```

Again, just like with the `<img>`, `<br>`, and `<hr>` tags, the slash in the closing tag is optional. It is not required in HTML5, but you can include it if you prefer.

One thing to mention is that you should not be using the `<br>` tag to create space between elements. Instead, you should use CSS to control the spacing between elements. The `<br>` tag should only be used to create line breaks within text. Keep the rule in your head that HTML is for content and structure, while CSS is for presentation and styling.

## Horizontal Rules

A horizontal rule is used to create a horizontal line on the page. In HTML, you can use the `<hr>` tag to create a horizontal rule. The `<hr>` tag is an empty tag, which means it does not have a closing tag. Here is an example of how to use the `<hr>` tag:

```html
<p>This is the first paragraph.</p>
<hr />
<p>This is the second paragraph.</p>
```

The `<hr>` tag is a self-closing tag, so you do not need to include a closing tag. The `<hr>` tag creates a horizontal line that spans the width of the containing element. You can use CSS to style the horizontal rule, such as changing the color, width, and height.

## HTML Entities

HTML entities are special characters that have a specific meaning in HTML. For example, the `&lt;` entity represents the less-than sign `<`, and the `&gt;` entity represents the greater-than sign `>`. These entities are used to display characters that have special meaning in HTML, such as `<`, `>`, `&`, and `"`.

The reason you may use these entities is that some characters have special meaning in HTML, such as the less-than sign `<`, which is used to start an HTML tag. If you want to display the less-than sign as text on the page, you need to use the `&lt;` entity.

## `<code>` Tag

Let's say that you want to show some code on your website. You can use the `<code>` tag to wrap the code and the `&lt;` and `&gt;` entities to display the less-than and greater-than signs. Here is an example:

```html
<p>
  This is an example of a code snippet:
  <code>&lt;p&gt;This is a paragraph&lt;/p&gt;</code>
</p>
```

The content inside a `<code>` element is typically displayed in a monospace font (e.g., Courier New, Consolas) to differentiate it from regular text.

	Here are some common codes for entities:

```
	- &gt; for >
    - &lt; for <
    - &amp; for &
    - &quot; for "
    - &apos; for '
    - &nbsp; for Non-breaking space
    - &copy; for ©
    - &reg; for ®
    - &trade; for ™
    - &deg; for °
```

## `<pre>` Tag

The `<pre>` tag is used to display preformatted text. This means that the text inside the `<pre>` tag is displayed exactly as it is written in the HTML file, including spaces, line breaks, and tabs. The `<pre>` tag is useful for displaying code snippets or text that needs to maintain its formatting.

Here is an example of how to use the `<pre>` tag:

```html
<pre>
  This is some preformatted text.
  It will be displayed exactly as it is written here.
</pre>
```

Even if I space one of the paragraphs over, it will be displayed exactly as it is written in the HTML file.
