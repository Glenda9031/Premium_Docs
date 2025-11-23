# HTML Document Structure

Right now, we just have an `<h1>` tag in our `index.html` file. This is not a complete HTML document. You need to include a few essential elements to create a valid HTML document.

- `<!DOCTYPE html>`: This declaration tells the browser that the document is an HTML5 document. There are other versions of HTML, but HTML5 is the latest and most widely used version. The `<!DOCTYPE html>` declaration should be the first line of your HTML document.
- `<html>`: The root element of an HTML page.
- `<head>`: Contains meta-information about the document, such as its title and links to external resources. This information is not displayed on the page itself.
- `<title>`: Sets the title of the document, which appears in the browser tab.
- `<body>`: Contains the content of the document, such as text, images, and links.

Let's create a basic HTML document structure by adding these elements to the `index.html` file:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Web Page</title>
  </head>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

This is the standard structure of an HTML document. The `<!DOCTYPE html>` declaration tells the browser that the document is an HTML5 document. The `<html>` element is the root element of the document, and it contains the `<head>` and `<body>` elements. You should see the title "My First Website" in the browser tab and the heading "Hello World!" displayed on the page.

## Indentation

You may have noticed that the elements inside the `<html>`, `<head>`, and `<body>` tags are indented. Indentation is not required for HTML to work, but it is a good practice to make your code more readable. Indentation helps you see the structure of your document and understand how elements are nested within each other.

There is a hierarchy in HTML elements, and indentation helps you visualize this hierarchy. It is common to use two or four spaces for indentation, but you can choose any number of spaces or tabs that you prefer. Consistent indentation makes your code easier to read and maintain.

## Prettier

If you are using Visual Studio Code, you can install an extension called Prettier to automatically format your code. Prettier will take care of indentation, line breaks, and other formatting rules for you. This can save you time and ensure that your code is consistently formatted. You can set it to format on save by going to the settings and enabling the "Format On Save" option. This way, if you have something out of place, Prettier will fix it for you automatically. It's also nice because we will always have the same formatting throughout the project.

## Comments

You can also add comments to your code. Comments are used to explain your code and are not displayed in the browser. You can add comments in HTML using the following syntax:

```html
<!-- This is a comment -->
```

When I build a large project, I like to add comments to different sections of my code. This helps me understand what each section does and makes it easier to navigate through the code. Comments are also useful when working in a team because they provide context and explanations for other developers.
