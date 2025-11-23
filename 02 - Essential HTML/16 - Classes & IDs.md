# Classes & IDs

In the last lesson, we created a very simple layout using divs and spans. We used divs to group elements together and spans to apply styles to specific parts of the text. In this lesson, we will look at classes and IDs.

## Classes

A class is an attribute that can be added to an HTML element to apply a specific style to it. It is used to group elements together that share the same style. A class can be used multiple times on a page.

Let's apply some classes to our layout:

```html
<!-- Header -->
<div class="header">
  <h1 class="text-xl">My Website</h1>
  <!-- Navigation -->
  <ul class="nav">
    <li><a href="index.html">Home</a></li>
    <li><a href="about.html">About</a></li>
    <li><a href="contact.html">Contact</a></li>
  </ul>
</div>

<!-- Sections -->
<div class="card text-center">
  <h2 class="text-lg">Section 1</h2>
  <p>
    This is the first paragraph of
    <span class="primary-text">section 1</span>.
  </p>
  <p>
    This is the first paragraph of
    <span class="primary-text">section 1</span>.
  </p>
  <p>This is the second paragraph of section 1.</p>
</div>

<div class="card text-center">
  <h2 class="text-lg">Section 2</h2>
  <p>
    This is the first paragraph of
    <span class="secondary-text">section 2</span>.
  </p>
  <p>
    This is the second paragraph of<span class="secondary-text">section 2</span
    >.
  </p>
</div>

<!-- Footer -->
<div class="footer">@copy; 2024 My Website</div>
```

In this example, I have added classes that describe the content of the element. These can be used in CSS to style each element. Sometimes you will see classes that are more generic like `container`, `card`, or `text-center`. These are utility classes that can be used throughout the project. Other classes are more specific like `header` and `footer`. These are used to target specific elements.

You can also add multiple classes to an element:

```html
<div class="card text-center"></div>
```

This element has two classes: `card` and `text-center`.

This will make more sense when we actually get into the CSS.

## IDs

An ID is an attribute that can be added to an HTML element to target it specifically. It is used to apply a specific style to an element. An ID should only be used once on a page. You can physically add more than one, but the common convention and recommendation is one per page. If you have multiple elements like a card, you would use a class. If you have a specific element like a header, you would use an ID.

Now, there are many ways to use classes and IDs. You can use them for styling, JavaScript, and linking to specific parts of the page. You can target IDs with CSS and style the elements, but I don't recommend using IDs for styling. I recommend using classes for styling and IDs for JavaScript and linking. I have changed my thoughts on this. In fact, in the first version of this course, we used IDs for styling. I have since changed my mind. Anything that is being used purely for styling should be a class. Anything that is being used for JavaScript or linking should be an ID.

Let's add some IDs to our layout:

```html
<!-- Header -->
<div class="header" id="header">
  <h1 class="text-xl">My Website</h1>
  <!-- Navigation -->
  <ul class="nav" id="nav">
    <li><a href="#">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</div>

<!-- Sections -->
<div class="card text-center" id="about">
  <h2 class="text-lg">Section 1</h2>
  <p>
    This is the first paragraph of
    <span class="primary-text">section 1</span>.
  </p>
  <p>
    This is the second paragraph of
    <span class="primary-text">section 1</span>.
  </p>
</div>

<div class="card text-center" id="contact">
  <h2 class="text-lg">Section 2</h2>
  <p>
    This is the first paragraph of
    <span class="secondary-text">section 2</span>.
  </p>
  <p>
    This is the second paragraph of
    <span class="secondary-text">section 2</span>.
  </p>
</div>

<!-- Footer -->
<div class="footer" id="footer">@copy; 2024 My Website</div>
```

In this example, I have added IDs to the header, navigation, sections, and footer. These can be used to target specific elements with JavaScript or link to specific parts of the page. If I click on the About link in the navigation, it will take me to the About section. This is done by adding an anchor tag with the href attribute set to the ID of the element I want to link to. If I click on the Contact link, it will take me to the Contact section.

There are many cases where you won't even need to use IDs. You can use classes for both styling and JavaScript. But it's good to know how to use them.
