# Features Mobile

We have the features section looking good on desktop, but we need to make sure it looks good on mobile as well. Let's go down to the `@media` query for `992px` and add the following styles:

```css
/* Features */
.features__grid {
  grid-template-columns: 1fr;
}

.features__grid-column {
  gap: 3rem;
}

.features__grid-column-left,
.features__grid-column-right {
  order: 2; /* Set the order of left and right grid columns */
  margin-bottom: 2rem;
}

.features__grid-column-center {
  order: 1; /* Set the order of the center grid column */
  margin-bottom: 3rem;
}

.features__grid-item {
  text-align: center;
  flex-direction: column-reverse;
  max-width: 400px;
}

.features__grid-column-right .features__grid-item{
  text-align: center;
  flex-direction: column-reverse;
}

.features__grid-item-icon {
  margin: 0 auto;
}

.features__grid-column-center img {
  max-width: 300px;
}
```

First, we stacked the grid items into a single column. Then we reordered the grid items to make sure the center column is on top (the image). We also centered the list items and icons, and set a max-width for the list columns.

Since we aligned the right side column to the right on desktop, we need to make sure it's centered on mobile. We set the text-align and also made the flex-direction column-reverse so that the icon is on top and the text is below it.

Finally, we set a max-width for the center image to make sure it doesn't overflow the container.
