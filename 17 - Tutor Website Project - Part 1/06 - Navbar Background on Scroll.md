# Navbar Background On Scroll

We want to have a transparent background for the navbar, but have a solid background when scrolling. We will need to add a bit of JavaScript to achieve this.

We can now change the background of the `.navbar` class from `black` to `transparent`:

```css
.navbar {
  /* ... rest of styles */
  background: transparent;
}
```

Also, add the following CSS:

```css
/* Navbar on scroll style */
.navbar.navbar-scroll {
  background-color: rgba(
    235,
    77,
    85,
    0.8
  ); /* Adjusted RGBA values for a darker color */
  backdrop-filter: blur(
    10px
  ); /* Optional: Adds a blur effect to the background */
}
```

We are setting the background color to a darker shade of red with an alpha value of `0.8`. This will make the background slightly transparent. We are also adding a `backdrop-filter` property with a `blur` value of `10px`. This will add a blur effect to the background.

### JavaScript

Now we need to add some JavaScript to change the background of the navbar when scrolling. Add the following code to the `script.js` file:

```js
// Change navbar background color on scroll
window.addEventListener('scroll', function () {
  var navbar = document.querySelector('.navbar');
  if (window.scrollY > 0) {
    navbar.classList.add('navbar-scroll');
  } else {
    navbar.classList.remove('navbar-scroll');
  }
});
```

Now when you scroll, you should see the background of the navbar change from transparent to a solid color.
