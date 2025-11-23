# Sizing Elements

The `width` and `height` properties are used to set the width and height of an element.

Let's use the following HTML:

```html
<div class="box box-1">
  <h1>Box 1</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ad, excepturi
    quos repudiandae tenetur deserunt mollitia quasi unde explicabo laudantium.
  </p>
</div>
<div class="box box-2">
  <h1>Box 2</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ad, excepturi
    quos repudiandae tenetur deserunt mollitia quasi unde explicabo laudantium.
  </p>
</div>
<div class="box box-3">
  <h1>Box 3</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero ad, excepturi
    quos repudiandae tenetur deserunt mollitia quasi unde explicabo laudantium.
  </p>
</div>
```

I am going to give you some pre-written CSS to style this HTML. Don't worry about this for now.

```css
body {
  font-family: 'Poppins', sans-serif;
}

.box {
  background-color: darkblue;
  color: white;
  text-align: center;
  padding: 20px;
  margin: 20px;
}
```

Let's add the `width` using pixels to the `.box-1` class.

```css
.box-1 {
  width: 200px;
}
```

The `.box-1` element will now have a width of `200px`. The height of the box is not set but it will adjust to the content inside it. We could also set the height to `auto`.

## Overflow

Let's add a height of `100px`, which is less than the content inside the `.box-2` element.

```css
.box-2 {
  width: 200px;
  height: 100px;
}
```

you can see that the text overflows the box. This is because the content is larger than the height of the box. We can control how the content overflows the box using the `overflow` property.

By default, it is set to `visible`, which means that the content will overflow the box. We can set it to `hidden`, `scroll`, or `auto`.

```css
.box-2 {
  width: 200px;
  height: 100px;
  overflow: hidden;
}
```

The `hidden` value will hide the content that overflows the box. The `scroll` value will add a scrollbar to the box if the content overflows. The `auto` value will add a scrollbar only if the content overflows.

We can also use percentages to set the width and height of an element. Let's set the width of the `.box-3` element to `50%`.

```css
.box-3 {
  width: 50%;
}
```

## Min and Max Width and Height

We can also set the minimum and maximum width and height of an element using the `min-width`, `max-width`, `min-height`, and `max-height` properties.

Let's set the minimum width of the `.box-3` element to `200px` and the maximum width to `400px`.

```css
.box-3 {
  width: 50%;
  min-width: 200px;
  max-width: 400px;
}
```

The `.box-3` element will have a width of `50%` but will not be able to go below `200px` or above `400px`.

The reason you would use these properties is to ensure that the element does not become too small or too large, which can affect the layout of the webpage.
