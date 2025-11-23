# Hero

Now we will work on the main hero header section.

One thing I want to mention. I added a `.container` utility class on the navbar. Let's move the following styles from `navbar__container` to `container`:

```css
.container {
  max-width: 1100px;
  margin: 0 auto;
}
```

This is preferance, but I am trying to minimize the repetition in our CSS. We will be using a `btn` utility class below as well.

## HTML

Let's add the hero section to the `index.html` file right under the `navbar` section:

```html
<!-- Hero -->
<header class="hero">
  <div class="hero__container container">
    <div class="hero__content">
      <h1 class="hero__title">
        Your
        <span class="hero__title--primary">productivity</span>
        assistant
      </h1>
      <p class="hero__description">
        Boost your productivity and improve your health with Leno - the
        all-in-one app for developers and creators.
      </p>
      <div class="hero__buttons">
        <a href="#download" class="hero__button btn">
          <i class="fa-brands fa-apple"></i>
          For Apple</a
        >
        <a href="#download" class="hero__button btn">
          <i class="fa-brands fa-android"></i>
          For Android</a
        >
      </div>
    </div>
    <div class="hero__image">
      <img src="images/header-smartphones.png" alt="Leno App" />
    </div>
  </div>
</header>
```

The html is pretty simple. It is a container with two divs. The first div contains the content and the second div contains the image.

Obviously this will look like crap because we haven't added any CSS yet. Let's start on that now.

## CSS

We will start by adding the padding and background. The background will be a combination of a gradient and an image. Add the following CSS to the `styles.css` file:

```css
/* Hero */
.hero {
  padding: 11.5rem 2rem 8rem;
  background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url('../images/header-background.jpg') center center/cover no-repeat;
}
```

It should already be contained, because it is inside the `.container` class. We will use the `hero__container` to make it a flexbox. Add the following CSS to the `styles.css` file:

```css
.hero__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
}
```

#### Hero Content

There are some styles I want to add for the content:

```css
.hero__content {
  max-width: 500px;
}

.hero__title {
  font-size: 3.3rem;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 1.2;
}

.hero__title--primary {
  color: var(--primary-color);
}

.hero__description {
  margin-top: 1.5rem;
  font-size: 1.2rem;
  line-height: 1.6;
}

.hero__image img {
  width: 100%;
  max-width: 500px;
}
```

We are restricting the width of the content to 500px. The title is uppercase, bold, and has a larger font size. The primary color is set to the primary color variable. The description has a smaller font size and a line height of 1.6.

We have a modifier for the title text. We will use this to change the color of the word "productivity" to the primary color.

We are also setting the image to be 100% width and a max width of 500px.

#### Hero Buttons

For buttons, I actually want to have a utility class that we can apply anywhere. Let's add the following CSS to the top of the `styles.css` file under the `.container` class:

```css
/* Button Styles */
.btn {
  padding: 0.5rem 2rem;
  background-color: var(--primary-color);
  border: 2px solid transparent;
  color: #fff;
  font-weight: 600;
  border-radius: 50px;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: var(--secondary-color);
  border: 2px solid var(--primary-color);
}
```

Now we can style the hero buttons:

```css
.hero__buttons {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1.5rem;
  margin-top: 2rem;
}

.hero__button {
  padding: 1rem 2rem;
}

.hero__button i {
  margin-right: 0.5rem;
}
```

We are making the buttons flex and centering them. We are adding a gap between the buttons and a margin top of 2rem. The buttons have padding and the icon has a margin right of 0.5rem.

## Responsive Hero

We have some styles to add to the media queries. I actually want a media query for anything below `992px`. So let's add the following above the `768px` media query:

```css
/* Media Queries */
@media (max-width: 992px) {
}
```

We will add the following styles to the `992px` media query:

```css
/* Media Queries */
@media (max-width: 992px) {
  /* Hero */
  .hero {
    padding-top: 10rem;
    text-align: center;
  }

  .hero__container {
    flex-direction: column;
  }

  .hero__title {
    font-size: 2.3rem;
  }

  .hero .hero__buttons {
    flex-direction: column;
    gap: 1rem;

    margin: 2rem auto;
  }

  .hero .hero__buttons {
    flex-direction: column;
    margin-top: 3rem;
  }

  .hero .hero__button {
    width: 100%;
  }
}
```

We changed the direction to column for the container. We also changed the title font size, padding and some other things. It should look like this:

<img src="../images/leno-hero-mobile.png" width="400px" />
