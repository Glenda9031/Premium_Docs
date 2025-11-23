# Testimonials

Each testimonial will have a picture, a name, and some text. We will have three on large screens, two on medium screens, and one on small screens. We could stack them, but I want to try out different things. We will use CSS Grid for this.

## HTML

Add the following HTML to your `index.html` file:

```html
<!-- Testimonials -->
<section class="testimonials" id="testimonials">
  <div class="testimonials__container container">
    <div class="testimonials__card">
      <div class="testimonials__card-image">
        <img src="images/testimonial-1.jpg" alt="Testimonial 1" />
      </div>
      <div class="testimonials__card-content">
        <p class="testimonials__card-text">
          "Leno has truly transformed how I manage my time and health. Highly
          recommended!"
        </p>
        <h3 class="testimonials__card-title">Samantha Samson</h3>
      </div>
    </div>
    <div class="testimonials__card">
      <div class="testimonials__card-image">
        <img src="images/testimonial-2.jpg" alt="Testimonial 2" />
      </div>
      <div class="testimonials__card-content">
        <p class="testimonials__card-text">
          "As a developer, I rely on Leno every day to keep me focused and
          energized. It's a game-changer!"
        </p>
        <h3 class="testimonials__card-title">Mike Johnson</h3>
      </div>
    </div>
    <div class="testimonials__card">
      <div class="testimonials__card-image">
        <img src="images/testimonial-3.jpg" alt="Testimonial 3" />
      </div>
      <div class="testimonials__card-content">
        <p class="testimonials__card-text">
          "With Leno, I've been able to achieve my goals faster and healthier
          than ever before. It's a must-have app!"
        </p>
        <h3 class="testimonials__card-title">Laney Smith</h3>
      </div>
    </div>
  </div>
</section>
```

## CSS

Now let's create a grid using the container:

```css
/* Testimonials */
.testimonials {
  padding: 4rem 2rem;
  text-align: center;
}

.testimonials__container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  align-items: center;
  justify-content: center;
}
```

Then we will style the cards:

```css
.testimonials__card {
  padding: 0 3rem;
}

.testimonials__card-image img {
  width: 96px;
  height: 96px;
  margin-right: auto;
  margin-bottom: 1.5rem;
  margin-left: auto;
  border-radius: 50%;
}

.testimonials__card-text {
  font-style: italic;
  margin-bottom: 1.5rem;
}
```

## Media Queries

Let's make the grid two columns on medium screens and one column on small screens.

In the `@media` rule for `992px`, add the following:

```css
/* Testimonials */
.testimonials__container {
  grid-template-columns: repeat(2, 1fr);
}

.testimonials__card {
  padding: 0 1.5rem;
}

.testimonials__card:nth-child(3) {
  display: none;
}
```

We are using the `:nth-child()` pseudo-class to hide the third card.

In the `@media` rule for `768px`, add the following:

```css
.testimonials__container {
  grid-template-columns: 1fr;
}

.testimonials__card:nth-child(2) {
  display: none;
}
```

We are using the `:nth-child()` pseudo-class to hide the second card.
