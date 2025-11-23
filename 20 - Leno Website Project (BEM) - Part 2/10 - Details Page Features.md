# Details Page Features

We are going to put some features with text and icons in the details page.

## HTML

Let's add the html for the features on the inner details page:

```html
<!-- Details Features -->
<section class="details-features">
  <div class="details-features__container container">
    <h2 class="details-features__title">Features</h2>
    <div class="details-features__list">
      <div class="details-features__list-item">
        <i class="fas fa-rocket fa-4x"></i>
        <div class="details-features__list-text">
          <h3 class="details-features__list-title">Real-Time Data</h3>
          <p class="details-features__list-description">
            Access real-time data instantly, ensuring you're always up-to-date
            with the latest information. Whether it's market trends, user
            activity, or system performance metrics, stay informed with our
            real-time data solutions.
          </p>
        </div>
      </div>
      <div class="details-features__list-item">
        <i class="fas fa-user fa-4x"></i>
        <div class="details-features__list-text">
          <h3 class="details-features__list-title">Simple Integration</h3>
          <p class="details-features__list-description">
            Integrate our solutions seamlessly into your existing workflow with
            minimal effort. Our easy-to-use APIs and intuitive documentation
            make integration a breeze, allowing you to focus on what matters
            most - delivering value to your users.
          </p>
        </div>
      </div>
      <div class="details-features__list-item">
        <i class="fas fa-code fa-4x"></i>
        <div class="details-features__list-text">
          <h3 class="details-features__list-title">Easy To Use</h3>
          <p class="details-features__list-description">
            Experience unparalleled ease of use with our user-friendly interface
            and intuitive features. From beginners to experts, our platform is
            designed to cater to all skill levels, ensuring a smooth and
            hassle-free experience for everyone.
          </p>
        </div>
      </div>
      <div class="details-features__list-item">
        <i class="fas fa-compass fa-4x"></i>
        <div class="details-features__list-text">
          <h3 class="details-features__list-title">High Accuracy</h3>
          <p class="details-features__list-description">
            Rely on our high-precision algorithms and robust data processing
            techniques to deliver accurate insights every time. With our
            advanced technology and rigorous validation processes, you can trust
            that your data is always reliable and precise.
          </p>
        </div>
      </div>
      <div class="details-features__list-item">
        <i class="fas fa-chart-pie fa-4x"></i>
        <div class="details-features__list-text">
          <h3 class="details-features__list-title">Reporting Tools</h3>
          <p class="details-features__list-description">
            Empower your team with powerful reporting tools that provide
            actionable insights and in-depth analysis. From customizable
            dashboards to comprehensive reports, our reporting tools make it
            easy to track performance, identify trends, and make informed
            decisions.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
```

Each feature has an icon, title, and description. We are using Font Awesome icons for the icons.

## CSS

Let's add the css for the features on the inner details page:

```css
/* Details Features */
.details-features {
  padding: 4rem 2rem;
  background: var(--tertiary-color);
}

.details-features__title {
  font-size: 2.3rem;
  margin-bottom: 2rem;
  text-transform: uppercase;
  text-align: center;
}

.details-features__list-item {
  display: flex;
  gap: 1.5rem;
  align-items: center;
  margin-bottom: 3.5rem;
  background: rgba(255, 255, 255, 0.1);
  padding: 1.5rem;
  border-radius: 20px;
}

.details-features__list-item i {
  color: var(--primary-color);
}

.details-features__list-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}
```

I think this is a good way to show the features on the details page. It's clear and easy to read. The icons add visual interest and help to quickly convey the key points of each feature. The styling is consistent with the rest of the website, maintaining a cohesive design throughout. Overall, I'm happy with how this section and the website itself turned out.
