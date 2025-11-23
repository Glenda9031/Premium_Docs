# Social Icons & Footer

In this section we will create the social icons section and the footer. The social icons will be a simple row of icons with links to social media profiles. The footer will contain a navigation menu, and a copyright text.

## HTML

Let's add the HTML for both sections to the `index.html` file:

```html
<!-- Social -->
<section class="social section">
  <div class="container">
    <p>Follow us on social media for updates and news about our courses</p>

    <div class="social-icons">
      <a href="#"><i class="fa-brands fa-facebook fa-2x"></i></a>
      <a href="#"><i class="fa-brands fa-twitter fa-2x"></i></a>
      <a href="#"><i class="fa-brands fa-instagram fa-2x"></i></a>
      <a href="#"><i class="fa-brands fa-linkedin fa-2x"></i></a>
      <a href="#"><i class="fa-brands fa-youtube fa-2x"></i></a>
      <a href="#"><i class="fa-brands fa-pinterest fa-2x"></i></a>
    </div>
  </div>
</section>

<!-- Footer -->
<footer class="footer">
  <div class="footer-flex container">
    <ul class="footer-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">Terms</a></li>
      <li><a href="#">Privacy</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
    <p>&copy; 2024 Tutor. All rights reserved</p>
  </div>
</footer>
```

## CSS

Let's add the CSS for the social icons and footer sections:

```css
/* Social */
.social {
  background: var(--dark-color);
  color: #fff;
  padding: 6rem 2rem;
  text-align: center;
  font-size: 1.7rem;
  margin-bottom: 0;
}

.social a {
  color: #fff;
}

.social a:hover {
  color: var(--secondary-color);
}

.social p {
  margin-bottom: 2rem;
}

.social-icons {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 2rem;
}

/* Footer */
.footer {
  background: var(--dark-color);
  color: #76859a;
  border-top: 1px solid #384653;
  padding: 0.5rem 2rem;
}

.footer-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer a {
  color: #76859a;
}

.footer a:hover {
  color: var(--secondary-color);
}

.footer ul {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin: 2rem 0;
}
```

We use flexbox to align the social icons and footer links. We add some background colors, padding, etc.

The section should look like this:

<img src="../images/tutor-12.png" />
