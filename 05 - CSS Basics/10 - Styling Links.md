# Styling Links

When we styling links, there are multiple states to consider:

- **a:link** - a normal, unvisited link
- **a:hover** - a link when the user mouses over it
- **a:active** - a link the moment it is clicked
- **a:focus** - a link the moment it receives focus
- **a:visited** - a link the user has visited

Normal and hover are really the only two states that are commonly styled. The others are less common, but can be useful in some cases.

Let's use the following HTML:

```html
<p>Check out our <a href="#" class="link-1">latest blog post</a></p>
```

By default, most browsers will display links in blue and underlined. To change this, we can use the following CSS:

```css
a {
  text-decoration: none;
  color: darkblue;
}
```

Of course you can use any color you want, I am just using something that is not the default blue. Now, let's style the other states:

### Hover

This style will be applied when the user hovers over the link:

```css
a:hover {
  color: darkred;
}
```

### Active

This style will be applied when the user clicks on the link:

```css
a:active {
  color: magenta;
}
```

### Focus

This style will be applied when the link receives focus:

```css
a:focus {
  color: darkorange;
}
```

### Visited

This style will be applied to links that the user has already visited:

```css
a:visited {
  color: darkgreen;
}
```

It isn't that typical to style visited links differently, but it can be useful in some cases.
