# Transitions Explained

Transitions are a way to change property values smoothly (over a given duration). They are used to make the user experience more engaging and interactive. When you hover over a button and it changes color, that's a transition. When you hover over an image and it zooms in, that's a transition.

## Transition vs Animation

Transitions and animations are similar in that they both change property values over time. However, they differ in how they are triggered and controlled.

- **Transitions**: Transitions are triggered by a change in state, such as hovering over an element. So it is always from one state to another. They are controlled by the browser and are defined using the `transition` property in CSS.
- **Animations**: Animations are triggered by an event or happen automatically on a loop. They are controlled by keyframes and are defined using the `@keyframes` rule in CSS.

## Animatable Properties

There are a ton of properties that can be animated using transitions. Here are some common ones:

- `background-color` - Changes the background color of an element.
- `color` - Changes the text color of an element.
- `opacity` - Changes the transparency of an element.
- `width` - Changes the width of an element.
- `height` - Changes the height of an element.
- `transform` - Changes the position, rotation, scale, and skew of an element. This is a very common and powerful property to animate.
- `box-shadow` - Changes the shadow of an element.

There are many more properties that can be animated but these are some really common ones.

## Transition Property

The `transition` property is used to define the transition effect for an element. It has the following syntax:

```css
transition: property duration timing-function delay;
```

- `property`: The CSS property you want to transition.
- `duration`: The duration of the transition in seconds (or milliseconds).
- `timing-function`: The speed curve of the transition. This can be `ease`, `linear`, `ease-in`, `ease-out`, or `ease-in-out`.
- `delay`: The delay before the transition starts.

Here's an example:

```css
button {
  transition: background-color 0.5s ease;
}
```

To see it in action, you can hover over it because that's when the transition will happen. You can also use JavaScript to trigger transitions.

In the next lesson, we'll create some transitions.
