# Creating Transitions

Now we will create a few transitions. Remember, the syntax is:

```bash
  transition: property duration timing-function delay;
```

Let's use the following HTML:

```html
<div class="container">
  <button class="btn">Hover Me</button>
</div>
```

And the intial CSS:

```css
body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 600px;
  margin: 30px auto;
}
```

## Button Hover

We will create a simple hover effect on the button. When the button is hovered over, the background color will change. Let's do it without the transition first:

```css
.btn {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn:hover {
  background-color: #0056b3;
}
```

If you hover the button, it will change color instantly. Let's add a transition to make it smoother:

```css
.btn {
  // Other styles
  transition: background-color 0.8s;
}
```

Now the color will change smoothly over 0.8 seconds. You can adjust the duration to make it faster or slower. The only arguments that are required are the property and duration. The timing function and delay are optional.

Let's add a delay of 2 seconds:

```css
.btn {
  // Other styles
  transition: background-color 0.8s 2s;
}
```

Now it won't change color for 2 seconds after hovering.

You can also add the timing function. Let's use `ease-in-out` and remove the delay:

```css
.btn {
  // Other styles
  transition: background-color 0.8s ease-in-out;
}
```

The timing function will make the transition start slow, speed up, and then slow down again. You can use `ease`, `ease-in`, `ease-out`, `linear`, `step-start`, `step-end`, and `steps()`.

## Multiple Properties

You can also transition multiple properties. Let's add a transition to the text color as well:

```css
.btn {
  // Other styles
  transition: background-color 0.8s ease-in-out, color 0.8s ease-in-out;
}

.btn:hover {
  color: yellow;
  background-color: #0056b3;
}
```

Now both the background color and text color will transition over 0.8 seconds.

If you want the same transition for both properties, you can do this:

```css
.btn {
  // Other styles
  transition: background-color, color 0.8s ease-in-out;
}
```

## Transition All Properties

You can also transition all properties with the following:

```css
.btn {
  // Other styles
  transition: all 0.8s ease-in-out;
}
```

This will transition all properties over 0.8 seconds.

Let's transition some other properties. Let's add a width to the hover:

```css
.btn:hover {
  color: yellow;
  background-color: #0056b3;
  width: 400px;
}
```

If you hover, the width changes but it's instant. This is because we did not set a width to begin with. Let's add a width to the button:

```css
.btn {
  // Other styles
  width: 200px;
}
```

Now the width will transition over 0.8 seconds.

We could transition the border radius as well:

```css
.btn:hover {
  // Other styles
  border-radius: 50px;
}
```

So you see, you can transition just about anything that is numeric or has multiple states. Just remember to set the initial value.

One of the coolest things to use with transtions is the `transform` property. We will look at that in the next lesson.
