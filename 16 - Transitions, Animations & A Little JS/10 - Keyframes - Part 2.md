# Keyframes - Part 2 (CSS Loader Animation)

We are going to look at keyframes a bit more in this lesson. In the last lesson, we used `to` and `from` to create keyframes. You can also use percentages to create keyframes. This is useful when you want to create more complex animations and have more than just the start and end states.

We are going to create a CSS loader that uses a couple different animations to create a cool effect of spinning and bouncing.

Let's use the following HTML:

```html
<div class="container">
  <div class="loader"></div>
</div>
```

And the following base CSS:

```css
.container {
  height: 100vh;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.loader {
  width: 80px;
  height: 80px;
  position: relative;
  background: #3498db;
}
```

First I just want to show you how to use percentages in keyframes. We are going to create a simple animation that will make the loader spin.

Add the following CSS:

```css
@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

This is a simple keyframe that will rotate the loader 360 degrees. Let's apply this animation to the loader:

```css
.loader {
  // ...
  animation: spin 2s linear infinite;
}
```

You should see a spinning square. We only have two points in the keyframe so it is essentially the same as using `to` and `from`. Let's add another point to the keyframe to make the loader change color.

Add the following CSS:

```css
@keyframes spin {
  0% {
    transform: rotate(0deg);
    background: #3498db;
  }
  50% {
    background: #e74c3c;
  }
  100% {
    transform: rotate(360deg);
    background: #3498db;
  }
}
```

Now, the loader will change color halfway through the animation. You can add as many points as you want to create more complex animations.

That's how you use percentages.

Now let's create the loader. I want to have two circles that spin around each other.

Let's first remove the background property from the loader, because we are going to use the ::before and ::after pseudo-elements to create the circles. I still want to keep the rest including the spinning animation.

```css
.loader {
  width: 80px;
  height: 80px;
  position: relative;
  animation: spin 2s linear infinite;
}
```

Change the spin keyframe to the following:

```css
@keyframes spin {
  100% {
    transform: rotate(360deg);
  }
}
```

This will keep the spinning animation. You won't see anything at the moment because we removed the background. Let's add the circles.

Add the following CSS:

```css
.loader::before,
.loader::after {
  content: '';
  position: absolute;
  top: 0;
  left: 35px;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background: #3498db;
}
```

What we are doing here is creating two circles that are 30px in diameter. We are positioning them absolutely to the loader. They are both on top of each other at the moment. Let's move the second circle to the right.

```css
.loader::after {
  left: -35px;
  background: #e74c3c;
}
```

Now you should see both circles spinning around each other. You can play around with the sizes and colors to create different effects.

Let's add a bounce animation to the circles. We are going to use percentages to create this animation.

Add the following CSS:

```css
@keyframes bounce {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-30px);
  }
}
```

At 0% and 100% the circles will be in their normal position. At 50% they will move up 30px. Let's apply this animation to the circles:

```css
.loader::before,
.loader::after {
  // ...
  animation: bounce 2s infinite ease-in-out;
}
```

That gives it a bit more life. If you comment out the spin animation, you will see the circles bouncing up and down.

Hopefully, this gives you a better understanding of keyframes and how you can use them to create more complex animations. Play around with the values to see what you can come up with.
