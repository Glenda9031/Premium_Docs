# Keyframes - Part 1

We looked at the `transition` property, which is one way of animating elements. Now we are going to look at CSS keyframes, which is another way of animating elements. Keyframes allow you to create complex animations by defining the start and end points of an animation. You can also define multiple points in between. If you have a width of 600px, you have every point from 0px to 600px. You can define the width at each point.

Keyframes are defined using the `@keyframes` rule. You can define multiple keyframes in a single `@keyframes` rule. Each keyframe is defined by a percentage value, which represents the progress of the animation. You can also use the `from` and `to` keywords to represent the start and end points of the animation.

Let's look at a simple example of animating the width of an element.

Here is the HTML:

```html
<div class="container">
  <div class="box"></div>
</div>
```

And the CSS:

```css
.container {
  max-width: 1100px;
  margin: 30px auto;
}

.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
}
```

We are going to animate the width of the `.box` element. We are going to make it grow from 100px to 500px.

## Defining Keyframes with `@keyframes`

Add the following CSS:

```css
@keyframes animate1 {
  from {
    width: 100px;
  }

  to {
    width: 500px;
  }
}
```

We are defining a keyframe called `animate1`. The `from` keyword represents the start of the animation, and the `to` keyword represents the end of the animation. We are changing the width of the `.box` element from 100px to 500px.

## `animation` Property

Now we need to apply the keyframes to the `.box` element. We can do this using the `animation` property.

Add the following CSS:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  animation: animate1 2s;
}
```

When you load th page, the `.box` element will grow from 100px to 500px over 2 seconds.

## `animation-iteration-count`

You can also set the `animation-iteration-count` property to make the animation repeat a certain number of times.

Add the following CSS:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  animation: animate1 2s;
  animation-iteration-count: 3;
}
```

Now the animation will repeat 3 times. You can also use the `infinite` keyword to make the animation repeat indefinitely.

## `animation-fill-mode`

You can set the `animation-fill-mode` property to determine what styles are applied to the element before and after the animation. Right now, it will jump back to the original width after the animation is complete. You can set it to `forwards` to keep the final style of the animation.

Comment out the `animation-iteration-count` property because we don't want the animation to repeat.

Add the following CSS:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  animation: animate1 2s;
  animation-fill-mode: forwards;
}
```

Now it stays at 500px after the animation is complete.

## `animation-delay`

You can also add a delay to the animation using the `animation-delay` property:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  animation: animate1 2s;
  animation-fill-mode: forwards;
  animation-delay: 3s;
}
```

Now the animation will start after 3 seconds.

## `animation-direction`

You can also set the `animation-direction` property to make the animation play in reverse:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  animation: grow 2s;
  animation-iteration-count: infinite;
  animation-direction: reverse;
}
```

Now the animation will play in reverse.

## `animation-timing-function`

You can also set the `animation-timing-function` property to change the speed of the animation. There are a few different values you can use:

- `ease`: Slow at the beginning and end, but fast in the middle.
- `linear`: The same speed from start to finish.
- `ease-in`: Starts slow and speeds up.
- `ease-out`: Starts fast and slows down.
- `ease-in-out`: Starts slow, speeds up, and then slows down.
- `cubic-bezier()`: Define your own values.

Let's set the speed to a bit longer, and use the `ease-in` timing function:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  animation: animate1 5s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in;
}
```

You'll see that it starts off slow and speeds up. If you change it to `ease-out`, it will start fast and slow down.

## Multiple Properties

Let's also animate the color of the `.box` element. We are going to change the color from `lightcoral` to `lightblue`.

We'll change the name of the animation as well:

```css
@keyframes animate1 {
  from {
    width: 100px;
    background-color: lightcoral;
  }

  to {
    width: 500px;
    background-color: lightblue;
  }
}
```

Now it will grow and change color.

Let's move it on the page from one place to the other. First, set it to `position: absolute` and center it on the page:

```css
.box {
  // ...
  position: absolute;
}
```

Now we are going to move it from the top left corner to the bottom right corner.

```css
@keyframes animate1 {
  from {
    width: 100px;
    background-color: lightcoral;
    top: 0;
    left: 0;
  }

  to {
    width: 500px;
    background-color: lightblue;
    top: 100vh;
    left: 100vw;
  }
}
```

Now it will go from the top left corner to the bottom right corner in 2 seconds. You can increase the time to make it slower.

That's a basic overview of CSS keyframes. We'll dig in a bit more in the next lesson.
