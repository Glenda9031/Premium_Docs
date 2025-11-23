# Project Setup

We are going to start our project. We will create a new project folder and set up the project structure. Create a folder called `lumina-creative` in your `projects` folder. Inside the `lumina-creative` folder, create the following folders and files:

```bash
lumina-creative
├── css
│   └── styles.css
├── images
├── index.html
├── about.html
└── contact.html
```

## Images

Get the images from the `images` folder download for this section. You can also get them from the main repository.

## HTML

Open the `index.html` file and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Lumina Creative</title>
    <link rel="stylesheet" href="css/styles.css" />
    <link rel="icon" href="images/favicon.ico" />
  </head>
  <body>
    <h1>Lumnina Creative</h1>
  </body>
</html>
```

## Fonts

We are going to use the `Open Sans` font from Google Fonts. Add the following code to the `head` tag in the `index.html` file:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap"
  rel="stylesheet"
/>
```

## Icons

We are going to include the `Font Awesome` icons. Add the following code to the `head` tag in the `index.html` file:

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.4/css/lightbox.css"
  integrity="sha512-Woz+DqWYJ51bpVk5Fv0yES/edIMXjj3Ynda+KWTIkGoynAMHrqTcDUQltbipuiaD5ymEo9520lyoVOo9jCQOCA=="
  crossorigin="anonymous"
  referrerpolicy="no-referrer"
/>
```

## Base CSS

In the `styles.css` file, add the following code:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body {
  font-family: 'Open Sans', sans-serif;
  line-height: 1.6;
}

a {
  text-decoration: none;
  color: #333;
}

ul {
  list-style: none;
}

img {
  width: 100%;
}
```

We are just adding a reset and setting the base font family and line height. We are also setting the default styles for links, lists, and images.

Now we are ready to start building our website. In the next section, we will create the header and navigation for our website.
