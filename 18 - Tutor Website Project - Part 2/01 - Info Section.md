# Info Section

This section will have a background image on the left and some text and a list with check icons on the right. We will use a flex container to achieve this layout.

## HTML

Let's start by adding the HTML structure to the `index.html` file:

```html
<!-- Info -->
<section class="info" id="info">
  <div class="info-container">
    <div class="info-left"></div>
    <div class="info-content">
      <h2>Who Is This Course For?</h2>
      <p>
        This course is designed for individuals seeking to enhance their skills
        and knowledge in web design, development, and digital marketing. Whether
        you are a seasoned web designer, a budding web developer or a marketing
        professional looking to expand your skill set.
      </p>
      <ul>
        <li><i class="fas fa-check"></i> Web Designers</li>
        <li><i class="fas fa-check"></i> Web Developers</li>
        <li><i class="fas fa-check"></i> Marketing Professionals</li>
        <li><i class="fas fa-check"></i> Entrepreneurs</li>
        <li><i class="fas fa-check"></i> Business Owners</li>
      </ul>
    </div>
  </div>
</section>
```

The `info` section contains two main elements: `info-left` and `info-content`. The `info-left` element will have a background image, and the `info-content` element contains the text and list.

We are going to add the background image to the `info-container` and then just add 50% spacing on the `info-left` element to create a gap between the image and the text.

## CSS

Let's add the following CSS code to the `style.css` file:

```css
/* Info */
.info-container {
  background: url('../images/audience.jpg') top center/cover no-repeat;
  display: flex;
}

.info-content {
  background-color: var(--primary-color);
  color: white;
  flex: 1;
  padding: 4rem;
}

.info-content h2 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.info-content p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
}

.info-content ul li {
  font-size: 1.2rem;
  line-height: 2;
}

.info-content i {
  margin-right: 0.5rem;
  color: var(--secondary-color);
}

.info-left {
  width: 50%;
}
```

We used `flex-1` to make the `info-content` element take up the remaining space. The rest of the styling is pretty straightforward. We set the background image on the `info-container`, added padding to the `info-content` element, and styled the text and list items.

On small screens, I am going to get rid of the image and just show the text content. Add this to the `768px` media query:

```css
/* Screens less than 768px */
@media screen and (max-width: 768px) {
  /* ...Other styles */

  .info-container {
    flex-direction: column;
  }

  .info-content {
    padding: 2rem;
  }

  .info-content h2 {
    font-size: 1.5rem;
  }

  .info-content p {
    font-size: 1rem;
  }

  .info-left {
    display: none;
  }
}
```

This section should look like this:

<img src="../images/tutor-7.png" />
