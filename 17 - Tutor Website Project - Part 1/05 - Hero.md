# Hero

Now we will create the Hero section of the website. This is the first thing that users will see when they visit the website. It is important to make a good first impression, so we want to make sure that this section looks great. It will have some text, image, and a call-to-action button. We will also add a background image and an svg at the bottom to give it a wave effect.

## How The SVG Wave Works

We will be using an SVG wave at the bottom of the hero section. This will give the section a nice effect. The SVG wave is created using the `<svg>` tag and the `<path>` tag. The `<path>` tag is used to define a path. The `d` attribute is used to define the path data. The path data is a list of commands and parameters that define the path. The `M` command is used to move to a point, the `C` command is used to draw a cubic Bezier curve, and the `Z` command is is used to close the path. Now it is important to understand that we don't usually just write the path data by hand. you would most likely use a tool to generate the path data for us. You can use something like [Blobmaker](https://www.blobmaker.app/) to generate the SVG wave. When you are a developer for a company, you are usually going to have someone else create the entire design and layout within a design tool like Figma or Adobe XD. They will then export the SVG for you to use in the project. That is the approach that we are taking here. We will pretend that we have a designer that has given us the SVG wave to use in the project.

## HTML

Let's start by adding the HTML for the Hero section. Open the `index.html` file and add the following code right under the navbar section:

```html
<!-- Hero -->
<header class="hero">
  <div class="hero-container container">
    <div class="hero-content">
      <h1>Create Your Own Video Courses</h1>
      <p>
        Dive deep into the world of creativity and learn to craft stunning
        videos that captivate your audience.
      </p>
      <a href="#" class="btn">$29 Get Course</a>
    </div>
    <img src="images/header-course.png" alt="hero" />
  </div>
</header>
```

We have a `header` tag with a class of `hero`. Inside the `header` tag, we have a `div` tag with a class of `hero-container`. This is a container that will hold the content of the hero section. Inside the `hero-container` div, we have two children. The first div has a class of `hero-content`. The second element is an `img` tag.

We will use flexbox to align the content of the hero section. The `hero-container` div will have a `display` of `flex`. Let's add the following CSS:

```css
/* Hero */
.hero {
  padding: 11.5rem 2rem 8rem;
  background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url('../images/header-background.jpg') center center/cover no-repeat;
  color: #fff;
  overflow-x: hidden;
  position: relative;
}

.hero-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 8rem;
  gap: 6rem;
}

.hero h1 {
  font-size: 3.5rem;
  line-height: 1.2;
  font-weight: 700;
  margin-bottom: 1rem;
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 2rem;
  line-height: 1.8;
  font-weight: 400;
}

.hero img {
  margin-right: -100px;
  width: 100%;
}
```

The `hero` background image is set using the `background` property. We are using a linear gradient to create a dark overlay on the background image. This will make the text more readable. The `hero-container` div has a `display` of `flex` and `justify-content` of `space-between`. This will align the content to the left and right edges of the container. The `gap` property is used to add space between the two children of the `hero-container` div. The `hero img` has a `margin-right` of `-100px`. This will move the image to the left by 100px. This is a common technique used to create overlapping elements. The `overflow-x` property is set to `hidden` on the `hero` class. This will hide any content that overflows the x-axis. We will use this to hide the SVG wave that we will add later.

## Button Styling

We have a class of `btn` on the button. Let's add the following CSS in the utility class part of the CSS file to style the button:

```css
.btn {
  display: inline-block;
  padding: 1.6rem 2.6rem;
  border: 1px solid var(--secondary-color);
  border-radius: 32px;
  background-color: var(--secondary-color);
  color: #384653;
  font-weight: 600;
  font-size: 0.875rem;
  line-height: 0;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.2s;
}

.btn:hover {
  background-color: var(--primary-color);
  border-color: #fff;
  color: #fff;
}
```

We are adding some padding, border, border-radius, background color, and text color to the button. We are also adding a hover effect to the button. When the button is hovered, the background color, border color, and text color will change.

## SVG Wave

Now we are going to apply the SVG wave at the bottom of the hero section. We will add the following code right above the closing `header` tag:

```html
<svg
  class="frame-decoration"
  data-name="Layer 2"
  xmlns="http://www.w3.org/2000/svg"
  preserveAspectRatio="none"
  viewBox="0 0 1920 192.275"
>
  <defs>
    <style>
      .cls-1 {
        fill: #ffffff;
      }
    </style>
  </defs>
  <title>frame-decoration</title>
  <path
    class="cls-1"
    d="M0,158.755s63.9,52.163,179.472,50.736c121.494-1.5,185.839-49.738,305.984-49.733,109.21,0,181.491,51.733,300.537,50.233,123.941-1.562,225.214-50.126,390.43-50.374,123.821-.185,353.982,58.374,458.976,56.373,217.907-4.153,284.6-57.236,284.6-57.236V351.03H0V158.755Z"
    transform="translate(0 -158.755)"
  />
</svg>
```

There is a class on the SVG tag called `frame-decoration`. We will use this class to style the SVG wave. Add this to the CSS file:

```css
.hero .frame-decoration {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100px;
}
```

This will position the SVG wave at the bottom of the hero section. The `position` is set to `absolute`, `bottom` is set to `0`, and `left` is set to `0`. This will position the SVG wave at the bottom left corner of the hero section. The `width` is set to `100%` and the `height` is set to `100px`. This will make the SVG wave take up the full width of the hero section and have a height of 100px.

## Media Queries For The Hero Section

We need to make the hero section responsive. Let's add the following media queries to the CSS file:

```css
/* Screens less than 1200px */
@media (max-width: 1200px) {
  .hero .hero-flex {
    gap: 2rem;
  }

  .hero img {
    max-width: 500px;
    margin-right: 0;
  }

  .hero h1 {
    font-size: 3rem;
  }
}
```

We are changing the spacing and the size of the image and fonts for screens less than 1200px.

Let's add another media query for screens less than `992px`:

```css
/* Screens less than 992 */
@media (max-width: 992px) {
  .hero {
    text-align: center;
  }

  .hero .hero-flex {
    flex-direction: column;
    padding-bottom: 4rem;
  }

  .hero img {
    max-width: 600px;
    margin-top: 2rem;
  }
}
```

We don't need to add anything for the `768px` media query.

Finally, for the `576px` breakpoint, we will just change the image width:

```css
/* Screens less than 576 */
@media (max-width: 576px) {
  .hero {
    padding-right: 0.2rem;
    padding-left: 0.2rem;
  }

  .hero h1 {
    font-size: 2.5rem;
  }

  .hero img {
    max-width: 350px;
  }
}

```

Now the hero section should look good on all of the screen sizes. it should look like this:

<img src="../images/tutor-3.png" alt="Hero Section">
