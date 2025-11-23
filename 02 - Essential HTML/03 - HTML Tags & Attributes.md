# HTML Tags & Attributes

HTML tags are the building blocks of web development. They are used to create the structure of a webpage and define its content. Remember, they are not used to style the content or to make things like buttons functional. That's where CSS and JavaScript come in. Tags are for defining the structure and content of a webpage. Tags are often called elements as well, so you may hear me use those terms interchangeably. The tag is the opening and closing part of the element, and the element is the tag and the content inside it.

The standard format of an HTML tag is as follows:

```html
<tagname>content</tagname>
```

You have an opening tag, which is surrounded by angle brackets (`<` and `>`), and a closing tag, which is the same as the opening tag but with a forward slash (`/`) before the tag name. The content goes between the opening and closing tags.

Here is an example of a heading tag and a paragraph tag:

```html
<h1>Some Heading</h1>

<p>This is a paragraph</p>
```

The browser will render the text as a heading and paragraph and it will also add a bit of default styling. The heading will be larger and the heading and paragraph will have some margin.

We will learn about all of the common tags throughout the next couple of sections, but here is a quick summary of some of the most common tags:

- `<html>`: The root element of an HTML page.
- `<head>`: Contains meta-information about the document, such as its title and links to external resources.
- `<title>`: Sets the title of the document, which appears in the browser tab.
- `<body>`: Contains the content of the document, such as text, images, and links.
- `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`: Headings of different sizes, with `<h1>` being the largest and `<h6>` being the smallest.
- `<p>`: Paragraphs of text.
- `<a>`: Links to other pages or resources.
- `<img>`: Images.
- `<ul>`, `<ol>`, `<li>`: Unordered lists, ordered lists, and list items.
- `<table>`, `<tr>`, `<th>`, `<td>`: Tables, table rows, table headers, and table data cells.
- `<div>`, `<span>`: Generic containers for grouping elements.
- `<form>`, `<input>`, `<button>`, `<label>`: Form elements for collecting user input.

These are just a few of the many tags available in HTML. We will cover more tags and their attributes in the upcoming sections.

## Self-Closing Tags

Some tags do not have a closing tag and are called self-closing tags or void elements. These tags are used to insert content that does not require additional content inside them. For example, the `<img>` tag is a self-closing tag because it does not contain any content. Here is an example of a self-closing tag:

```html
<img src="image.jpg" alt="alternative text" />
```

A self-closing tag can end with a forward slash (`/`) before the closing angle bracket (`>`). This is optional in HTML5. The slash is required in XML and XHTML, which is an older reformulation of HTML. In HTML5, most people don't use it, but it's kind of stuck around as a habbit for me so I do tend to use it but you don't have to. 

This tells the browser that the tag does not have a closing tag and should be treated as a self-contained element. Self-closing tags are used for elements like images, line breaks, and input fields.

## HTML Attributes

HTML tags can have attributes that provide additional information about the element. Attributes are added to the opening tag and consist of a name and a value. The format of an attribute is as follows:

```html
<tagname attribute="value">content</tagname>
```

Here is an example of an image tag with attributes:

```html
<img src="image.jpg" alt="alternative text" />
```

The `src` attribute specifies the URL of the image file, and the `alt` attribute provides alternative text for the image. Attributes are used to customize the behavior or appearance of an element. Different tags have different attributes that can be used to modify their behavior.

Another example would be the anchor tag (`<a>`), which is used to create hyperlinks. The `href` attribute specifies the URL that the link points to. Here is an example of an anchor tag with an `href` attribute:

```html
<a href="https://www.google.com">Visit Google</a>
```

We will get much more into these specific tags and elements as we move along.
