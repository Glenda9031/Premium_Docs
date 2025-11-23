# Sticky Navbar

In this lesson, we will use the small project from the last lesson and make the navbar sticky. This is a common feature on websites where the navbar stays at the top of the page as you scroll down. I will add a little bit extra and make the navbar a bit transparent when it is not sticky. This will take a bit of JavaScript to accomplish.

All that we have to do to make the navbar sticky is to add the following CSS:

```css
.header {
  position: sticky;
  top: 0;
  z-index: 1000;
}
```

This will make the navbar stick to the top of the page. The `z-index` property is used to make sure the navbar is on top of everything else.

## Transparent on Scroll

Let's make it so the navbar is transparent when it is not sticky. We can do this by adding a class to the navbar when the user scrolls down. We will use JavaScript to accomplish this.

First, add a new class to the CSS file:

```css
.transparent {
  background: linear-gradient(
    45deg,
    rgba(255, 0, 0, 0.8),
    rgba(0, 0, 255, 0.8)
  ); /* Adjust opacity as needed */
}
```

We want to preserve the gradient background, so we are still using the `linear-gradient` function. Otherwise you would just use `background: rgba(0, 0, 0, 0.8);` to make it black with 80% opacity.

## JavaScript

Now we need to add some JavaScript to add the class when the user scrolls down. Create a new file called `main.js` and add the following code and place the `<script>` tag at the bottom of the HTML file above the closing `</body>` tag.

In the JavaScript file:

```js
document.addEventListener('DOMContentLoaded', function () {
  const header = document.querySelector('.header');

  // Function to add/remove transparency class based on scroll position
  function toggleHeaderTransparency() {
    if (window.scrollY > 0) {
      header.classList.add('transparent');
    } else {
      header.classList.remove('transparent');
    }
  }

  // Listen for scroll events and update transparency
  window.addEventListener('scroll', toggleHeaderTransparency);
});
```

We are adding an event listener to the `scroll` event and calling the `toggleHeaderTransparency` function. This function checks the `window.scrollY` property to see how far the user has scrolled. If the user has scrolled down at all, we add the `transparent` class to the header. If the user scrolls back to the top, we remove the class.

## Back To Top Button

Let's also add a button icon that will take the user back to the top of the page when clicked. We will use a Font Awesome icon for this. Include the Font Awesome CSS in the `<head>` of the HTML file:

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
  integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A=="
  crossorigin="anonymous"
  referrerpolicy="no-referrer"
/>
```

Add the following HTML just above the script tag:

```html
<a href="#" class="back-to-top-btn">
  <i class="fas fa-arrow-up"></i>
</a>
```

Now the CSS:

```css
.back-to-top-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  font-size: 20px;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background-color 0.3s;
}

.back-to-top-btn:hover {
  background-color: #0056b3;
}
```

Now you have a button to take you to the top of the page.

You probably noticed that the button is always visible. We can add a class to hide it when the user is at the top of the page. Add the following JavaScript to the `main.js` file:

```js
document.addEventListener('DOMContentLoaded', function () {
  const header = document.querySelector('.header');
  const backToTopButton = document.querySelector('.back-to-top-btn');

  // Function to add/remove transparency class based on scroll position
  function toggleHeaderTransparency() {
    if (window.scrollY > 0) {
      header.classList.add('transparent');
      backToTopButton.style.display = 'flex';
    } else {
      header.classList.remove('transparent');
      backToTopButton.style.display = 'none';
    }
  }

  // Listen for scroll events and update transparency
  window.addEventListener('scroll', toggleHeaderTransparency);
});
```

We simply brought in the button element and added a style to show or hide it based on the scroll position.
