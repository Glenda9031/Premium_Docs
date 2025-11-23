# ::before & ::after Pseudo Elements

Now we're going to look at the `::before` and `::after` pseudo elements. These elements allow you to insert content before or after an element. You can use them to add decorative elements to your page. A lot of the time, you'll see them used for things like arrows, icons, or decorative lines. I find them really useful for image overlays because you can add a gradient or color overlay to an image without having to add extra markup. I will give you a very simple example of both in this lesson and we will do an overlay in the next one.

Let's use the following HTML:

```html
<div class="container">
  <h2>World</h2>
  <form>
    <label class="is-required" for="name">Name</label>
    <input type="text" id="name" name="name" required />
  </form>
   <a href="#" class="btn">Click Here</a>
</div>
```

And the following CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  background: #f4f4f4;
  padding: 10px;
}

label {
  display: flex;
  align-items: center;
}

input {
  width: 100%;
  padding: 8px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
  position: relative;
}
```

## The `::before` Selector

The `::before` selector inserts content before the content of an element. You can use it to add decorative elements to your page or to just simply add content. Let's add the word "Hello" before the `h2` element.

Add the following CSS:

```css
h2::before {
  content: 'Hello';
  color: red;
  margin-right: 5px;
}
```

Both the `::before` and `::after` pseudo elements require the `content` property. This property is used to insert content before or after the element. In this case, we are adding the word "Hello" before the `h2` element. We are setting the color to red and adding some margin to the right. There are many times where you'll want to use these for purely decorative purposes but you still need to add the `content` property. You just set it to an empty string.

## The `::after` Selector

Let's make this a little more real-world. We are going to add an asterisk to the `label` element to indicate that the field is required. We can do this by using the `::after` pseudo element.

Add the following CSS:

```css
label.is-required::after {
  content: '*';
  color: red;
  margin-left: 5px;
  font-size: 1.2rem;
}
```

The `::after` selector inserts content after the content of an element. In this case, we are adding an asterisk to the `label` element. We are setting the color to red, adding some margin to the left, and increasing the font size. This is a common pattern for indicating that a field is required. You can also use this to add icons or other decorative elements to your page without having to add extra markup.

We can also position it i other places. Let's add the following:

```css
h2::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 300px;
  height: 400px;
  background: red;
}

```

So we have a big red box and the styling isn't actually on any solid element in the markup. We essentially get 2 extra selectors with these elements.

We could even create some kind of overlay effect when we hover a link. Let's add the following CSS:

```CSS
.btn:after {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255, 255, 255);
  z-index: -1;
  pointer-events: none;
}

.btn:hover:after {
  z-index: 1;
  background: rgba(0, 0, 0, 0.75);
}
```

We are setting a background overlay and on hover, making that overlay black with some transparency. In the next lesson we will create an image overlay, which is something much more useful.

## CSS Reset

Up to this point, we have been using the following syntax for resetting margin, padding and setting the box-sizing property:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

However, it is common to also include the following in a CSS reset:

```css
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

This will also reset the `::before` and `::after` pseudo elements. It is a good practice to include this in your CSS reset. So we will use this from now on.

Both the `::before` and `::after` pseudo elements can use a single colon `:` or a double colon `::`. The double colon is the newer syntax and is recommended. It is more consistent with the newer pseudo elements like `::marker` and `::spelling-error`. The single colon syntax is the older syntax and is still supported for backwards compatibility.
