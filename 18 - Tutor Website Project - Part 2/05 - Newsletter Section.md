# Newsletter Section

The newsletter section will have a gray background and will have a heading, paragraph, and a form with an input and button. The form will have a class of `newsletter-form`.

## HTML

Let's add the following code to the `index.html` file:

```html
<!-- Newsletter -->
<section class="newsletter section" id="newsletter">
  <div class="newsletter-flex container">
    <h2>Subscribe To Our Newsletter</h2>
    <p>
      Stay updated with the latest news, offers, and insights from our platform.
      Join our newsletter community today!
    </p>
    <form action="#">
      <input type="email" placeholder="Enter your email" />
      <button type="submit" class="btn">Subscribe</button>
    </form>
  </div>
</section>
```

## CSS

Let's add the CSS for the newsletter section:

```css
/* Newsletter */
.newsletter {
  text-align: center;
  margin: 0 2rem;
}

.newsletter-flex {
  background: var(--light-color);
  border: 1px solid #eee;
  color: #384653;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  padding: 4rem 2rem;
}

.newsletter h2 {
  font-size: 2rem;
  font-weight: 700;
}

.newsletter p {
  max-width: 600px;
}

.newsletter input[type='email'] {
  padding: 1rem 2rem;
  border: 1px solid #ccc;
  border-radius: 32px;
  margin: 1rem 0;
  width: 100%;
  max-width: 400px;
}
```

We are setting the newsletter container to a flexbox, but we are using `flex-direction: column` to stack the elements vertically. The input field will have a padding of 1rem on the top and bottom and 2rem on the left and right. We are using a border radius of 32px to make the input field rounded. The input field will have a margin of 1rem on the top and 0 on the bottom. The width will be 100% of the container and a maximum width of 400px.

## Media Queries

All I want to do on smaller screens is to reduce the font size of the heading and not display the paragraph. Add the following media query to the `style.css` file:

```css
/* Screens less than 768px */
@media screen and (max-width: 768px) {
  /* ...Other styles */

  .newsletter h2 {
    font-size: 1.5rem;
  }

  .newsletter p {
    display: none;
  }
}
```

The section should look like this:

<img src="../images/tutor-11.png" />
