# Preview Section

Now we will start the preview section. This will have the main image with an animated play icon in the middle. We will add some CSS and JavaScript to make the video open in a modal when this button is clicked. This section will be broken into three parts. The main layout, the animated button and the modal.

Let's start the basic layout of the preview section. We will add the following HTML:

```html
<!-- Preview -->
<section class="preview" id="preview">
  <div class="preview__container container">
    <div class="preview__content">
      <h2 class="preview__title">Preview</h2>
      <p class="preview__description">
        Take a sneak peek at Leno's sleek and intuitive interface:
      </p>
      <div class="preview__image-container">
        <div class="preview__video-wrapper">
          <img src="images/video-frame.jpg" alt="alternative" />
          <button class="preview__video-button">
            <span class="preview__video-play-button">
              <span></span>
            </span>
          </button>
        </div>
      </div>
    </div>
  </div>
</section>
```

There is nothing showing for the button because we will create the entire thing with CSS including the animation.

Let's add some of the basic CSS for this section:

```css
/* Preview */
.preview {
  background: url('../images/video-background.jpg') center center/cover
    no-repeat;
}

.preview__container {
  padding: 6rem 2rem;
  text-align: center;
}

.preview__title {
  font-size: 2.3rem;
  margin-bottom: 2rem;
  text-transform: uppercase;
}

.preview__description {
  max-width: 600px;
  margin: 1rem auto 4rem;
}

.preview__video-wrapper {
  position: relative;
}

.preview__video-wrapper img {
  width: 100%;
  max-width: 900px;
  border-radius: 10px;
}
```

In the next lesson, we will create the icon/button
