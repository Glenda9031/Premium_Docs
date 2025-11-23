# About Page

The about page will consist of hero with a different slogan, a services section and a team section.

Let's create an `about.html` file if you haven't already and copy and paste the entire `index.html`. Then remove everything in between the header and footer. Also, change the `.current` class to be on the about link.

```html
<li><a href="about.html" class="current">About</a></li>
```

Here is the code so far:

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
          <li><a href="about.html" class="current">About</a></li>
          <li><a href="contact.html">Contact</a></li>
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

## Hero Section

Let's start with the hero section HTML

```html
<section class="hero">
  <div class="container">
    <h2>
      <span class="bg-primary"> Inspired</span> minds, shaping exceptional
      projects fueled by <span class="bg-primary">ingenuity</span>.
    </h2>
  </div>
</section>
```

There is actually nothing we have to do in the CSS because we already have those styles. We are just changing the text.

## Services Section

Let's add the services HTML:

```html
<section class="services">
  <div class="container">
    <h2 class="section-heading">Our Services</h2>
    <div class="services-flex">
      <div class="service-item">
        <h4>Photography</h4>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt eum
          eveniet optio ut ab? Dolorum maxime velit tempore! Repellat, sint!
        </p>
      </div>
      <div class="service-item">
        <h4>Web Design</h4>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt eum
          eveniet optio ut ab? Dolorum maxime velit tempore! Repellat, sint!
        </p>
      </div>
      <div class="service-item">
        <h4>Graphic Design</h4>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Incidunt eum
          eveniet optio ut ab? Dolorum maxime velit tempore! Repellat, sint!
        </p>
      </div>
    </div>
  </div>
</section>
```

This is pretty simple. We have a section with a `.services` class. In the container is a `.section-heading` class, which is a utility class because we will use this in other places as well. Then we have the services flexbox and some items.

Let's add the CSS for the section heading. Put this with the other utility classes:

```css
.section-heading {
  font-size: 1.6rem;
  text-align: center;
  margin-bottom: 40px;
}
```

Now for the services CSS:

```css
/* Services */
.services {
  background: #333;
  color: #fff;
  padding: 3rem 0 4rem;
}

.services-flex {
  display: flex;
  gap: 2rem;
}

.service-item h4 {
  font-size: 1.1rem;
  margin-bottom: 10px;
}
```

Here, we are setting a background color of `#333` to the services section. Notice we did not add it to or within the container, because we want it to spread all the way across the page. This is a common practice for backgrounds. We also added some padding.

Then we created a flexbox with some other basic styling on that and the items.

## Team Section

Now let's add the HTML for the team section:

```html
<section class="team">
  <div class="container container-lg">
    <h2 class="section-heading">Our Team</h2>
    <div class="team-flex">
      <div class="team-item">
        <img src="images/team1.jpg" alt="" />
        <h4>Kevin Samson</h4>
        <p>Founder</p>
      </div>
      <div class="team-item">
        <img src="images/team2.jpg" alt="" />
        <h4>Rebecca Willliams</h4>
        <p>Designer</p>
      </div>
      <div class="team-item">
        <img src="images/team3.jpg" alt="" />
        <h4>Ben Markson</h4>
        <p>Designer/Developer</p>
      </div>
    </div>
  </div>
</section>
```

Very simple. We have the heading and then the flexbox with some images of the team members.

Let's add the CSS:

```css
/* Team */
.team {
  padding: 3rem 0 4rem;
}

.team-flex {
  display: flex;
  gap: 20px;
}

.team-item {
  flex: 1;
}

.team-item img {
  border-radius: 10px;
}
```

We added some basic styles and the flexbox.

## Media Query

We want the services and team items to stack on small screens. Add the following in the media query:

```css
.header-flex,
.footer-flex,
.services-flex,
.team-flex {
  flex-direction: column;
  gap: 20px;
}
```

The page should look like this:

<img src="../images/lumina-7.png" alt="" width="600" />
