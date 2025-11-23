# CSS Custom Properties

CSS custom properties are a way to define properties that can be reused throughout your CSS. They are also known as CSS variables.

These come in handy because sometimes you have something like a color repeated throughout your CSS and you want to change it in one place. This is where custom properties come in. Even if you only have one instance of a property, it can be helpful to define it as a custom property for clarity.

Let's use the following HTML:

```html
<header>
      <h1>Custom Properties</h1>
</header>
<div class="container">
  <div class="box box-1">
    <h3>Lorem, ipsum dolor.</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
      voluptates, quas, quos, quod quae quibusdam quia quidem voluptate
      voluptatum doloribus quae.
    </p>
  </div>
  <div class="box box-2">
    <h3>Lorem, ipsum dolor.</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
      voluptates, quas, quos, quod quae quibusdam quia quidem voluptate
      voluptatum doloribus quae.
    </p>
  </div>
  <div class="box  box-3">
    <h3>Lorem, ipsum dolor.</h3>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam
      voluptates, quas, quos, quod quae quibusdam quia quidem voluptate
      voluptatum doloribus quae.
    </p>
  </div>
</div>
```

And the following base CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
}

header {
  background-color: lightblue;
  padding: 20px 0;
  text-align: center;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  display: flex;
  gap: 20px;
}

.box {
  width: 100%;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
```

## Scope

When you create a custom property, you create it within a scope. Let's say that we wanted this to only apply to a class of `.container` and everything within it. We would do this:

```css
.container {
  --primary-color: lightblue;
}
```

The custom property syntax is a bit different. It starts with `--` and then the name of the property. In this case, we are setting the primary color to `lightblue`. I could use any property/variable name that I want.

This will only apply to the `.container` class and everything within it.

## Usage

To use a custom property is also a bit weird. You use the `var()` function. So let's change the background color of the header and box 1 to the primary color:

```css
header {
  //...
  background-color: var(--primary-color);
}

.box-1 {
  background-color: var(--primary-color);
}
```

Notice it only works for box 1 because we set the custom property on the `.container` class.

## Global Properties

Usually, we set global custom properties by setting the `:root` scope, which pertains to the `html` element. So let's move this right below the reset and change it to:

```css
:root {
  --primary-color: lightblue;
}
```

Now we can use it anywhere. It should work for both the header and box 1.

This is convenient because you can have 20 instances of the same color and only need to change it in one place.

Even if you don't have a bunch of instances of a property, it can be helpful for clarity. For example, if you have a color that is only used once, you can define it as a custom property to make it clear what it is.

Let's add colors for the other boxes:

```css
:root {
  --primary-color: lightblue;
  --secondary-color: lightcoral;
  --tertiary-color: lightgreen;
}
```

And use them in the boxes:

```css
.box-1 {
  background-color: var(--primary-color);
}

.box-2 {
  background-color: var(--secondary-color);
}

.box-3 {
  background-color: var(--tertiary-color);
}
```

You don't even have to put the entire value in the variable value. For instance, maybe we just want the shadow opacity of the shadow:

```css
:root {
  //..
  --shadow-opacity: 0.5;
}
```

And use it like this:

```css
.box {
  //...
  box-shadow: 0 0 10px rgba(0, 0, 0, var(--shadow-opacity));
}
```

You may put something like the width of the container or maybe even have multiple container widths:

```css
:root {
  //...
  --container-width: 600px;
  --container-width-large: 1100px;
}

.container {
  max-width: var(--container-width);
}

.container-lg {
  max-width: var(--container-width-large);
}
```

This is a simple example, but you can see how this can be useful.

We will use custom properties in some upcoming projects.
