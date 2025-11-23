# Font & Text Properties

In the last lesson, we looked at the `font-family` property in CSS. Now we are going to look at some other properties that can be used to style fonts/text in CSS. These properties allow you to control the size, weight, style, and spacing of text on your website.

Here is a summary of the font/text properties:

- **font-family**: Specifies the font family for text.
- **font-size**: Sets the size of the font.
- **font-weight**: Sets the thickness or boldness of the font.
- **font-style**: Sets the style of the font (normal, italic, or oblique).
- **font-variant**: Controls the usage of small-caps glyphs.
- **line-height**: Sets the height of a line of text.
- **letter-spacing**: Sets the spacing between characters.
- **word-spacing**: Sets the spacing between words.
- **text-align**: Specifies the horizontal alignment of text.
- **text-decoration**: Sets the decoration of text (underline, overline, line-through, etc.).
- **text-transform**: Controls the capitalization of text (uppercase, lowercase, capitalize).
- **text-indent**: Specifies the indentation of the first line of text.
- **text-shadow**: Adds shadow effects to text. We will look at this later.
- **white-space**: Sets how white space inside an element is handled.

Here is the HTML for this lesson:

```html
<div class="container">
  <div>
    <h2>Keep It Sporty</h2>
    <p>Clothing to keep you active and healthy.</p>
    <a href="#">View Collection</a>
  </div>

  <div>
    <h2>Keep It Casual</h2>
    <p>Clothing to keep you comfortable and stylish.</p>
    <a href="#">View Collection</a>
  </div>

  <div>
    <h2>Keep It Formal</h2>
    <p>Clothing to keep you looking sharp.</p>
    <a href="#">View Collection</a>
  </div>
</div>
```

## Font Size

The `font-size` property is used to set the size of the text. You can specify the size in pixels, ems, rems, or percentages. We will go over the different units in a later lesson. For now, we will use pixels (`px`). A pixel is a unit of measurement that is relative to the screen resolution.

The default font size for most browsers is **16px**. Headings are usually larger than the default font size. You can set the font size for different elements in your HTML document. Here is an example of how to set the font size for an `h2` element:

```css
h2 {
  font-size: 26px;
}
```

The default size for an `h2` element is **24px**. In the example above, we are setting the font size to **26px**.

## Font Weight

The `font-weight` property is used to set the weight of the text. You can specify the weight using keywords or numeric values. The most common keywords are `normal`, `bold`, `bolder`, and `lighter`. You can also use numeric values from **100** to **900**.

Here is an example of how to set the font weight for an `h2` element:

```css
h2 {
  font-weight: 500;
}
```

We are setting the weight to a more narrow value of **500**. I like how headings look with a lighter weight in many cases.

## Font Style

The `font-style` property is used to set the style of the text. You can specify the style using keywords like `normal`, `italic`, and `oblique`. The default value is `normal`. Here is an example of how to set the font style for an `h2` element:

```css
h2 {
  font-style: italic;
}
```

I don't use this property often, but it can be useful in some cases where you want to emphasize text.

## Font Property Shorthand

You can combine the `font-size`, `font-weight`, and `font-style` properties into a single `font` property. This is a shorthand property that allows you to set all three properties at once. Here is an example of how to set the font properties for an `h2` element:

```css
h2 {
  font: italic 500 26px;
}
```

## Font Variant

The `font-variant` property is used to control the usage of small-caps glyphs. You can specify the variant using keywords like `normal` or `small-caps`. Here is an example of how to set the font variant for an `h2` element:

```css
h2 {
  font-variant: small-caps;
}
```

I don't use this property often personally.

You can also use the value of `inherit` to inherit the font properties from the parent element.

## Text Decoration

The `text-decoration` property is used to set the decoration of text. You can specify the decoration using keywords like `none`, `underline`, `overline`, `line-through`, and `blink`. Here is an example of how to set the text decoration for an `a` element:

```css
a {
  text-decoration: none;
}
```

This will remove the underline from links. A lot of people, including myself, like to remove the underline from links. This is a common practice in web design.

## Text Transform

The `text-transform` property is used to control the capitalization of text. You can specify the transformation using keywords like `none`, `uppercase`, `lowercase`, and `capitalize`. Here is an example of how to set the text transform for an `h2` element:

```css
h2 {
  text-transform: uppercase;
}
```

This will transform the text to uppercase.

## Text Align

The `text-align` property is used to specify the horizontal alignment of text. You can specify the alignment using keywords like `left`, `right`, `center`, and `justify`. Here is an example of how to set the text alignment for an `p` element:

```css
p {
  text-align: center;
}
```

This will center the text inside the paragraph.

If you wanted to align the entire body of the document, you could do something like this:

```css
body {
  text-align: center;
}
```

## Text Indent

The `text-indent` property is used to specify the indentation of the first line of text. You can specify the indentation using keywords, percentages, or unit values. Here is an example of how to set the text indent for an `h2` element:

```css
h2 {
  text-indent: 20px;
}
```

This will indent the first line of the heading by **20px**.

## Line Height

The `line-height` property is used to set the height of a line of text. You can specify the height using keywords, percentages, or unit values. It is typical to just put a number with no units. In this case, the unit is a multiplier of the font size.

A common value that I like to use for the line-height of the `body` element is **1.6**. This value gives the text some breathing room and makes it easier to read:

```css
body {
  font-family: 'Poppins', sans-serif;
  line-height: 1.6;
}
```

If I increase the font size of the `body` element, the line height will also increase proportionally.

## Letter Spacing

The `letter-spacing` property is used to set the spacing between characters. You can specify the spacing using keywords, percentages, or unit values. Here is an example of how to set the letter spacing for an `h2` element:

```css
h2 {
  letter-spacing: 2px;
}
```

This will increase the spacing between the characters in the heading by **2px**.

## Word Spacing

The `word-spacing` property is used to set the spacing between words. You can specify the spacing using keywords, percentages, or unit values. Here is an example of how to set the word spacing for an `h2` element:

```css
h2 {
  word-spacing: 5px;
}
```

This will increase the spacing between the words in the heading by **5px**.

## White Space

The `white-space` property is used to set how white space inside an element is handled. You can specify the handling using keywords like `normal`, `nowrap`, `pre`, `pre-line`, and `pre-wrap`. Here is an example of how to set the white space for an `p` element:

```css
p {
  white-space: nowrap;
}
```
