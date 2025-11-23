# Navbar Backgrouns On Scroll

Right now, the navbar is transparent. When the user scrolls down, the navbar should have a background color with a little transparancy and blur. In order to do this, we need to add some JavaScript.

First, let's add the following CSS to the `styles.css` file right before the mobile menu styles:

```css
/* Navbar on scroll style */
.navbar.navbar--scroll {
  background-color: rgba(
    38,
    36,
    49,
    0.8
  ); /* Adjust the alpha (4th value) for transparency */
  backdrop-filter: blur(
    10px
  ); /* Optional: Adds a blur effect to the background */
}
```

We are using the `backdrop-filter` property to add a blur effect to the background. This is optional and may not work in all browsers.

If you manually add the class `navbar--scroll` to the navbar, it will have a transparent background. Now, let's add some JavaScript to add the class when the user scrolls down. Open the `scripts.js` file and add the following code at the very bottom of the file:

```javascript
// Change navbar background color on scroll
window.addEventListener('scroll', function () {
  var navbar = document.querySelector('.navbar');
  if (window.scrollY > 0) {
    navbar.classList.add('navbar--scroll');
  } else {
    navbar.classList.remove('navbar--scroll');
  }
});
```

We are adding a scroll event listener to the window object. When the user scrolls down, we check if the `window.scrollY` value is greater than 0. If it is, we add the `navbar--scroll` class to the navbar. If the user scrolls back to the top, we remove the class.

Now when you scroll, it should transition from a transparent background to a colored background with a blur effect. You can adjust the transparency and blur values in the CSS to get the desired effect.
