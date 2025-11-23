# Aria Attributes

In this lesson, we will go over some Aria attributes and how they can be used to make our HTML more accessible. We will learn about and use attributes like `aria-label`, `aria-labelledby`, `aria-describedby`, `aria-hidden`, `aria-expanded`, and `tabindex`.

## Aria-label

We already looked at the `aria-label` attribute in the previous lesson. This is an attribute that is used to provide an accessible name for an element. A good place to use this is when you have a link without text. For example, if you have an icon that is a link, you can use the `aria-label` attribute to provide a name for the link.

```html
<a href="https://instagram" aria-label="Follow us on instagram"
  ><i class="fa-brands fa-instagram"></i
></a>
```

## Aria-labelledby

The `aria-labelledby` attribute identifies the element (or elements) that labels the element it's applied to.

Let's look at the following HTML and run the screen reader:

```html
<h3>Company Links</h3>
<nav>
  <ul>
    <li><a href="/privacy">Privacy Policy</a></li>
    <li><a href="/terms">Terms Of Service</a></li>
    <li><a href="/contact">Contact Us</a></li>
  </ul>
</nav>
```

It reads the heading but then just says "List with 3 items". We can use the `aria-labelledby` attribute to provide an accessible name for the list.

```html
<h3 id="company-links">Company Links</h3>
<nav aria-labelledby="company-links">
  <ul>
    <li><a href="/privacy">Privacy Policy</a></li>
    <li><a href="/terms">Terms Of Service</a></li>
    <li><a href="/contact">Contact Us</a></li>
  </ul>
</nav>
```

Now it will read out "Company Links". This is useful for when you have a heading that describes a section of content.

## Aria-hidden

The `aria-hidden` attribute hides the current element from screen readers. This is useful when the element is purely decorative and does not add any meaning to the content.

A lot of people get confused and think that this will hide the content from the page so it is only visible to screen readers. This is not the case. This attribute will hide the content from screen readers but it will still be visible on the page if set to true. If set to false, it will be visible to screen readers as well as the page.

Run the screen reader with the following 2 paragraphs. It will skip the first one because it is hidden.

```html
<p aria-hidden="true">This content is hidden.</p>
<p aria-hidden="false">This content is not hidden.</p>
```
