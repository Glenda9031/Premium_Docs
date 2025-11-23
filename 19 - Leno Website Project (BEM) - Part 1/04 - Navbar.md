# Navbar

The navbar is a component that is used to provide navigation to the user. We will have a desktop version as well as a mobile version with a hamburger menu. We will do the basic desktop version first.

## HTML

Let's start by adding the following code to your `index.html` file:

```html
<!-- Navbar -->
<nav class="navbar">
  <div class="navbar__container">
    <div class="navbar__logo">
      <img src="images/logo.svg" alt="Leno App" />
    </div>
    <div class="navbar__menu">
      <ul class="navbar__menu-list">
        <li class="navbar__menu-item">
          <a href="#home" class="navbar__menu-link">Home</a>
        </li>

        <li class="navbar__menu-item">
          <a href="#features" class="navbar__menu-link">Features</a>
        </li>
        <li class="navbar__menu-item">
          <a href="#preview" class="navbar__menu-link">Preview</a>
        </li>
        <li class="navbar__menu-item">
          <a href="#details" class="navbar__menu-link">Details</a>
        </li>
        <li class="navbar__menu-item">
          <a href="#download" class="navbar__menu-link">Download</a>
        </li>
        <li class="navbar__menu-item">
          <a href="#" class="navbar__menu-link navbar__menu-link--primary"
            ><i class="fa-brands fa-facebook"></i
          ></a>
        </li>
        <li class="navbar__menu-item">
          <a href="#" class="navbar__menu-link navbar__menu-link--primary"
            ><i class="fa-brands fa-twitter"></i
          ></a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

Again, we are using the BEM methodology for our class names. We have a `navbar` class for for the main block and then we have all kinds of elements inside it. This project will not have that many modifiers, but we will have a few. As you can see, the `navbar__menu-link--primary` class is a modifier for the primary links.

## CSS

Let's start to add the CSS for this component. Add the following code to your `styles.css` file:

```css
/* Navbar */
.navbar {
  padding: 1rem 2rem;
  background: transparent;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: 1000;
  transition: background-color 0.3s ease-in-out; /* Add transition for background-color */
}
```

We are making the navbar fixed at the top of the page. We are also adding a transition for the background color. This will make the color change smoothly when we scroll the page. We will have to add some JavaScript to make this work. We also set the z-index to 1000 to make sure it is on top of everything.

We are setting the margin to 0 auto to center the container and setting the max-width to 1100px.

#### Navbar Flexbox

I want to use flexbox to align the logo and the menu items. We can use the navbar's container as the flex container. Let's add the following code to your `styles.css` file:

```css
.navbar__container {
  margin: 0 auto;
  max-width: 1100px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

We set a max width and put the content in the middle. We are setting the display to flex and using `justify-content: space-between` to push the logo to the left and the menu items to the right. We are also using `align-items: center` to vertically center the items.

#### Logo

Let's add some styles for the logo:

```css
.navbar__logo img {
  width: 112px;
  height: 36px;
}
```

I chose to wrap the img in a div so we can style it. You could also style the img directly if you prefer.

#### Menu

Let's add some styles for the menu:

```css
.navbar__menu-list {
  display: flex;
  align-items: center;
  gap: 2rem;
  font-weight: 600;
}
```

For hover, we will set the color to the primary color:

```css
.navbar__menu-link:hover {
  color: var(--primary-color);
}
```

I want the social links to have a different color so we will use the `--primary` modifier class:

```css
.navbar__menu-link--primary {
  color: var(--primary-color);
}

.navbar__menu-link--primary:hover {
  color: #fff;
}
```

Now we have our desktop navigation. Let's move on to the mobile navigation.
