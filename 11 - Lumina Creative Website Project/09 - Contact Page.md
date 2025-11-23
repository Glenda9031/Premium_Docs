# Contact Page

Create a `contact.html` page and copy and paste everything from one of the other pages and remove everything from within the header and footer. Also, change the `current` class to the contact link.

The HTML should look like this so far:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap"
      rel="stylesheet"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"
      integrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <link rel="stylesheet" href="css/styles.css" />
    <link rel="icon" href="images/favicon.ico" />
    <title>Luimna Creative</title>
  </head>
  <body>
    <header class="header">
      <div class="container header-flex">
        <div class="logo"><img src="images/logo.png" alt="SparkPort" /></div>
        <ul class="main-menu">
          <li><a href="index.html">Home</a></li>
          <li><a href="about.html">About</a></li>
          <li><a href="contact.html" class="current">Contact</a></li>
        </ul>
      </div>
    </header>

    <footer class="footer">
      <div class="container footer-flex">
        <img src="images/logo.png" alt="" />

        <div class="contact">
          <h4>Contact Us</h4>
          <ul>
            <li>(555) 555-5555</li>
            <li>contact@lumina.test</li>
            <li>10 Main st, Boston MA 02011</li>
          </ul>
        </div>

        <div class="social">
          <h4>Follow Us</h4>
          <a href="#"><i class="fab fa-facebook fa-2x"></i></a>
          <a href="#"><i class="fab fa-twitter fa-2x"></i></a>
          <a href="#"><i class="fab fa-instagram fa-2x"></i></a>
          <a href="#"><i class="fab fa-pinterest fa-2x"></i></a>
          <a href="#"><i class="fab fa-tumblr fa-2x"></i></a>
        </div>
      </div>
    </footer>
  </body>
</html>
```

## Hero

The hero is simple, add the following HTML:

```html
<section class="hero hero-reverse">
  <div class="container">
    <h2>
      <span class="bg-primary">Enthusiastic</span> thinkers, creating unique
      endeavors powered by <span class="bg-primary">creativity</span>.
    </h2>
  </div>
</section>
```

There is a slight change here. We added the class of `hero-reverse`. I want this one to have a dark background and light text.

Let's add the following CSS:

```css
.hero-reverse {
  background: #333;
  color: #fff;
}

.hero-reverse .bg-primary {
  color: #333;
}
```

Now the hero should be reversed.

## Contact Form

Now we want to add the HTML for the form:

```html
<section class="contact">
  <div class="container container-sm">
    <h2 class="section-heading">Contact Us</h2>
    <p>
      Have a question? Leave your information below and we will get back to you
      as soon as possible.
    </p>
    <form>
      <div class="form-group">
        <label for="first-name" class="visually-hidden">First Name</label>
        <input
          id="first-name"
          name="first-name"
          placeholder="First Name"
          type="text"
        />
      </div>
      <div class="form-group">
        <label for="last-name" class="visually-hidden">Last Name</label>
        <input
          id="last-name"
          name="last-name"
          placeholder="Last Name"
          type="text"
        />
      </div>
      <div class="form-group">
        <label for="email" class="visually-hidden">Email</label>
        <input
          id="email"
          name="email"
          placeholder="Email Address"
          type="email"
        />
      </div>
      <div class="form-group">
        <label for="message" class="visually-hidden">Message</label>
        <textarea id="message" name="message" placeholder="Message"></textarea>
      </div>
      <div class="form-group">
        <button class="btn" type="submit">Send Message</button>
      </div>
    </form>
  </div>
</section>
```

We are re-using the `section-heading` class here. The form is made up of `form-group` elements that have a label and an input. Notice the labels have a class of `visually-hidden`. That is because I don't want the labels to show as we will use the placeholders, however, we still want to include them for accessibility reasons. So we will add some styles to not show them but still have it there. We also have a class of `btn` on the button. This will be a utility class in case you want to re-use the button style.

Let's add the CSS for the contact area and form:

```css
/* Contact */
.contact {
  padding: 3rem 0 4rem;
}

.contact p {
  text-align: center;
  padding-bottom: 2rem;
}

.contact .form-group {
  margin: 2rem 0;
}

.contact input,
.contact textarea {
  border: none;
  border-bottom: 1px #333 solid;
  width: 100%;
  font-family: inherit;
  font-size: inherit;
  padding-bottom: 1rem;
}

.contact textarea {
  height: 200px;
}

.contact input:focus,
.contact textarea:focus {
  outline: none;
}
```

We have some padding on the section itself. The `.form-group` has some margin to space out the fields. We added a bunch of styles on the inputs and textarea. We made it so only the bottom border shows so it looks like a line for the inputs. I think this makes it look cleaner.

## Hide Labels

Let's add the CSS to hide the labels:

```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
```

We can't just use `display: none` because it will be completely removed. Instead, we just positioned it off the page.

The CSS clip property is used to specify a rectangular region that is visible within an element's box. The rect() function is used to define the rectangular region.

`clip: rect(0, 0, 0, 0)` sets the clipping region to be a rectangle with all sides having a length of 0. This essentially hides the entire content of the element, making it invisible.

## Button Class

Let's add the style for the `.btn` class with the rest of the utility classes:

```css
.btn {
  display: inline-block;
  padding: 1rem 2rem;
  border: 1px solid #333;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  cursor: pointer;
}

.btn:hover {
  background: #333;
  color: #fff;
}
```

We make it an inline block and add some padding, inherit the font styles, give it a transparent background, etc.

I do want the contact form button to span the entire width. So let's add this:

```css
.contact .btn {
  width: 100%;
}
```

That's it! The form should look like this:

<img src="../images/lumina-8"  alt="" width="600" />
