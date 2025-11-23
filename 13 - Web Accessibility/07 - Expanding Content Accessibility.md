# Expanded Content Accessibility

There will be times where there are tabs, accordions and other ways to show content where some of the content is hidden until the user interacts with it. This is great for saving space and keeping things organized, but it can be a problem for screen readers and other assistive technologies. We need to make sure that the content is accessible to everyone. This is where the `aria-expanded` attribute comes in. We can also use the `region` role to make the content more accessible.

I have the CSS and JS for a simple accordion below.

## CSS

```css
body {
  font-family: 'Arial', sans-serif;
}

.accordion {
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 20px;
}

.accordion-header {
  background-color: #f0f0f0;
  padding: 10px;
  cursor: pointer;
}

.accordion-content {
  display: none;
  padding: 10px;
}

.accordion-content {
  display: none; /* Hide content by default */
}

.accordion-content[aria-hidden='false'] {
  display: block; /* Show content when aria-hidden is false */
}
```

## JS

```js
document.addEventListener('DOMContentLoaded', function () {
  const headers = document.querySelectorAll('.accordion-header');

  headers.forEach((header) => {
    header.addEventListener('click', () => {
      const content = header.nextElementSibling;
      const expanded = header.getAttribute('aria-expanded') === 'true';

      // Toggle aria-expanded attribute
      header.setAttribute('aria-expanded', !expanded);

      // Toggle aria-hidden attribute
      content.setAttribute('aria-hidden', expanded);

      console.log('Accordion header clicked');
      console.log('aria-expanded:', header.getAttribute('aria-expanded'));
    });

    header.addEventListener('keydown', (event) => {
      if (event.key === 'Enter' || event.key === ' ') {
        event.preventDefault();
        header.click();
      }
    });
  });
});
```

## HTML

Now let's add some HTML to make it work:

```html
<div class="accordion">
  <div class="accordion-header" id="accordion-heading">
    Section 1: Introduction
  </div>
  <div class="accordion-content" id="accordion-content">
    <p>This section provides an introduction to the topic.</p>
  </div>
</div>
```

This will show the accordion and it will work, but if you try it through the screen reader, it is not very accssible.

Let's add a few things:

1. Add a role of button to the header
2. Add `aria-controls` to the header to let the screen reader know that this element controls the content element
3. Add `aria-expanded` to the false initially because it is collapsed. In the JavaScript, it is set to true when expanded.
4. Add `tabindex=0` because we want this to be able to be selected by tab like any button
5. Add a role of `region` to identify the content as a region and make it easily accessible
6. Add `aria-labelledby` to the content and set it to the id of the header. This will associate the content with the header.

Here is the updated HTML:

```html
<div class="accordion" role="region" aria-labelledby="accordion-heading">
  <div
    class="accordion-header"
    id="accordion-heading"
    role="button"
    aria-controls="accordion-content"
    aria-expanded="false"
    tabindex="0"
  >
    Section 1: Introduction
  </div>
  <div
    class="accordion-content"
    id="accordion-content"
    role="region"
    aria-labelledby="accordion-heading"
    aria-hidden="true"
  >
    <p>This section provides an introduction to the topic.</p>
  </div>
</div>
```

Now, when you run the screen reader, it will announce the section and let the user know that it is a button. When the user clicks on the button, it will announce that the content is expanded. If you collapse, it will let the user know that it is collapsed. This is a much better experience for the user.
