# 3D Trandforms (3D Card Mini-Project)

We looked at the basics of transforms. We can also use them to create 3D effects. Let's create a 3D card flip effect.

Let's add the HTML:

```html
<div class="container">
  <div class="card-container">
    <div class="card">
      <div class="front">Front Side</div>
      <div class="back">Back Side</div>
    </div>
  </div>
</div>
```

And some base CSS:

```css
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

In the HTML, we have a regular container to position the content. We have a card container and a card. The card has a front and back side. The front side will be visible by default and when we hover over it, it will flip to the back side.

The container just centers the card on the page.

Let's style the card and card container:

```css
.card-container {
  margin-top: 50px;
  text-align: center;
}

.card {
  width: 200px;
  height: 300px;
  position: relative;
}
```

The card container is just adding some margin to the top and centering the text. The card is given a width and height and is set to `position: relative`.

## Front and Back Styles

Let's add the background colors and make it look like a card. The front and back side will have different colors.

```css
.front {
  background-color: #3498db;
  color: white;
  line-height: 300px;
}

.back {
  background-color: #2ecc71;
  color: white;
  line-height: 300px;
}
```

## Positioning

We want to position the front and back side of the card on top of each other. We can do this by setting the front side to `position: absolute` and the back side to `position: absolute` as well:

```css
.front,
.back {
  position: absolute;
  width: 100%;
  height: 100%;
}
```

Right now, you'll only see the back side of the card because they are on top of each other.

## Rotate

We have a few rotate transforms that we can use. We can rotate on the X, Y, or Z axis. We can also rotate in 3D space. We want it to flip on the Y-axis, so we will be using the `rotateY` transform.

Let's add the following CSS:

```css
.card:hover {
  transform: rotateY(180deg); /* Flip the card on hover */
}
```

It should flip to the back side when you hover over it.

## Transition

Right now, there is no transition. It just goes from one side to the other instantly. We can add a transition to make it smooth.

```css
.card {
  // ...
  transition: transform 0.5s ease; /* Smooth transition */
   transform-style: preserve-3d; /* Preserve 3D transformations */
}
```

## Hide Back Side

We want the back side to be hidden by default. We can do this by rotating the card 180 degrees on the Y-axis:

```css
.back {
  transform: rotateY(180deg); /* Hide the back side */
}
```

Then we can set the `backface-visibility` property to `hidden` for both the front and back side. This property hides the backface when the element is flipped in 3D space.

```css
.front,
.back {
  // ...
  backface-visibility: hidden; /* Hide backface when flipped */
}
```

Now you should see the back side of the card when you hover over it.

## Perspective

To make the 3D effect more realistic, we can add perspective to the card container. This will make it look like the card is flipping in 3D space.

Add the `perspective` property to the card container:

```css
.card-container {
  // ...
  perspective: 1000px; /* Add perspective */
}
```

`1000` is a good value for the perspective. You can adjust it to your liking. The perspective property defines how far the object is away from the user. So, a lower value will result in a more intensive 3D effect than a higher value. Try setting it to `100` and you will see the difference.

Now the card will flip on hover with a smooth transition.
