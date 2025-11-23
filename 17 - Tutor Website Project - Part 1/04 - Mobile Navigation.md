# Mobile Navigation

We have our navbar working and looking good on desktop, but it's not very mobile friendly. We need to make it so that when the screen is small, the navbar collapses into a hamburger menu.

## HTML

Let's add the following HTML to our `index.html` file. We want to put this after the closing `</div>` after the closing `</ul>` of the desktop menu.

```html
<!-- Mobile Menu -->
<div class="mobile-menu">
  <!-- Hamburger button -->
  <div class="mobile-menu-toggle">
    <i class="fas fa-bars fa-2x"></i>
  </div>
  <!-- Mobile menu items -->
  <div class="mobile-menu-items">
    <ul class="mobile-menu-list">
      <li>
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#chapters">Chapters</a>
      </li>
      <li>
        <a href="#summary">Summary</a>
      </li>
      <li>
        <a href="#takeaways">Takeaways</a>
      </li>
      <li>
        <a href="#author">Author</a>
      </li>
      <li>
        <a href="contact.html">Contact</a>
      </li>
      <li>
        <a href="#"><i class="fa-brands fa-facebook"></i></a>
      </li>
      <li>
        <a href="#"><i class="fa-brands fa-twitter"></i></a>
      </li>
    </ul>
  </div>
</div>
```

It is going to show 2 menus now, which is not what we want. We will hide the mobile menu by default and show it only when the user clicks on the hamburger button. However, we need to first style the mobile menu.

Let's add the following CSS:

```css
/* Mobile Menu */
.navbar .mobile-menu {
  display: none;
}

.navbar .mobile-menu-toggle {
  color: #fff;
  cursor: pointer;
}

.navbar .mobile-menu-items {
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.8);
  opacity: 0.95;
  padding: 3rem 2rem;
  text-align: center;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.navbar .mobile-menu-list {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  font-size: 1.2rem;
}
```

We have the `.mobile-menu` class set to `display: none;` to hide the mobile menu by default. Let's add the following CSS in the `768px` media query:

```css
/* Screens less than 768px */
@media screen and (max-width: 768px) {
  .navbar .main-menu-items {
    display: none; /* Hide the desktop menu on small screens */
  }

  .navbar .mobile-menu {
    display: block; /* Show the mobile menu on small screens */
  }

  .navbar .mobile-menu-toggle {
    display: block;
    padding: 10px;
  }
}
```

This will make it so that the desktop menu is hidden on screens less than `768px` and the mobile menu is shown.

The rest of the CSS is just styling the mobile menu items and is pretty self-explanatory.

It should look like this on smaller screens:

<img src="../images/tutor-13.png" width="400" />

### Hide Mobile Menu items

Let's hide the mobile menu items. We are going to do this by moving them off of the page using the `transform` property. Add the following CSS to the `styles.css` file:

```css
.navbar .mobile-menu-items {
  position: absolute;
  transform: translatex(100%);
  /* ...rest of the styles */
}
```

We set the `transform` property to `translatex(100%);` to move the mobile menu items off of the page. This will push the mobile menu items to the right of the screen and hide them from view.

### `active` Class

We want to move them back into view when the `active` class is applied. Add the following CSS:

```css
.navbar .mobile-menu-items.active {
  transform: translatex(0); /* Show the mobile menu items */
}
```

This will move the mobile menu items back into view when the `active` class is applied. You can manually apply it to the `.mobile-menu-items` class in the HTML if you want to test it.

### JavaScript

Now, let's add some JavaScript to show and hide the mobile menu when the user clicks on the hamburger button. All we are going to do in the JS is apply the class of `active` to the mobile menu when the user clicks on the hamburger button.

Open the `scripts.js` file and add the following JavaScript:

```js
document.addEventListener('DOMContentLoaded', function () {
  // Get hamburger button and mobile menu items
  const toggleButton = document.querySelector('.navbar .mobile-menu-toggle');
  const mobileMenu = document.querySelector('.navbar .mobile-menu-items');

  // Add click event listener to toggle mobile menu visibility
  toggleButton.addEventListener('click', function () {
    mobileMenu.classList.toggle('active');
  });
});
```

We are simply adding an event listener to the hamburger button and toggling the `active` class on the mobile menu items when the user clicks on the hamburger button.

Now when you click on the hamburger menu, the mobile menu should slide in from the right.

That's it! We now have a responsive navbar that collapses into a hamburger menu on smaller screens.
