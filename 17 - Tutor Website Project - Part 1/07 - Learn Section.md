# Learn Section

The learn section is pretty simple. We will be using CSS Grid to create a responsive column layout of topics, which will just be images and text.

## HTML

Let's add the following HTML code to the `index.html` file under the hero section:

```html
<!-- Learn -->
<section class="learn">
  <div class="container">
    <div class="section-header">
      <h2>What Will You Learn</h2>
      <div class="heading-border"></div>
      <p>
        Embark on a journey of learning with our comprehensive video courses.
        Discover the secrets of successful video creation and enhance your
        skills.
      </p>
    </div>

    <div class="topics">
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-1.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Set Clear Objectives And Goals</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-2.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Plan Layout And Design Elements</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-3.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Sketch Creative Concepts</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-4.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Establish Strong Call-to-Actions</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-5.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Choose High-Quality HTML Templates</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-6.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Create Impressive Layout Previews</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-7.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Master Landing Page Coding Techniques</h3>
        </div>
      </div>
      <div class="topic">
        <div class="topic-image">
          <img src="images/description-8.jpg" alt="alternative" />
        </div>
        <div class="topic-text">
          <h3>Launch Your Project Successfully Online</h3>
        </div>
      </div>
    </div>
  </div>
</section>
```

We are going to have a utility class called `section-header` that will hold the heading and paragraph of the section. We have a heading with a class of `heading-border` that will be a border under the heading. This is just for decoration purposes. These are utility classes that we will use throughout the project.

Then we have our topics. Each topic will have a `div` element with a class of `topic`. Inside the topic div, we have two children. The first child is a div with a class of `topic-image`. This will hold the image of the topic. The second child is a div with a class of `topic-text`. This will hold the heading of the topic.

## CSS

Let's add the following CSS code to the `style.css` file with the rest of the utility classes:

```css
/* Section Header */
.section-header {
  max-width: 750px;
  margin: 0 auto;
  text-align: center;
  margin-bottom: 3rem;
}

.section-header h2 {
  font-size: 2rem;
  font-weight: 700;
  color: #384653;
  margin-bottom: 0.5rem;
}

.section-header p {
  font-size: 1.2rem;
  color: #384653;
}

.heading-border {
  width: 64px;
  height: 4px;
  background: var(--primary-color);
  margin: 0 auto 2rem;
}
```

We have a utility class called `section-header` that will center the content of the section. The heading will have a font size of 2rem and a font weight of 700. The paragraph will have a font size of 1.2rem. The heading border will have a width of 64px, a height of 4px, and a background color of the primary color.

### Topics Grid

Let's add the following CSS code to the `style.css` file under the hero styling:

```css
/* Learn/Topics */
.topics {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 2rem;
}

.topic {
  overflow: hidden; /* Hide the overflowing image */
}

.topic img {
  width: 100%;
  transition: transform 0.3s;
}

.topic img:hover {
  transform: scale(1.1); /* Scale the image to 110% of its original size */
}

.topic h3 {
  font-size: 1rem;
  font-weight: 700;
  margin: 0.5rem 0;
}
```

We are using a 4-column grid layout for the topics. Each topic will have a width of `100%` and a transition effect of 0.3s. When we hover over the image, it will scale to 110% of its original size without going outside of the container because we set `overflow` to `hidden`. The heading of the topic will have a font size of 1rem and a font weight of 700.

We want to make this responsive by changing the number of columns based on the screen size. Let's add the following CSS in the media queries:

```css
/* Screens less than 1200px */
@media screen and (max-width: 1200px) {
  /* ... rest of the styling */

  .topics {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* Screens less than 992 */
@media screen and (max-width: 992px) {
  /* ... rest of the styling */

  .topics {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Screens less than 576px */
@media screen and (max-width: 576px) {
  /* ... rest of the styling */

  .topics {
    grid-template-columns: repeat(1, 1fr);
  }
}
```

That's it for the learning section.
