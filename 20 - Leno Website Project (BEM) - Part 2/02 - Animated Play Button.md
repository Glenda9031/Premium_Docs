# Animated Play Button

We are going to create a button with a play icon in the middle of the image and it will have a pulse animation. This will be done with CSS only.

For now, just so we can see the placing of the button, let's add the text "Play" inside the button.

```html
<button class="preview__video-button">
  <span class="preview__video-play-button">
    <span>Play</span>
  </span>
</button>
```

There will be 4 parts of CSS to this button. The container, the cirlce that the icon is in, the play icon and the animation.

Let's start with the container.

```css
/* Play Button Container */
.preview__video-play-button {
  position: absolute;
  z-index: 10;
  top: 48%;
  left: 50%;
  display: block;
  box-sizing: content-box;
  width: 2rem;
  height: 2.75rem;
  padding: 1.125rem 1.25rem 1.125rem 1.75rem;
  border-radius: 50%;
  cursor: pointer;
  transform: translateX(-50%) translateY(-50%);
}
```

We are positioning it to the middle of the image. You should see the text "Play" in the middle of the image.

Now let's do the circle. We are going to use the `:after` pseudo element to create the circle around the text "Play". Add this to the CSS file:

```css
/* Circle around play button */
.preview__video-play-button:after {
  content: '';
  position: absolute;
  z-index: 1;
  top: 50%;
  left: 50%;
  display: block;
  width: 4.375rem;
  height: 4.375rem;
  border-radius: 50%;
  background: #00c9db;
  transition: all 200ms;
  transform: translateX(-50%) translateY(-50%);
}
```

When we use `:after` we are creating a new element that is a child of the element we are targeting. In this case, we are targeting the `preview__video-play-button` class. We are creating a circle with a background color of `#00c9db`. When you use `:after` you need to add the `content: ''` property. This is because the `:after` pseudo element is used to add content to the element. If you don't add the `content: ''` property, the element will not be created.

You can also delete the text "Play" from the button. Now you should see a circle.

Now let's add the play icon:

```css
/* Triangle inside play button */
.preview__video-play-button span {
  position: relative;
  display: block;
  z-index: 3;
  top: 0.375rem;
  left: 0.25rem;
  width: 0;
  height: 0;
  border-left: 1.625rem solid #fff;
  border-top: 1rem solid transparent;
  border-bottom: 1rem solid transparent;
}
```

Here, we are using the `span` element inside the `preview__video-play-button` class to create the play icon. We are using the `border` property to create the triangle. This can be a bit confusing, especially where the top and bottom are transparent. The border-left creates the vertical line on the left side. It has a specified width and color (1.625rem solid #fff), but since it's only one side, it doesn't create any visible shape yet.

border-top and border-bottom are set to 1rem solid transparent, which means they extend out from the top and bottom of the border-left line. Even though they're set to a solid style, the color is transparent, so they don't visually appear. However, they do extend the area of the border, effectively creating two angled lines extending from the top and bottom of the border-left line.

Now you should see a play icon in the middle of the circle.

Now let's add the animation. We will use the `:before` psuedo selector for this. We need to create a keyframe animation for the pulse effect. Add this to the CSS file:

```css
/* Play button animation */
.preview__video-play-button:before {
  content: '';
  position: absolute;
  z-index: 0;
  top: 50%;
  left: 50%;
  display: block;
  width: 4.75rem;
  height: 4.75rem;
  border-radius: 50%;
  background: #00c9db;
  animation: pulse-border 1500ms ease-out infinite;
  transform: translateX(-50%) translateY(-50%);
}

@keyframes pulse-border {
  0% {
    transform: translateX(-50%) translateY(-50%) translateZ(0) scale(1);
    opacity: 1;
  }
  100% {
    transform: translateX(-50%) translateY(-50%) translateZ(0) scale(1.5);
    opacity: 0;
  }
}
```

Now you should see the pulse effect on the circle.
