# Inner Content Styling

Now that we have the base styles in place and the flex alignment set up, we can start styling the inner content.

## Form Styling

Let's add the CSS for the form:

```css
/* Form */
.form-group {
  margin-bottom: 15px;
}

.form-group label {
  display: block;
  margin-bottom: 10px;
  font-size: 14px;
  font-weight: 600;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 15px;
  margin-bottom: 20px;
  border: none;
  border-radius: 5px;
  background: rgba(255, 255, 255, 0.2);
  color: #fff;
  outline: 0;
}

.form-group textarea {
  height: 100px;
  margin-bottom: 10px;
  resize: none;
}
```

All form sections are wrapped in a `form-group` class. Each form field has a label and an input or textarea element. The input and textarea fields have a white background with 80% opacity and white text.

## Button Styling

For the button, add the following CSS:

```css
/* Button */
.btn {
  padding: 15px 20px;
  border: none;
  border-radius: 20px;
  background: #ff4032;
  color: #fff;
  width: 100%;
  font-size: 16px;
  cursor: pointer;
}

.btn:hover {
  background: #ff5c4d;
}
```

The transition is set to change the background color over 0.5 seconds when hovering over the button.

## Text Container Styling

Here is the CSS for the text on the right side:

```css
/* Text Container */
.text-container h1 {
  font-size: 50px;
  margin: 50px 0 20px;
  line-height: 1.2;
}

.text-container p {
  font-size: 18px;
}
```

`margin: 50px 0 20px;` sets the top margin to 50px, the bottom margin to 20px, and the left and right margins to 0. It is the same as doing:

```css
margin-top: 50px;
margin-bottom: 20px;
margin-left: 0;
margin-right: 0;
```

In the next lesson, we will make the page responsive.
