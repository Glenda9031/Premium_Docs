# Make The Page Responsive

Now that we have the page looking good on desktops, let's make sure it looks great on mobile devices as well. We'll use a media query to adjust the layout and styling for smaller screens.

Add a media query at the bottom for screens smaller than `768px`:

```css
@media (max-width: 768px) {
}
```

## Header

In the media query, let's add the responsive header styles:

```css
 .header,
  .header .header-right {
    flex-direction: column;
    gap: 10px;
  }
```

We are just changing the layout from a horizontal row to a vertical column on smaller screens for both the header and the header-right elements

## Main Content

Add the following in the media query:

```css
.main-content {
  flex-direction: column-reverse;
  justify-content: start;
  margin: auto;
  padding-bottom: 50px;
}

.main-content form,
.main-content div {
  width: 100%;
}
```

Here, we are again, setting the layout to a column on smaller screens and centering the content. I used `column-reverse` because I want the form the bottom.

We set the `justify-content` to `start` so that the form and the text container are aligned to the top of the screen. This way, there is some space between the header and the main content on smaller screens but not too much space.

I also set the width to `100%` so that the form and the text container take up the full width of the screen.

## Text Container

Add the following in the media query:

```css
.text-container h1 {
  font-size: 40px;
  text-align: center;
  line-height: 1.4;
}

.text-container p {
  display: none;
}
```

I increased the font size of the heading and centered it. I also set the line height to `1.4` to make the text easier to read. I set the small text to `display: none` so that it doesn't show up on smaller screens.


That's it. Now it should look decent on mobile screens.
