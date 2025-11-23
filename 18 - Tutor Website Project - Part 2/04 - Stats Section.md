# Stats Section

The stats section will have a background image with an inline image on the left and some stat numbers, text and button on the right.

## HTML

Let's add the HTML for the stats section:

```html
<!-- Stats -->
<section class="stats section" id="stats">
  <div class="stats-flex container">
    <img src="images/stats.png" alt="" />
    <div class="stats-content">
      <div class="stats-numbers">
        <div>
          <h3>2000+</h3>
          <p>Happy Users</p>
        </div>
        <div>
          <h3>358</h3>
          <p>Issues Solved</p>
        </div>
        <div>
          <h3>980</h3>
          <p>Good Reviews</p>
        </div>
        <div>
          <h3>216</h3>
          <p>Case Studies</p>
        </div>
      </div>
      <p class="stats-text">
        Tutor is probably one of the best video courses on landing page making
        in the web industry
      </p>
      <a href="#" class="btn">Get The Course</a>
    </div>
  </div>
</section>
```

This is a simple section with a container that has an image and content. The content includes a heading, paragraph, and a button. We are using the `stats` class for the section and the `stats-flex` class for the flex container. The `stats-numbers` class is used for the stat numbers and text. The `stats-text` class is used for the paragraph.

## CSS

Let's add the CSS for the stats section:

```css
/* Stats */
.stats {
  background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url(../images/stats-background.jpg) center center/cover no-repeat;
  color: #fff;
}

.stats-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 4rem 2rem;
}

.stats img {
  width: 100%;
  max-width: 500px;
}

.stats-content {
  max-width: 500px;
}

.stats-numbers {
  display: flex;
  gap: 2rem;
  margin: 2rem 0;
  text-align: center;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

.stats-numbers h3 {
  font-size: 3rem;
  font-weight: 700;
}

.stats-numbers p {
  font-size: 0.8rem;
}

.stats-text {
  font-size: 1.2rem;
  margin-bottom: 2rem;
  text-align: center;
}

.stats .btn {
  display: block;
  margin: 0 auto;
  text-align: center;
  width: 200px;
}
```

We are using flexbox to align the main content and for the stat numbers. We set the background image with a linear gradient to make the text more readable. The stat numbers will be centered with a gap of `2rem`. The text will have a font size of 1.2rem and be centered. We added some additional styling to the button to center it.

## Media Queries

I want to stack the flex items into a column on screens that are less than `992px`. Add the following media query to the `style.css` file:

```css
/* Screens less than 992px */
@media screen and (max-width: 992px) {
  /* ...Other styles */

  .stats-flex {
    flex-direction: column;
    gap: 2rem;
  }
}
```

On really small screens, I want the stat numbers themselves to stack into a column. Add the following media query to the `style.css` file:

```css
/* Screens less than 576 */
@media screen and (max-width: 576px) {
  /* ...Other styles */
  .stats-numbers {
    flex-direction: column;
  }
}
```

This section should look like this:

<img src="../images/tutor-10.png" />
