# Flexbox Order

This is going to be a short lesson. I just want to show you how we can order our flex items in a different way than they appear in the HTML.

Let's use this HTML:

```html
<div class="flex-container">
  <div class="flex-item item-1">Item 1</div>
  <div class="flex-item item-2">Item 2</div>
  <div class="flex-item item-3">Item 3</div>
  <div class="flex-item item-4">Item 4</div>
  <div class="flex-item item-5">Item 5</div>
  <div class="flex-item item-6">Item 6</div>
</div>
```

and this CSS:

```css
body {
  font-family: Arial, sans-serif;
}

.flex-container {
  display: flex;
}

.flex-item {
  background-color: coral;
  border: 1px solid black;
  padding: 30px;
  flex: 1;
}
```

## `row-reverse` and `column-reverse`

We can use the `row-reverse` and `column-reverse` values for the `flex-direction` property to reverse the order of the flex items.

```css
.flex-container {
  display: flex;
  flex-direction: row-reverse; /* or column-reverse */
}
```

## `order`

We can use the `order` property to change the order of the flex items. The default value is `0`. We can use positive or negative values.

```css
.item-1 {
  order: 2;
}

.item-2 {
  order: 1;
}

.item-3 {
  order: 3;
}

.item-4 {
  order: 6;
}

.item-5 {
  order: 5;
}

.item-6 {
  order: 4;
}
```

So your HTML is in tact, but the order of the items is different.
