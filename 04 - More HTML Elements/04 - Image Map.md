# Image Map

An image map allows us to create clickable areas within an image using the `<map>` tag and the `usemap` attribute.

Let's use the following example:

```html
<img src="computer.jpg" alt="Computer" usemap="#computermap" />

<map name="computermap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.html">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.html">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.html">
</map> 
```

We use the `usemap` attribute on the image and then create a map with a `name` attribute that matches the usemap.

In that, we use an `<area>` tag to make a shape using coordinates. The area that we specify will be clickable and will go to the page in the `href` attribute.