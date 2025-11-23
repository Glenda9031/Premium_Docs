# CSS Custom Properties

Since we are using a color for hovered and current links as well as a utility class, we can create a custom property for it.

We will add the following to the `:root` selector at the top of the CSS file:

```css
:root {
  --primary-color: #fcf5e9;
}
```

To use this, we will go to the following CSS:

```css
.main-menu a:hover {
  background: #fcf5e9;
}

.main-menu .current {
  background: #fcf5e9;
  font-weight: bold;
}
```

and replace with this:

```css
.main-menu a:hover {
  background: var(--primary-color);
}

.main-menu .current {
  background: var(--primary-color);
  font-weight: bold;
}
```

There is one other place to use this and that is the `.bg-primary` class:

```css
.bg-primary {
  background: var(--primary-color);
  padding: 0 0.5rem;
}
```

So now, try changing the variable to `red` temporarily. You see, we only need to change it in one place.

## Container Sizes

We have 3 different container widths. Let's add a variable for each:

```css
:root {
  --primary-color: #fcf5e9;
  --container-normal: 1100px;
  --container-narrow: 900px;
  --container-wide: 1400px;
}
```

Now in the CSS, let's change the container widths to use these properties/variables:

```css
.container {
  max-width: var(--container-normal);
  margin: 0 auto;
  padding: 0 1.5rem;
}

.container-lg {
  max-width: var(--container-wide);
}

.container-sm {
  max-width: var(--container-normal);
}
```

So now, if you want to change the sizing, you have it available right at the top of the file.

If you want to add other styles as custom properties, feel free. It's a great way to keep your CSS organized and easy to maintain.
