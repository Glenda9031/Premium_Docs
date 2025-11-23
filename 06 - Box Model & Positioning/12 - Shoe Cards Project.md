# Shoe Cards Project

In this project, we will use the stuff that we've learned to create the following content cards:

<img src="../images/shoe-cards.png" alt="Shoe Cards" width="500"/>

We will use properties that have to do with the box model, such as `padding`, `margin`. We'll use colors as well as background images.

For the most part, any project that we do will always be stuff that we went over. I'm not going to include flexbox or transitions or anything like that because we haven't covered it yet.

### Images

There are 3 images that you need for this project. You can find them in the HTML-CSS-Sandbox in the corresponding section/folder.

### HTML

Let's start with the HTML, which is pretty simple:

```html
<div class="container">
  <div class="card card-sporty">
      <h2>Keep It Sporty</h2>
      <p>Shoes to keep you active and healthy.</p>
      <a href="#">View Collection</a>
   
  </div>
  <div class="card card-casual">
      <h2>Keep It Casual</h2>
      <p>Shoes to keep you comfortable.</p>
      <a href="#">View Collection</a>
  </div>
  <div class="card card-formal">
      <h2 class="formal">Keep It Formal</h2>
      <p>Shoes to keep you looking sharp.</p>
      <a href="#">View Collection</a>
  </div>
</div>
```

We have a container with three cards. Each card has a title, a description, and a link to view the collection.

They each have a `.card` class for regular styling and a `.card-sporty`, `.card-casual`, and `.card-formal` class for specific styling.

### Base CSS

Let's add some base CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Roboto', sans-serif;
  background-color: #d9e2e8;
}

.container {
  max-width: 600px;
  margin: 100px auto;
  padding: 0 20px;
}
```

We're setting the font family to Roboto, a sans-serif font. We're setting the background color to a light blue and centering the 600px container and adding a bit of padding.

<img src="../images/shoe-cards-1.png" alt="Shoe Cards" width="500"/>

### Card Styling

Let's style the card itself:

```css
.card {
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  margin: 20px 0;
  padding: 20px 20px 30px;
}
```

We're setting the background color to white, adding a border radius, a box shadow, some margin, and padding.

<img src="../images/shoe-cards-2.png" alt="Shoe Cards" width="500"/>

### Card Content Styling

Let's do the heading and paragraph:

```css
.card h2 {
  font-size: 27px;
  margin-bottom: 20px;
}

.card p {
  font-size: 18px;
  font-weight: 500;
  color: #333;
  margin-bottom: 30px;
}
```

### Heading Colors

I want the headings to be different colors. Each card has a specific class, so we will use those classes to style the headings:

```css
/* Heading colors */
.card-sporty h2 {
  color: #e04553;
}

.card-casual h2 {
  color: #0d4ba3;
}

.card-formal h2 {
  color: #512b22;
}
```

<img src="../images/shoe-cards-3.png" alt="Shoe Cards" width="500"/>

### Links

Let's style the links like buttons. This is a very common practice:

```css
.card a {
  text-decoration: none;
  color: #fff;
  background-color: #333;
  padding: 10px 20px;
  border-radius: 5px;
  font-size: 18px;
}

.card a:hover {
  opacity: 0.9;
}
```

### Link Colors

I also want the links to be different colors:

```css
/* Link colors */
.card-sporty a {
  background-color: #e04553;
}

.card-casual a {
  background-color: #0d4ba3;
}

.card-formal a {
  background-color: #512b22;
}
```

<img src="../images/shoe-cards-4.png" alt="Shoe Cards" width="500"/>

### Background Images

Finally, let's add the background images:

```css
/* Background Images */
.card-sporty {
  background: #fff url('./images/sporty.png') no-repeat center right/200px;
}

.card-casual {
 background: #fff url('./images/casual.png') no-repeat center right/200px;
}

.card-formal {
  background: #fff url('./images/formal.png') no-repeat center right/200px;
}
```

We have three images in the images folder. We're setting the background color to white and adding the image to the right of the card and setting the size to 200px.

<img src="../images/shoe-cards.png" alt="Shoe Cards" width="500"/>

In the real world, I would probably use an inline image and align it with flexbox. But for this project, we're just using background images, which is also fine.
