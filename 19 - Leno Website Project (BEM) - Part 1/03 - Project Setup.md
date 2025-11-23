# Project Setup

Let's get started with the Leno website. We will create the files, add the assets and add the boilerplate code.

Create a new folder called `leno-website` and inside it create the following folders and files:

```plaintext
leno-website/
├── images/
|── css/
|   └── styles.css
├── js/
|   └── script.js
├── index.html
```

For the images, you can get them from the main repository for the project. I will also include them in the project files for this section. Put them into the images folder.

In your `index.html` file, add the following code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="css/styles.css" />
    <link rel="icon" href="images/favicon.png" />
    <title>Leno App | Health & Productivity</title>
  </head>
  <body>
    <h1>Leno Website</h1>

    <script src="js/script.js"></script>
  </body>
</html>
```

Open the project with Live Server or any other server of your choice. You should see the title "Leno Website" on the page.

## Fonts & Icons

Let's add the fonts and icons to the project. We will use `Open Sans` Google Fonts and Font Awesome for this project.

Add the following link tags to the head of your `index.html` file:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap"
  rel="stylesheet"
/>
```

Now add the Font Awesome link to the head of your `index.html` file:

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
  integrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA=="
  crossorigin="anonymous"
  referrerpolicy="no-referrer"
/>
```

We are using version 6.5.1 of font awesome.

## Base CSS

We will have a little bit of base styling including some custom properties. Let's add the following code to your `styles.css` file:

```css
/* Reset */
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Variables */
:root {
  --primary-color: #08c0dd;
  --secondary-color: #262431;
  --tertiary-color: #2f2c3d;
}

html,
body {
  font-family: 'Open Sans', sans-serif;
  background: var(--secondary-color);
  color: #fff;
  line-height: 1.6;
  scroll-behavior: smooth;
}

a {
  color: #fff;
  text-decoration: none;
}

ul {
  list-style: none;
}
```

We are resetting the margin and padding on all elements and setting the box-sizing to border-box. We are also setting some custom properties for the colors.

We are setting the body/html font-family to Open Sans and setting the background color to the secondary color. We are also setting the color to white and the line-height to 1.6.

I want to have smooth scrolling on the website so I am setting the scroll-behavior to smooth.

In the next lesson, we will start to work on the navbar for the website.
