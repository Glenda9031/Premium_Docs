# SVG (Scalable Vector Graphics) Element

SVG (Scalable Vector Graphics) is an XML-based vector image format for two-dimensional graphics with support for interactivity and animation. What makes SVG different from other image formats is that it can be created and edited with any text editor, as well as with drawing software and SVGs do not lose any quality if they are zoomed or resized like a png or any other image format.

Creating SVGs from scratch is a bit of a pain, but there are a number of tools that can help you create them. Here are a few:

- [Inkscape](https://inkscape.org/)
- [Adobe Illustrator](https://www.adobe.com/products/illustrator.html)
- [Adobe XD](https://www.adobe.com/products/xd.html)
- [Figma](https://www.figma.com/)
- [Adobe Spark](https://spark.adobe.com/)
- [Adobe Photoshop](https://www.adobe.com/products/photoshop.html)

## Creating a Simple SVG

Here is a simple SVG that creates a red circle with a border and some text in it:

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="red" stroke="black" stroke-width="4" />
  <text
    x="50"
    y="60"
    font-family="Verdana"
    font-size="30"
    text-anchor="middle"
    fill="white"
  >
    SVG
  </text>
</svg>
```

If you want to create really intricate SVGs, you can use a tool like [Inkscape](https://inkscape.org/).

Blob shapes are popular in the design world. You may use something like [Blobmaker](https://www.blobmaker.app/) to create them. Here is an example of a blob shape SVG:

```html
<svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
  <path
    fill="#FF0066"
    d="M47.9,-55.3C62.4,-45,74.6,-30.1,77.3,-13.8C80,2.5,73.1,20.4,63.5,36.2C53.8,52,41.4,65.8,26.1,71.1C10.8,76.4,-7.3,73.2,-20.2,64.6C-33.1,56,-40.7,41.9,-51.1,27.6C-61.6,13.4,-74.9,-1.1,-72.7,-12.7C-70.5,-24.2,-52.7,-32.9,-38,-43.2C-23.3,-53.6,-11.6,-65.5,2.5,-68.5C16.7,-71.6,33.5,-65.7,47.9,-55.3Z"
    transform="translate(100 100)"
  />
</svg>
```

You probably don't want to type all of that out by hand.
