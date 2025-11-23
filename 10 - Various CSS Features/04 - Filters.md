# CSS Filters

CSS filters allow you to apply visual effects to images and elements. You can use them to adjust the color, contrast, brightness, and more. Filters are a great way to enhance your designs and make them more visually appealing.

Let's start with the following HTML:

```html
<div class="container">
  <img class="image" src="./mario.jpg" alt="" />
</div>
```

And the following CSS:

```css
img {
  width: 100%;
}

.container {
  max-width: 900px;
  margin: 70px auto;
}
```

We just have a simple image inside a container. Let's add some filters to it.

## Grayscale

The `grayscale` filter converts an image to grayscale. You can specify the amount of grayscale by using a percentage value.

Add the following CSS:

```css
.image {
  filter: grayscale(100%);
}
```

This maybe a case where you want to use vendor prefixes for better browser support. If you search https://shouldiprefix.com/ for filters, you'll see that you should use prefixes for `filter`. It actually only recommends `-webkit-filter` for Safari, but we'll use it for all browsers.

```css
.image {
  filter: grayscale(100%);
  -webkit-filter: grayscale(100%);
  -moz-filter: grayscale(100%);
  -o-filter: grayscale(100%);
  -ms-filter: grayscale(100%);
}
```

Now the image will be grayscale. You can adjust the amount of grayscale by changing the value.

## Blur

The `blur` filter applies a blur effect to an element. You can specify the amount of blur by using a length value.

```css
.image {
  filter: blur(5px);
}
```

Now the image has a blur to it. You can adjust the amount of blur by changing the value. Change to 50px and see the difference.

## Brightness

The `brightness` filter adjusts the brightness of an element. You can specify the brightness by using a percentage value.

```css
.image {
  filter: brightness(200%);
}
```

Now the image will be twice as bright. You can adjust the brightness by changing the value. You can use a range from 0 to 1000 percent. 100 is the default value.

## Contrast

The `contrast` filter adjusts the contrast of an element. You can specify the contrast by using a percentage value.

```css
.image {
  filter: contrast(200%);
}
```

Now the image will have twice the contrast. You can adjust the contrast by changing the value. You can use a range from 0 to 1000 percent. 100 is the default value.

## Drop Shadow

The `drop-shadow` filter applies a drop shadow to an element. You can specify the horizontal offset, vertical offset, blur radius, and color.

```css
.image {
  filter: drop-shadow(10px 10px 5px red);
}
```

Now the image will have a red drop shadow. You can adjust the values to change the shadow.

## Hue Rotate

The `hue-rotate` filter rotates the colors of an element. You can specify the angle of rotation in degrees.

```css
.image {
  filter: hue-rotate(90deg);
}
```

Now the image will have its colors rotated by 90 degrees. You can adjust the angle to change the colors.

## Invert

The `invert` filter inverts the colors of an element. You can specify the amount of inversion by using a percentage value.

```css
.image {
  filter: invert(100%);
}
```

Now the image will have its colors inverted. You can adjust the amount of inversion by changing the value.

## Opacity

The `opacity` filter adjusts the opacity of an element. You can specify the opacity by using a percentage value.

```css
.image {
  filter: opacity(50%);
}
```

Now the image will be 50% transparent. You can adjust the opacity by changing the value. This is similar to the `opacity` property in CSS.

## Saturate

The `saturate` filter adjusts the saturation of an element. You can specify the saturation by using a percentage value.

```css
.image {
  filter: saturate(200%);
}
```

Now the image will be twice as saturated. You can adjust the saturation by changing the value. You can use a range from 0 to 1000 percent. 100 is the default value.

## Sepia

The `sepia` filter converts an image to sepia. You can specify the amount of sepia by using a percentage value.

```css
.image {
  filter: sepia(100%);
}
```

Now the image will be sepia. You can adjust the amount of sepia by changing the value.

## Multiple Filters

You can chain multiple filters together. Let's apply a grayscale filter and a blur filter to the image.

```css
.image {
  filter: grayscale(100%) blur(5px);
}
```

Now the image will be grayscale and have a blur effect. You can chain as many filters as you want.

## Reset Filters

You can reset the filters by using the `none` value.

```css
.image {
  filter: none;
}
```

Now the image will have no filters applied.
