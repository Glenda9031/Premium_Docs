# Implementing CSS

We are finally getting into the fun part of the course, which is CSS. There is not a whole lot that you can do with just HTML or just CSS for that matter. However, when you combine the two, you can create some amazing things. In this lesson, we will be focusing on how to implement CSS into a web page.

There are three ways to implement CSS into a web page:

1. Inline CSS
2. Internal CSS
3. External CSS

## Inline CSS

Inline CSS is when you add the CSS directly to the HTML element. This is not the best practice, but it is the quickest way to style an element. You can add the `style` attribute to an HTML element and set the CSS properties directly. Here is an example:

```html
<h1 style="color: blue; font-size: 50px; margin-bottom: 0">
  This is a heading.
</h1>
<p style="color: red">This is a paragraph.</p>
```

We will talk about the syntax of CSS in the next lesson but in the example above, we are setting the color of the heading to blue, the font size to 50px, and the margin bottom to 0. We are setting the color of the paragraph to red. As you can imagine, a page with a lot of styling like this would be a nightmare to maintain. You don't really want to do this unless you have a really good reason.

## Internal CSS

Internal CSS is when you add the CSS to the `style` element in the `head` section of the HTML document. This is a step up from inline CSS because you can target multiple elements with the same style. Here is an example:

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>HTML & CSS Sandbox</title>
  <style>
    h1 {
      color: blue;
      font-size: 50px;
      margin-bottom: 0;
    }

    p {
      color: red;
    }
  </style>
</head>

<body>
  <h1>This is a heading.</h1>
  <p>This is a paragraph.</p>
</body>
```

This gives us the same exact result, but our CSS is now in the `head` section of the HTML document. This is a better way to do it because it does add what we call "separation of concerns". However, this is still not the best practice because we are mixing the structure of the document with the presentation in the same file.

## External CSS

External CSS is when you create a separate CSS file and link it to your HTML document. This is the best practice because it separates the structure of the document from the presentation. Here is an example:

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>HTML & CSS Sandbox</title>
  <link rel="stylesheet" href="style.css" />
</head>

<body>
  <h1>This is a heading.</h1>
  <p>This is a paragraph.</p>
</body>
```

In the example above, we are linking an external CSS file called `style.css` to our HTML document. This is the best practice because it separates the structure of the document from the presentation. This makes it easier to maintain and update your styles.
