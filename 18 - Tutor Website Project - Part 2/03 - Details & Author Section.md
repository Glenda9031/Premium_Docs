# Details & Author Section

The details and author sections will be styled the same with an image on one side and content on the other except the image and content will be swapped.

## HTML

Let's add the HTML for both sections:

```html
<!-- Course Details -->
<section class="details section" id="details">
  <div class="details-flex container">
    <img src="images/details.png" alt="" />
    <div class="details-content">
      <h2>Course Details</h2>
      <div class="heading-border"></div>
      <p>
        Gain insight into the course curriculum, structure, and what to expect
        throughout your learning journey.
      </p>
      <a href="#" class="btn">See Details</a>
    </div>
  </div>
</section>

<!-- Author Information -->
<section class="details section" id="author">
  <div class="details-flex container">
    <img src="images/author.png" alt="" />
    <div class="details-content">
      <h2>Author Information</h2>
      <div class="heading-border"></div>
      <p>
        Learn about the author's background, expertise, and contributions to the
        course content.
      </p>
      <ul>
        <li>
          <i class="fas fa-chevron-circle-right text-primary"></i
          ><strong>Expertise:</strong> Curabitur facilisis lectus varius at
          viverra.
        </li>
        <li>
          <i class="fas fa-chevron-circle-right text-primary"></i
          ><strong>Experience:</strong> Blandit turpis a est eget augue ornare.
        </li>
        <li>
          <i class="fas fa-chevron-circle-right text-primary"></i
          ><strong>Skills:</strong> Sed vulputate aliquet eget non velit.
        </li>
      </ul>
      <a href="#" class="btn">See Details</a>
    </div>
  </div>
</section>
```

This is pretty straightforward. We have a container with an image and content. We are using the `details` class for both sections. The content includes a heading, paragraph, and a button. We are using the `heading-border` class to create a border under the heading. In the CSS, we want to align the border to the left instead of centering it.

## CSS

Let's add the CSS for the details and author sections:

```css
/* Details */
.details-flex {
  display: flex;
  gap: 4rem;
  align-items: center;
  justify-content: center;
}

.details img {
  width: 100%;
  max-width: 500px;
}

.details h2 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.details .heading-border {
  margin: 0; /* Align border to left */
}

.details p {
  margin: 1rem 0 2rem;
}

/* Author */
.details + .details .details-flex {
  flex-direction: row-reverse;
}

.details ul {
  margin-bottom: 2rem;
}

.details ul li {
  line-height: 2;
}

.details i {
  margin-right: 0.5rem;
}
```

We are using flexbox for the alignment. For the `heading-border` class, I set the margin to `0` to align it to the left. For the author section, I am using the adjacent sibling combinator `+` to target the second `.details` class and reverse the direction of the flex container. I also added some spacing to the list items and icons.

## Media Queries

Add the following for the `992px` media query:

```css
/* Screens less than 992px */
@media screen and (max-width: 992px) {
  /* ...Other styles */

  .details-flex {
    flex-direction: column;
    gap: 2rem;
  }

  .details-content {
    text-align: center;
  }

  .details .heading-border {
    margin: 0 auto; /* Align border to center */
  }

  .details + .details .details-flex {
    flex-direction: column;
  }
}
```

We are changing the flex direction to `column` for screens less than `992px`. We are also centering the content and border for the details section. For the author section, we are stacking the image and content on top of each other.

Then on really small screens, I just want to align the `ul` to the left. Add the following media query:

```css
/* Screens less than 576 */
@media screen and (max-width: 576px) {
  /* ...Other styles */

  .details ul {
    text-align: left;
  }
}
```

The section should look like this:

<img src="../images/tutor-9.png" />
