# Base CSS & Header Styles

Now that we have the HTML, we can start stying the page. We will start with the base CSS and the header styles. Add the following CSS to your `style.css` file:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Open Sans', sans-serif;
  background: black;
  color: white;
  line-height: 1.6;
}
```

We are setting a reset, applying the Open Sans font, and setting the background to black and the text color to white.

The background of the body is black, but the wrapper will have a background gradient and image. Let's add that next.

```css
.wrapper {
  height: 100%;
  background: linear-gradient(
      to bottom,
      rgba(255, 64, 50, 0.8),
      rgba(71, 17, 116, 0.9)
    ),
    url('../images/background.jpg') no-repeat center center;
  min-height: 100vh;
}
```

The background consists of a linear gradient and an image. The linear gradient is a mix of red and purple, and the image is centered and set to cover the entire background. 

## Header

Now let's style the header:

```css
<!-- Header -->
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px;
}

.header .logo {
  width: 100px;
}

.header .header-right {
  display: flex;
  align-items: center;
  gap: 25px;
}

.header .header-right i {
  margin-right: 5px;
}

.header .header-right a {
  color: #fff;
}

.header .header-right a:hover {
  color: #ff4032;
}
```

We are sizing the logo and adding some space between the logo and the right side of the header. We are using flex for that as well as for the right side of the header.

## Main Content

Let's style the main content:

```css
/* Main Content */
.main-content {
  display: flex;
  gap: 50px;
  max-width: 1100px;
  margin: 200px auto;
  justify-content: center;
  align-items: start;
  height: 100%;
  padding: 0 40px;
}

.main-content form {
  flex: 1;
}

.main-content .text-container {
  flex: 1;
}

```

We are using flex to align the form and the image side by side. We want the 2 items to take up the entire width of the container and be of equal size, so we are setting `flex: 1` for both. This is short for:

```css
flex-grow: 1;
flex-shrink: 1;
flex-basis: 0;
```

It means that the items will grow and shrink to fill the available space.

In the next lesson, we will style the inner content.
