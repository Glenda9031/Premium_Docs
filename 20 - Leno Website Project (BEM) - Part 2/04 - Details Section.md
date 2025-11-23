# Details Section

The details section is a grid with two rows and two columns of text and images. The text part will also have a link that will take the user to the details.html page.

## HTML

Let's add the HTML for the details section.

```html
<!-- Details -->
<section class="details" id="details">
  <div class="details__container container">
    <div class="details__grid">
      <!-- Grid Item 1 -->
      <div class="details__grid-image">
        <img src="images/details-1.png" alt="Leno App" />
      </div>
      <!-- Grid Item 2 -->
      <div class="details__grid-content">
        <h3 class="details__grid-heading">
          Start using Leno today and set your long term goals
        </h3>
        <p class="details__grid-description">
          Ac ante ipsum primis in faucibus. Nam et porttitor ipsum. Morbi eros
          augue, blandit in varius gravida tempor a massa. Curabitur ante dolor
          euismod a arcu nec pellentque
        </p>
        <a href="details.html" class="details__grid-button button">More</a>
      </div>

      <!-- Grid Item 3 -->
      <div class="details__grid-content">
        <h3 class="details__grid-heading">
          The calendar feature helps you schedule tasks
        </h3>
        <p class="details__grid-description">
          Ac ante ipsum primis in faucibus. Nam et porttitor ipsum. Morbi eros
          augue, blandit in varius gravida tempor a massa. Curabitur ante dolor
          euismod a arcu nec pellentque
        </p>
        <a href="details.html" class="details__grid-button button">More</a>
      </div>
      <!-- Grid Item 4 -->
      <div class="details__grid-image">
        <img src="images/details-2.png" alt="Leno App" />
      </div>
    </div>

    <!-- Details Icons -->
    <div class="details__icons">
      <div class="details_icons-item">
        <i class="fas fa-users fa-4x"></i>
        <div class="details__icons-amount">55,000</div>
        <h4 class="details__icons-title">Happy Customers</h4>
      </div>
      <div class="details__icons-item">
        <i class="fas fa-code fa-4x"></i>
        <div class="details__icons-amount">585</div>
        <h4 class="details__icons-title">Issues Solved</h4>
      </div>
      <div class="details__icons-item">
        <i class="fas fa-comments fa-4x"></i>
        <div class="details__icons-amount">788</div>
        <h4 class="details__icons-title">Good Reviews</h4>
      </div>
      <div class="details__icons-item">
        <i class="fas fa-rocket fa-4x"></i>
        <div class="details__icons-amount">100</div>
        <h4 class="details__icons-title">Case Studies</h4>
      </div>
      <div class="details__icons-item">
        <i class="fas fa-edit fa-4x"></i>
        <div class="details__icons-amount">110</div>
        <h4 class="details__icons-title">Press Article</h4>
      </div>
    </div>
  </div>
</section>
```

We have a grid with 4 items and then we have some icons with the amount and title.

Let's style the grid first:

```css
.details {
  padding: 9rem 2rem;
}

.details__grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 5rem;
  align-items: center;
  justify-content: center;
}

.details__grid-content {
  max-width: 500px;
  width: 100%;
}

.details__grid-heading {
  font-size: 2rem;
  margin-bottom: 2rem;
  line-height: 1.2;
}

.details__grid-description {
  margin-bottom: 2rem;
  line-height: 1.6;
}
```

Now, the icons:

```css
/* Details Icons */
.details__icons {
  margin-top: 8rem;
  display: flex;
  gap: 2rem;
  justify-content: space-around;
  text-align: center;
}

.details__icons i {
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.details__icons-amount {
  font-size: 3.5rem;
  font-weight: 600;
}

.details__icons-title {
  font-size: 1.3rem;
  font-weight: 400;
}
```

This looks good on desktop but we need to make it responsive. Let's add the following to the `992px` media query:

```css
/* Details */
.details__grid {
  grid-template-columns: 1fr;
  text-align: center;
}

.details__grid-image img {
  max-width: 400px;
  width: 100%;
}

.details__grid-content {
  max-width: 400px;
  width: 100%;
  margin: 0 auto;
}

.details__icons {
  flex-direction: column;
  gap: 2rem;
  margin-top: 4rem;
}
```

This will stack everything on top of each other on smaller screens.
