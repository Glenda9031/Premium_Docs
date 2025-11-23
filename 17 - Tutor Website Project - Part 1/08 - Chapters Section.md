# Chapters Section

The chapters section will consist of a section header and a grid of cards with some text and icons. Each card will represent a chapter of the course. We will create a utility class for the cards as we will use them in other sections as well.

## HTML

Let's start by adding the HTML structure for the chapters section. Create a new file called `02 - Chapters Section.html` and add the following code:

```html
<!-- Course Chapters -->
<section class="chapters section" id="chapters">
  <div class="container">
    <div class="section-header">
      <h2>Main Course Chapters</h2>
      <div class="heading-border"></div>
      <p>
        Explore the core concepts and techniques covered in our video course.
        Each chapter is designed to equip you with essential skills for video
        creation.
      </p>
    </div>
    <div class="chapter-cards">
      <div class="card">
        <img src="images/chapters-icon-1.svg" alt="chapter 1" />
        <h3>Setting Clear Objectives</h3>
        <p>
          Learn how to define clear objectives and goals for your video
          projects, ensuring focus and direction
        </p>
      </div>
      <div class="card">
        <img src="images/chapters-icon-2.svg" alt="chapter 2" />
        <h3>Content Creation Strategies</h3>
        <p>
          Dive into effective content creation strategies that resonate with
          your audience
        </p>
      </div>
      <div class="card">
        <img src="images/chapters-icon-3.svg" alt="chapter 3" />
        <h3>Coding Essentials</h3>
        <p>
          Explore the fundamentals of coding for video projects, including HTML,
          CSS, and JavaScript
        </p>
      </div>
    </div>
  </div>
</section>
```

This has a similar format to the learning section. It has a header with a title and subtitle. Below that, we have a grid of cards, each representing a chapter of the course.

Notice that the `section` tag has a class of `section`. This is a utility class that most sections will have just to add some margin to the top and bottom of the section. If you find yourself doing the same thing for multiple sections, you can create a utility class like this. There is also an ID because we will have a link in the navbar that will scroll to this section.

## Card Utility Class

Let's add a class for the cards and the section:

```css
/* Card */
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  background: #fff;
  padding: 2rem 1.75rem 2rem 1.75rem;
  box-shadow: 0 4px 12px 0 rgba(0, 0, 0, 0.1);
}

/* Section */
.section {
  margin: 4rem 0;
}
```

This is a pretty common card layout. We have a white background, some padding, a shadow and centered text. We are also setting the card to be a flex container with the direction set to column.

The `section` class is just adding some margin to the top and bottom of the section.

Let's style the rest of this section:

```css
/* Chapters */
.chapter-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  padding: 2rem 0 4rem;
}

.chapter-cards .card img {
  width: 130px;
  margin-top: 1rem;
}

.chapter-cards .card h3 {
  font-size: 1.25rem;
  font-weight: 700;
  margin: 1rem 0;
}
```

We are using the grid to make a 3-column layout. Each card will have an image, a heading, and a paragraph. The image will have a width of 130px and a margin at the top. The heading will have a font size of 1.25rem and a font weight of 700.

It should look like this:

<img src="../images/tutor-5.png" alt="Chapters Section">

Let's add the following media query class to make the section responsive:

```css
/* Screens less than 992px */
@media screen and (max-width: 992px) {
  /* Other Styles */

  .chapter-cards {
    grid-template-columns: 1fr;
  }
}
```
