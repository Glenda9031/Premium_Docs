# Global Attributes

Global attributes are attributes common to all HTML elements; they can be used on all elements, though they may have no effect on some elements.

We are not going to cover all of them, but we will cover the most common ones.

We have already covered some of these in the previous chapters.

## `class`

This attribute is used to assign a class to an element. Classes are used for grouping elements together for styling or scripting purposes. You can have multiples of the same class.

```html
<h2 class="text-xl">Heading 1</h2>
```

## `id`

This attribute is used to assign a unique identifier to an element. This can be used for targeting it with CSS or JavaScript. The value of the `id` attribute must be unique within a page.

```html
<h2 id="main-heading">Heading 2</h2>
```

## `style`

The `style` attribute is used to add CSS styles to an element. The value of the `style` attribute is a CSS declaration block.

```html
<p style="color: red;">This is a paragraph</p>
```

## `accesskey`

The `accesskey` attribute is used to define a keyboard shortcut to activate or focus an element.

```html
<button accesskey="h" onclick="alert('Home Button Clicked')">Home</button>
```

I know this is not a JavaScript course, but I added an inline click event on this button that will show an alert when clicked. We assigned an accesskey of `h` to the button. You need to hit the following to use the keyboard shortcut:

- **Windows/Linux**: `Alt + Shift + h`
- **Mac**: `Option + Shift + h`

## `title`

The `title` attribute is used to provide additional information about an element. This information is usually displayed as a tooltip when the mouse hovers over the element.

```html
<button accesskey="h" title="Click Me" onclick="alert('Home Button Clicked')">
  Home
</button>
```

## `hidden`

The `hidden` attribute is used to hide an element from the user. The element is still in the DOM, but it is not visible on the page.

```html
<div hidden>This is a hidden div</div>
```

## `data-*`

The `data-*` attributes are used to store custom data on an element. The `*` can be any name you want. You can use this to store data that you can use with JavaScript.

```html
<div data-user-id="1234567890">This is a div</div>
```

## `tabindex`

The `tabindex` attribute is used to define the order in which elements receive focus when the user presses the Tab key. The value of the `tabindex` attribute is a number.

```html
<button tabindex="3">This is a button</button>
<button tabindex="1">This is a button</button>
<button tabindex="2">This is a button</button>
```

## `contenteditable`

The `contenteditable` attribute is used to make an element editable. The value of the `contenteditable` attribute can be `true`, `false`, or `inherit`.

```html
<div contenteditable="true">This is an editable div. Click to edit</div>
```

You would need to add some JavaScript to make the change actually do something and stick.

## `draggable`

The `draggable` attribute is used to make an element draggable. The value of the `draggable` attribute can be `true`, `false`, or `auto`.

```html
<div draggable="true">This is a draggable div</div>
```

`autofocus`

The `autofocus` attribute is used to specify that an element should automatically get focus when the page loads.

```html
<input type="text" autofocus />
```

## `autocapitalize`

The `autocapitalize` attribute is used to specify whether or not the text should be capitalized when typing.

```html
<input type="text" id="name" name="name" autocapitalize />
```
