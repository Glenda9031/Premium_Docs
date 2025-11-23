# Colors

We can use colors for all kinds of things in web development. We can use them to set the background color of an element, the text color, the border color, and more. We can use color names, hex codes, RGB, RGBA, HSL, and HSLA values to set colors in CSS.

Here is the HTML for this lesson:

```html
<div class="container">
  <div class="card">
    <h2 class="sporty">Keep It Sporty</h2>
    <p>Clothing to keep you active and healthy.</p>
    <a href="#">View Collection</a>
  </div>

  <div class="card">
    <h2 class="casual">Keep It Casual</h2>
    <p>Clothing to keep you comfortable and stylish.</p>
    <a href="#">View Collection</a>
  </div>

  <div class="card">
    <h2 class="formal">Keep It Formal</h2>
    <p>Clothing to keep you looking sharp.</p>
    <a href="#">View Collection</a>
  </div>
</div>
```

## Color Names

There are 147 color names that are supported by all browsers. Let's set the text color of the `h2` classes to some color names:

```css
/* Class Selectors */
.sporty {
  color: red;
}

.casual {
  color: blue;
}

.formal {
  color: brown;
}
```

We are setting the text color of the `h2` elements with the classes `sporty`, `casual`, and `formal` to `red`, `blue`, and `brown`, respectively.

## Hex Codes

Hex codes are a way to represent colors in CSS. They are a combination of six characters that represent the amount of red, green, and blue in a color. Hex codes start with a `#` followed by six characters.

We tend to use black and white a lot, the hex value for black is `#000000` and the hex value for white is `#ffffff` however, when you have a color that is all the same, you can use a shorthand 3-character hex code. For example, the hex code for black can be written as `#000`, and the hex code for white can be written as `#fff`.

Let's set the `body` background color to white and the text to black:

```css
body {
  font-family: Arial, sans-serif;
  background-color: #ffffff;
  /* We can also use the shorthand */
  /* background-color: #fff; */
  /* For the background color, you can also just use the `background` property */
  /* background: #fff; */
  color: #000000;
  /* We can also do */
  /* color: #000; */
}
```

Let's set the `h2` elements to some hex codes:

```css
.sporty {
  color: #e04553; /* A dark red */
}

.casual {
  color: #0d4ba3; /* A dark blue */
}

.formal {
  color: #512b22; /* Brown */
}
```

## RGB and RGBA

RGB stands for red, green, and blue. We can use RGB values to set colors in CSS. RGB values range from 0 to 255. We can also use RGBA values to set colors with an alpha value. The alpha value ranges from 0 to 1. This will give it a transparency effect.

Here are some examples on the `card` class:

```css
.card {
  /* RGB Values */
  background-color: rgb(0, 0, 0); /* black */
  background-color: rgb(255, 255, 255); /* white */
  background-color: rgb(255, 0, 0); /* red */
  background-color: rgb(0, 255, 0); /* green */
  background-color: rgb(0, 0, 255); /* blue */
  background-color: rgb(173, 216, 230); /* light blue */

  /* RGBA Values */
  background-color: rgba(0, 0, 0, 0.5); /* black with 50% opacity */
}
```

## HSL and HSLA

HSL stands for hue, saturation, and lightness. This is not as common as hex, color names or rgb. I almost never use this. The hue value ranges from 0 to 360, the saturation value ranges from 0% to 100%, and the lightness value ranges from 0% to 100%. We can also use HSLA values to set colors with an alpha value. The alpha value ranges from 0 to 1. This will give it a transparency effect.

Here are some examples on the `card` class:

```css
.card {
  /* HSL Values */
  background-color: hsl(0, 100%, 50%); /* red */
  background-color: hsl(240, 100%, 50%); /* blue */
  background-color: hsl(120, 100%, 50%); /* green */
  background-color: hsl(180, 100%, 50%); /* cyan */
  background-color: hsl(60, 100%, 50%); /* yellow */
  background-color: hsl(0, 0%, 0%); /* black */
  background-color: hsl(0, 0%, 100%); /* white */

  /* HSLA Values */
  background-color: hsla(0, 100%, 50%, 0.5); /* red with 50% opacity */
}
```

Most of the time we will be using hex codes because that is my preference. You can use whatever you like. I just find hex codes to be the most readable and easy to use. If I need transparency for something like a hero overlay, I will use RGBA values.

## Opacity

I figured that I would mention opacity here. You can set the opacity of an element using the `opacity` property. Just like the alpha value in RGBA, the value ranges from 0 to 1. Here is an example:

```css
.card {
  opacity: 0.5; /* 50% opacity */
}
```

This will make the `card` class 50% transparent. This includes everything in it including the text. If you only want the background to be transparent, you can use RGBA values on the `background-color` property.
