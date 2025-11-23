# The Viewport

The viewport is the **user's visible area of a web page**. It varies with the device. Obviously, it will be smaller on a smartphone than on a desktop screen. Years ago, websites were designed for desktop screens, and the viewport was the same as the screen size. But now, with the rise of mobile devices, websites need to be responsive and adapt to different screen sizes.

HTML5 introduced the `viewport` meta tag to control the layout on mobile browsers. This tag gives the browser instructions on how to control the page's dimensions and scaling. We have been using the `viewport` meta tag in our projects, but we haven't really talked about it yet. Let's see how it works.

## The `viewport` Meta Tag

The `viewport` meta tag looks like this:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

If you don't include this tag in your HTML, the browser will render the page at a typical desktop screen width, scaled to fit the screen. This means that the text will be too small to read on a mobile device. The `viewport` meta tag tells the browser to set the page width to the device's width and scale it to 100%.

<img src="../images/viewport.png" alt="Viewport" width="500">

The `viewport` meta tag has a few attributes that you can use to control the layout:

- `width=device-width`: Sets the width of the page to follow the screen width of the device. This is essential for responsive web design.
- `initial-scale=1.0`: Sets the initial zoom level when the page is first loaded by the browser. 1.0 means no zoom. A value of 0.5 would zoom the page out to 50%, and a value of 2.0 would zoom the page in to 200%.

You can also set the `viewport` meta tag to disable zooming:

```html
<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"
/>
```

This will prevent the user from zooming in or out on the page. This is not recommended because it can make your website inaccessible to people with visual impairments.

That's really it. Just be sure to always include the `viewport` meta tag in your projects. Luckily, Emmet adds it automatically with the `!` shortcut. You can also use the `meta:vp` Emmet abbreviation to add the `viewport` meta tag.
