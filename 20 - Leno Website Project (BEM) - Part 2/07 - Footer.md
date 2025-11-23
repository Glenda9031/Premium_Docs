# Footer

The footer will have 3 columns. The first will be an about section, the second will be quick links and the last will be some social icons/links.

## HTML

Let's add the HTML:

```html
<!-- Footer -->
<footer class="footer">
  <div class="footer__container container">
    <div class="footer__about">
      <div class="footer__title">About Leno</div>
      <div class="footer__description">
        Leno is a mobile app that helps you stay focused and improve your
        productivity. The app provides you with tools to set goals, track your
        progress, and maintain a healthy work-life balance.
      </div>
    </div>
    <div class="footer__links">
      <div class="footer__title">Quick Links</div>
      <ul class="footer__links-list">
        <li class="footer__links-item">
          <a href="#home" class="footer__links-link">Home</a>
        </li>
        <li class="footer__links-item">
          <a href="#testimonials" class="footer__links-link">Testimonials</a>
        </li>
        <li class="footer__links-item">
          <a href="#features" class="footer__links-link">Features</a>
        </li>
        <li class="footer__links-item">
          <a href="#preview" class="footer__links-link">Preview</a>
        </li>
        <li class="footer__links-item">
          <a href="#details" class="footer__links-link">Details</a>
        </li>
        <li class="footer__links-item">
          <a href="#download" class="footer__links-link">Download</a>
        </li>
      </ul>
    </div>
    <div class="footer__social">
      <a href="#" class="footer__social-link"
        ><i class="fa-brands fa-facebook fa-3x"></i
      ></a>
      <a href="#" class="footer__social-link"
        ><i class="fa-brands fa-twitter fa-3x"></i
      ></a>
      <a href="#" class="footer__social-link"
        ><i class="fa-brands fa-instagram fa-3x"></i>
      </a>
      <a href="#" class="footer__social-link"
        ><i class="fa-brands fa-linkedin fa-3x"></i>
      </a>
    </div>
  </div>
</footer>
```

## CSS

Now for the CSS:

```css
/* Footer */
.footer {
  padding: 4rem 2rem;
  background: var(--tertiary-color);
  color: #9f9caf;
  font-size: 0.9rem;
}

.footer a {
  color: #9f9caf;
}

.footer a:hover {
  color: #fff;
}

.footer__container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  justify-content: space-between;
  align-items: center;
  gap: 6rem;
}

.footer__title {
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
  color: #fff;
}

.footer__social {
  display: flex;
  justify-content: center;
  gap: 1.5rem;
}
```

This is simple. We are using a grid layout for the footer container and flex for the social links.

Let's make the footer responsive. Add the following CSS to the `992px` media query:

```css
.footer {
  font-size: 1rem;
}

.footer__container {
  grid-template-columns: 1fr;
  text-align: center;
  gap: 3rem;
  max-width: 600px;
}
```

Now everything in the footer will stack and center.
