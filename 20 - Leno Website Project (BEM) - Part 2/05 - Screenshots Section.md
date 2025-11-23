# Screenshots Section

This is a pretty simple section. It will just be some images in a flex row with a flex wrap.

## HTML

Let's add the HTML:

```html
<!-- Screenshots -->
<section class="screenshots" id="screenshots">
  <div class="screenshots__container container">
    <div class="screenshots__content">
      <h2 class="screenshots__title">Screenshots</h2>
      <div class="screenshots__images">
        <img src="images/screenshot-1.png" alt="Screenshot 1" />

        <img src="images/screenshot-2.png" alt="Screenshot 2" />

        <img src="images/screenshot-3.png" alt="Screenshot 3" />

        <img src="images/screenshot-4.png" alt="Screenshot 4" />

        <img src="images/screenshot-5.png" alt="Screenshot 5" />
      </div>
    </div>
  </div>
</section>
```

## CSS

Now for the CSS:

```css
/* Screenshots */
.screenshots {
  padding: 6rem 2rem;
  background: var(--tertiary-color);
  text-align: center;
}

.screenshots__container {
  max-width: 1200px;
}

.screenshots__title {
  font-size: 2.3rem;
  text-transform: uppercase;
  border-bottom: 2px solid var(--primary-color);
  width: 300px;
  margin: 0 auto 2.5rem;
}

.screenshots__images {
  display: flex;
  justify-content: space-between;
  gap: 1rem;
  flex-wrap: wrap;
}

.screenshots__images img {
  width: 100%;
  max-width: 200px;
  border-radius: 10px;
  margin: 0 auto;
}
```

We are making the width of this section a bit wider (1200px) to accommodate the images. We are also adding a border-bottom to the title to make it stand out a bit more.

The images are set to 100% width and a max-width of 200px. This way they will be responsive and not too big on larger screens.
