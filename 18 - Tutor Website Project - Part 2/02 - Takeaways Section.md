# Takeaways Section

The takeaways section will have the standard heading and then a grid layout of cards with icons and text. We will use a CSS Grid here.

## HTML

Let's start by adding the HTML structure to the `index.html` file:

```html
<!-- Takeaways -->
<section class="takeaways section" id="takeaways">
  <div class="container">
    <div class="section-header">
      <h2>Key Takeaways</h2>
      <div class="heading-border"></div>
      <p>
        This section highlights some of the key insights and learnings you'll
        gain from the course. Take a look at what you can expect to achieve:
      </p>
    </div>
    <div class="takeaways-cards">
      <div class="card">
        <i class="fas fa-rocket fa-3x text-primary"></i>
        <p>
          <strong>Enhanced Skills</strong> - Develop advanced skills in web
          design & development
        </p>
      </div>
      <div class="card">
        <i class="fas fa-globe fa-3x text-primary"></i>
        <p>
          <strong>Global Perspective</strong> - Gain insights into industry
          trends and best practices
        </p>
      </div>
      <div class="card">
        <i class="fas fa-cloud fa-3x text-primary"></i>
        <p>
          <strong>Cloud Technology</strong> - Explore the latest cloud
          technologies and tools
        </p>
      </div>
      <div class="card">
        <i class="fas fa-user fa-3x text-primary"></i>
        <p>
          <strong>Networking </strong> - Connect with fellow professionals and
          expand your network
        </p>
      </div>
      <div class="card">
        <i class="fas fa-cog fa-3x text-primary"></i>
        <p>
          <strong>Problem-Solving</strong> - Enhance your problem-solving
          abilities and critical thinking skills
        </p>
      </div>
      <div class="card">
        <i class="fas fa-server fa-3x text-primary"></i>
        <p>
          <strong>Technical Proficiency</strong> - Improve your technical
          proficiency and stay ahead in the digital landscape.
        </p>
      </div>
    </div>
  </div>
</section>
```

## CSS

The section heading as well as the cards will already be styled with our utility classes. Let's add some CSS to style the rest of the section:

```css
/* Takeaways */
.takeaways-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  padding: 1.5rem 0;
}

.takeaways-cards .card {
  flex-direction: row;
  text-align: left;
}

.takeaways-cards .card i {
  margin-right: 1rem;
}
```

We are setting a grid layout for the cards with 3 columns and a gap of `2rem`. We are also adding some padding to the cards for better spacing. The cards will have a row direction and the icon will have a margin to the right for spacing.

I also want to add a couple utility classes for text color. Add the following to the `style.css` file in the utility classes section:

```css
/* Text Colors */
.text-primary {
  color: var(--primary-color);
}

.text-secondary {
  color: var(--secondary-color);
}
```

Now the icons should be colored with the primary color.

## Media Query

I want to stack the cards on screens that are less than `992px`. We already have this style for the chapter cards, so we can reuse it here. Add the following media query to the `style.css` file:

```css
/* Screens less than 992px */
@media screen and (max-width: 992px) {
  .chapter-cards,
  .takeaways-cards {
    grid-template-columns: 1fr;
  }
}
```

Thats it for the takeaways section. You should now have a nicely styled section with key takeaways from the course.

<img src="../images/tutor-8.png" />
