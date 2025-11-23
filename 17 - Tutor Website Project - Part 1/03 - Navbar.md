# Navbar

The navbar we are using is pretty standard. I use this on many projects. It is a sticky navbar that will stick to the top of the page when you scroll. It has a logo on the left and links on the right. A hamburger menu will show on small screens with a mobile menu and the navbar has a background color that changes when you scroll. We will need some JS for the mobile menu and the scroll effect, but we will do that a bit later. Let's start with the HTML and CSS for the desktop menu.

## HTML

Here is the HTML for the menu:

```html
<nav class="navbar">
  <div class="navbar-flex container">
    <img src="images/logo.svg" alt="Tutor" />
    <div class="main-menu-items">
      <ul class="main-menu-list">
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
</nav>
```

This is pretty simple. We have a `nav` element with a class of `navbar`. Inside that we have a `div` with two classes, `navbar-flex` and `container`. The reason that I have two classes is because the `container` class is a utility class that we will use in a bunch of places. It is just a class that sets the max-width to 1200px and centers the content. The `navbar-flex` class is a class that I will use to style the navbar and add flexbox. 

## Container Class

Let's add the following CSS to your `styles.css` file:

```css
/* Utility Classes */

/* Container */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.container-sm {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 2rem;
}
```

This is the container class that I was talking about. We are going to have an area at the top of the file for utility classes. These are classes that we will use in multiple places. The container class sets the max-width to 1200px, centers the content and adds some padding to the left and right. We will also have a container-sm class that will set the max-width to 1000px. We will use this on some sections that we want to be a little smaller.

## Navbar CSS

Let's add the following CSS to your `styles.css` file:

```css
/* Navbar */
/* Navbar */
.navbar {
  padding: 1rem 2rem;
  background: black /* temporary */;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: 1000;
  transition: background-color 0.3s ease-in-out;
}

.navbar .navbar-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar img {
  width: 81px;
  height: 32px;
}

.navbar .main-menu-list {
  display: flex;
  align-items: center;
  gap: 2rem;
  font-weight: 600;
}

.navbar a {
  color: #fff;
}

.navbar a:hover {
  color: var(--secondary-color);
}

.navbar i {
  font-size: 1.5rem;
}
```

We set the background of the navbar to black temporarily so we can see it. We will change this to a transparent color later. We set the padding to 1rem on the top and bottom and 2rem on the left and right. We set the position to fixed and the top, right, and left to 0. This will make the navbar stick to the top of the page. We set the z-index to 1000 so it will be on top of everything else. We set the transition to background-color 0.3s ease-in-out so the background color will change smoothly when we scroll.

We set the display to flex on the `navbar-flex` class so we can align the logo and the menu items. We set the width and height of the logo to 81px and 32px. We set the display to flex on the `main-menu-list` class so we can align the menu items. We set the gap to 2rem so there is some space between the menu items. We set the font-weight to 600 on the menu items. We set the color to white on the links and the font-size to 1.5rem on the icons.

That's it for the desktop menu. We will add the mobile menu in the next section.
