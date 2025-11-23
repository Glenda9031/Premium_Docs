# 3D Rotating Cube Mini-Project

In this lesson, we are going to create a 3D rotating cube. This is a fun little project that will help you understand how to use both keyframes and CSS transforms to create 3D effects.

Let's use the following HTML:

```html
<div class="container">
  <div class="cube">
    <div class="face front">Front</div>
    <div class="face back">Back</div>
    <div class="face right">Right</div>
    <div class="face left">Left</div>
    <div class="face top">Top</div>
    <div class="face bottom">Bottom</div>
  </div>
</div>
```

## Container

Here is the container CSS:

```css
.container {
  perspective: 1000px;
  width: 200px;
  height: 200px;
  margin: 50px auto;
}
```

Remember, the `perspective` property is what gives the 3D effect. The higher the value, the more pronounced the 3D effect will be.

## Cube

Now let's style the cube:

```css
.cube {
  position: relative;
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
}
```

We are just setting the width and height to be 100% of the container, which is 200px by 200px. The `transform-style` property is set to `preserve-3d` so that the children of the cube will also be in 3D space.

## Faces

Now let's style the face class, which is on each side of the cube:

```css
.face {
  position: absolute;
  width: 200px;
  height: 200px;
  line-height: 200px;
  text-align: center;
  font-size: 20px;
}
```

This positions the text in the center of each face. The `line-height` property is set to 200px so that the text is vertically centered.

Let's style the front face:

```css
.front {
  background-color: #f00;
  transform: translateZ(100px);
}
```

The `translateZ` function moves the face along the z-axis. Since the cube is 200px by 200px, we are moving the front face 100px away from the viewer. X is left and right, Y is up and down, and Z is forward and backward.

Let's style the back face:

```css
.back {
  background-color: #00f;
  transform: rotateY(180deg) translateZ(100px);
}
```

The `rotateY` function rotates the face around the y-axis. We are rotating it 180 degrees so that it is facing the opposite direction. We then move it along the z-axis.

You won't see any changes yet because the back face is behind the front face.

## Animation

Before we do the rest of the faces, let's add an animation to the cube so we can see what happens at this point.

Here is the keyframes animation:

```css
@keyframes rotateCube {
  0% {
    transform: rotateY(0deg);
  }
  100% {
    transform: rotateY(360deg);
  }
}
```

We are simply rotating the cube around the y-axis from 0 to 360 degrees.

Now apply it to the cube:

```css
.cube {
  // ...
  animation: rotateCube 5s infinite linear;
}
```

It should start spinning and you will see the front and back faces.

Let's do the rest of the faces.

```css
.right {
  background-color: #0f0;
  transform: rotateY(90deg) translateZ(100px);
}

.left {
  background-color: #ff0;
  transform: rotateY(-90deg) translateZ(100px);
}

.top {
  background-color: #0ff;
  transform: rotateX(90deg) translateZ(100px);
}

.bottom {
  background-color: #f0f;
  transform: rotateX(-90deg) translateZ(100px);
}
```

## Rotate on Both Axes

If you want to rotate the cube on both the x and y axes, you can do so by adding `rotateX` and `rotateY` functions to the keyframes animation.

```css
@keyframes rotateCube {
  0% {
    transform: rotateY(0deg) rotateX(0deg);
  }
  100% {
    transform: rotateY(360deg) rotateX(360deg);
  }
}
```

Now the cube will rotate on both axes.
