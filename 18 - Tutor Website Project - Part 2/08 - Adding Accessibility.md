# Adding Accessibility

In this lesson, I want to add some accessibility to the website. In reality, we should have done this at the time, however, I did not plan on adding accessibility until after the initial recording.

## Navigation Menu

When you have a hamburger menu, you should add the `arial-expanded` as well as `aria-controls` and some other things. Let's replace the current nav with the following:

```html
<nav class="navbar" role="navigation" aria-label="Main Navigation">
  <div class="navbar-flex container">
    <a href="/" aria-label="Logo Home Link">
      <img src="images/logo.svg" alt="Tutor Logo" />
    </a>

    <div class="main-menu-items">
      <ul class="main-menu-list">
        <li>
          <a href="/">Home</a>
        </li>
        <li>
          <a href="#chapters">Chapters</a>
        </li>
        <li>
          <a href="#summary">Summary</a>
        </li>
        <li>
          <a href="#takeaways">Takeaways</a>
        </li>
        <li>
          <a href="#author">Author</a>
        </li>
        <li>
          <a href="contact.html">Contact</a>
        </li>
        <li>
          <a
            href="https://facebook.com"
            target="_blank"
            aria-label="Follow Us On Facebook"
          >
            <i class="fa-brands fa-facebook"></i>
          </a>
        </li>
        <li>
          <a
            href="https://twitter.com"
            target="_blank"
            aria-label="Follow Us On Twitter"
          >
            <i class="fa-brands fa-twitter"></i>
          </a>
        </li>
      </ul>
    </div>

    <!-- Mobile Menu -->
    <div class="mobile-menu">
      <!-- Hamburger button -->
      <div
        class="mobile-menu-toggle"
        role="button"
        aria-expanded="false"
        aria-controls="mobile-menu-items"
        aria-label="Open mobile menu"
        tabindex="0"
      >
        <i class="fas fa-bars fa-2x"></i>
      </div>
      <!-- Mobile Menu Items -->
      <div id="mobile-menu-items" class="mobile-menu-items">
        <ul class="mobile-menu-list">
          <li>
            <a href="/">Home</a>
          </li>
          <li>
            <a href="#chapters">Chapters</a>
          </li>
          <li>
            <a href="#summary">Summary</a>
          </li>
          <li>
            <a href="#takeaways">Takeaways</a>
          </li>
          <li>
            <a href="#author">Author</a>
          </li>
          <li>
            <a href="contact.html">Contact</a>
          </li>
          <li>
            <a
              href="https://facebook.com"
              target="_blank"
              aria-label="Follow Us On Facebook"
            >
              <i class="fa-brands fa-facebook"></i>
            </a>
          </li>
          <li>
            <a
              href="https://twitter.com"
              target="_blank"
              aria-label="Follow Us On Twitter"
            >
              <i class="fa-brands fa-twitter"></i>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</nav>
```

Be sure to change on both the homepage and contact

Here is what we added:

- A role of `navigation` and a label of `Main Navigation` on the `<nav>`
- Added a link around logo with an aria-label
- Aria label on the social media icons
- Added a role, aria-expanded, aria-controls, aria-label and tabindex on the hamburger menu toggle button. That way the user knows it is a button and knows what it controls and when it is expanded.
- Add an id to the toggle button for controls

## Stats

The numbers in the stat section should have a label. There is a heading for each one, so this is a good case for `aria-labelledby`. Change the section to the following:

```html
<!-- Stats -->
    <section class="stats section" id="stats">
      <div class="container stats-flex">
        <img src="images/stats.png" alt="stats" />
        <div class="stats-content">
          <div class="stats-numbers">
            <div>
              <h3 aria-labelledby="stats-happy-users">2000+</h3>
              <p id="stats-happy-users">Happy Users</p>
            </div>
            <div>
              <h3 aria-labelledby="stats-issues-solved">358</h3>
              <p id="stats-issues-solved">Issues Solved</p>
            </div>
            <div>
              <h3 aria-labelledby="stats-good-reviews">980</h3>
              <p id="stats-good-reviews">Good Reviews</p>
            </div>
            <div>
              <h3 aria-labelledby="stats-case-studies">216</h3>
              <p id="stats-case-studies">Case Studies</p>
            </div>
          </div>

          <p class="stats-text">
            Tutor is probably one of the best video courses on landing page
            making in the web industry
          </p>
          <a href="#" class="btn">Get The Course</a>
        </div>
      </div>
    </section>
```

## Social Icon Links

I'm going to do is add a label to the social icon links in at the bottom:

```html
<!-- Social -->
<section class="social section">
  <div class="container">
    <p>Follow us on social media for updates and news about our courses.</p>
    <div class="social-icons">
      <a
        href="https://facebook.com"
        target="_blank"
        aria-label="Follow Us On Facebook"
      >
        <i class="fa-brands fa-facebook fa-2x"></i>
      </a>
      <a
        href="https://twitter.com"
        target="_blank"
        aria-label="Follow Us On Twitter"
      >
        <i class="fa-brands fa-twitter fa-2x"></i>
      </a>
      <a
        href="https://instagram.com"
        target="_blank"
        aria-label="Follow Us On Instagram"
        ><i class="fa-brands fa-instagram fa-2x"></i>
      </a>
      <a
        href="https://linkdin.com"
        target="_blank"
        aria-label="Follow Us On Linkdin"
        ><i class="fa-brands fa-linkedin fa-2x"></i>
      </a>
      <a
        href="https://youtube.com"
        target="_blank"
        aria-label="Follow Us On Youtube"
      >
        <i class="fa-brands fa-youtube fa-2x"></i>
      </a>
      <a
        href="https://pinterest.com"
        target="_blank"
        aria-label="Follow Us On Pinterest"
      >
        <i class="fa-brands fa-pinterest fa-2x"></i>
      </a>
    </div>
  </div>
</section>
```

Be sure to add this to the contact page as well.

There are other things that you could do such as adding roles and creating landmarks, but I think what we have is ok.
