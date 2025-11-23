# Download Section

The download section is very similar to the hero/header. It will have a background image with text and buttons on the left and a large image on the right. The image on the right will be a mockup of the app or website that the user can download.

## HTML

Let's add the HTML:

```html
<!-- Download -->
<section class="download" id="download">
  <div class="download__container container">
    <div class="download__content">
      <p class="download__description">
        Download Leno today to see the benefits and enjoy the results faster
        than any other app out there
      </p>
      <div class="download__buttons">
        <a href="details.html" class="download__button button">
          <i class="fa-brands fa-apple"></i>
          For Apple</a
        >
        <a href="details.html" class="download__button button">
          <i class="fa-brands fa-android"></i>
          For Android</a
        >
      </div>
    </div>
    <div class="download__image">
      <img src="images/download.png" alt="Leno App" />
    </div>
  </div>
</section>
```

## CSS

Now for the CSS:

```css
/* Download */
.download {
  padding: 11.5rem 2rem 8rem;
  background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url('../images/download-background.jpg') center center/cover no-repeat;
}

.download__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
}

.download__content {
  max-width: 500px;
}

.download__description {
  margin-top: 1.5rem;
  font-size: 1.5rem;
  line-height: 1.6;
  text-align: center;
}

.download__image img {
  width: 100%;
  max-width: 500px;
}
```

We are using a background gradient and image and using the container to create a flex layout.

#### Download Buttons

We have the main `button` class, which gives us some default styling. I want to add some styles to the button container and the buttons themselves.

```css
.download__buttons {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1.5rem;
  margin-top: 2rem;
}

.download__button {
  padding: 1rem 2rem;
}

.download__button i {
  margin-right: 0.5rem;
}
```

## Responsive Design

Let's make the download section responsive. Add the following to the `992px` media query:

```css
/* Download */
.download {
  padding-top: 10rem;
  text-align: center;
}

.download__container {
  flex-direction: column-reverse;
}

.download__title {
  font-size: 2.3rem;
}

.download .download__buttons {
  flex-direction: column;
  margin-top: 3rem;
}

.download .download__button {
  width: 100%;
}

.download__button {
  padding: 0.7rem;
}
```

The columns will stack and be reversed on smaller screens, and the buttons will be 100% wide and stacked vertically.
