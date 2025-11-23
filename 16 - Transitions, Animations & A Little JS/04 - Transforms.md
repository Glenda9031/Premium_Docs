# Transforms

We looked at the `transition` property in the last lesson. Now we are going to look at transforms, which are often used with the `transition` property. Transforms allow you to rotate, scale, skew, or translate an element. It is a great way to add some interactivity to your site. It's also one of the most performant ways to animate elements.

There is a really good documentation page on transforms where you can play with the different values. You can find it [here](https://developer.mozilla.org/en-US/docs/Web/CSS/transform).

## Transform Values

There are a few different values you can use with the `transform` property. Here are some of the most common ones:

- `rotate()`: Rotates the element by a specified number of degrees.
- `scale()`: Scales the element by a specified number.
- `skew()`: Skews the element by a specified number of degrees.
- `translate()`: Moves the element along the x and y axis.

Let's add some HTML to our example page:

```html
<div class="container">
  <img class="logo" src="./logo.png" alt="" width="200" />
</div>
```

And some CSS:

```css
.container {
  max-width: 600px;
  margin: 130px auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

The logo image should be in the project files.

## Rotate

Let's use the `transform` property to rotate the logo:

```css
.logo {
  transform: rotate(90deg);
}
```

This will rotate it on load. You can also add a transition to make it rotate on hover:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: rotate(90deg);
}
```

Now the logo will rotate 90 degrees when you hover over it.

## Multiple Transforms & Scale

You can also chain multiple transforms together. Let's rotate and scale the logo:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: rotate(90deg) scale(1.5);
}
```

Now the logo will rotate 90 degrees and scale up by 1.5 when you hover over it.

## Transform Origin

You can also use the `transform-origin` property to change the origin of the transform. By default, the origin is the center of the element. Let's change the origin to the top left corner:

```css
.logo {
  transition: transform 0.5s;
  transform-origin: top left;
}

.logo:hover {
  transform: rotate(90deg) scale(1.5);
}
```

Now the logo will rotate and scale from the top left corner.

## Translate

You can also use the `transform` property to move an element along the x and y axis. There are a few different values you can use:

- `translateX()`: Moves the element along the x axis.
- `translateY()`: Moves the element along the y axis.
- `translate()`: Moves the element along the x and y axis.

Let's move the logo along the x axis:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: translateX(100px);
}
```

Now, let's move the logo along the y axis:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: translateY(100px);
}
```

Now, let's move the logo along the x and y axis:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: translate(100px, 100px);
}
```

To go the opposite direction, you can use negative values.

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: translate(-100px, -100px);
}
```

## Skew

You can also use the `transform` property to skew an element. There are a few different values you can use:

- `skewX()`: Skews the element along the x axis.
- `skewY()`: Skews the element along the y axis.
- `skew()`: Skews the element along the x and y axis.

Let's skew the logo along the x axis:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: skewX(30deg);
}
```

Now, let's skew the logo along the y axis:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: skewY(30deg);
}
```

Now, let's skew the logo along the x and y axis:

```css
.logo {
  transition: transform 0.5s;
}

.logo:hover {
  transform: skew(30deg, 30deg);
}
```

These are just simple examples, but you can get really creative with transforms. They are a great way to add some interactivity to your site.
