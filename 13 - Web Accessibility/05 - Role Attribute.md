# The Role Attribute

In this lesson, we will learn about the `role` attribute and how it can be used to make our HTML more accessible and assign semantic meaning. The `role` attribute is used to define the purpose of an element or section. It is especially useful for non-semantic elements like `<div>` and `<span>`. The `role` attribute can be used to provide additional information to assistive technologies like screen readers.

  The role attribute doesn't start with `aria-` but it is part of the ARIA attributes, which stands for **Accessible Rich Internet Applications** and is a set of attributes and roles that make web content more accessible. We'll look into these more in the next video.

ARIA roles are added to HTML elements using `role="role type"`, where role type is the name of a role in the ARIA specification.

You definitley do not want to overuse the `role` attribute. It is best to use it only when it is necessary. If you can use a native HTML element or attribute with the semantics and behavior already built in, instead of re-purposing an element and adding an ARIA role, that is what you should do. Having too many roles creates confusion or "noise" for users of assistive technologies.

There may be cases where you want an image as a button for example. You can add the role of button to that image and in the screen reader, it will be announced as a button. It's important to know that adding the role doesn't make it function like a button. That's up to you to add an event listener and so on. All the attribute does is let the user know it's a button.

## Predefined Roles

There are many predefined roles in the ARIA specification. There are specific categories as well. You can see all roles at https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles.

Here are the role categories:

- **Document Structure Roles** - Provide structural description for a section of a page (toolbar, tooltip)
- **Landmark Roles** - Content areas within a page (navigation, search)
- **Live Region Roles** - Used for dynamic changing content like alerts, status messages, and notifications
- **Widget Roles** - Common interactive patterns. Usually used in conjunction with JavaScript (button, checkbox, slider)
- **Window Roles** - Creating subwindows like modals and dialogs

Some of the common roles include:

- `button` - A clickable button
- `checkbox` - A checkable input that has three possible values: true, false, or mixed
- `dialog` - A dialog box or window
- `link` - A hyperlink
- `menu` - A menu of options
- `heading` - Define heading for a section
- `navigation` - A navigation bar
- `search` - Represets a search form or results
- `list` - A list of items
- `listbox` - A list of selectable options
- `menuitem` - An option in a menu or menu bar
- `main` - The main content of a document

There are tons more. Remember, if you can use a semantic tag instead of a div with a role, do that. For example, use a `<button>` instead of a `<div role="button">` if possible. But there may be cases where you need to use a div or link or image but you need to assign it the role of a button.

Let's look at some examples:

## banner

```html
<div role="banner">
  <h1>My Website</h1>
  <p>Welcome to my website</p>
</div>
```

This identifies this part of the markup as a banner.

Let's use the role of `main`:

```html
<div role="main">
  <h2>My Website</h2>
</div>
```

Use the screen reader and it will say "entered main".

This is an example of where I would rather use the semantic tag `<main>` instead of the `role` attribute. Change it to that and you'll see the screen reader will say the same thing.

## button

Let's add a link with the role of `button` in the main area:

```html
<a href="#" role="button">Click Me</a>
```

In this example, we are using an anchor tag with a role of button. Keep in mind that adding the role will just add additional information to the element. It will not change the behavior of the element. So in this case, the anchor tag will still act like a link, but it will be announced as a button to screen readers. If you want to change the behavior, you would need to use JavaScript.

As an example, let's use an image as a button:

```html
<img src="https://picsum.photos/200/300" alt="Random Image" />

<script>
  document
    .querySelector('img')
    .addEventListener('click', () => alert('Image Clicked'));
</script>
```

This image will just be announced as an image and the user will not know it is clickable. Let's add a role of `button`:

```html
<img src="https://picsum.photos/200/300" alt="Random Image" role="button" />
```

Now the user will be notified it is a button, however, it will disregard the alt text. So you may want to add an `aria-label` attribute as well:

```html
<img
  src="https://picsum.photos/200/300"
  alt="Random Image"
  role="button"
  aria-label="Random Image - Click Me"
/>
```

Now it is treated as a button and the label will be read out.

## tabindex

The `tabindex` attribute is used to define the order in which elements are focused when the user presses the tab key. The default value is 0. The value can be negative or positive. A negative value means that the element is not focusable. A positive value means that the element is focusable and the value defines the order in which the element is focused.

The issue that we have with this image button is that it is not focusable. We can make it focusable by setting the `tabindex` attribute to a positive value. Let's set it to 0:

```html
<img
  src="https://picsum.photos/200/300"
  alt="Random Image"
  role="button"
  aria-label="Random Image - Click Me"
  tabindex="0"
/>
```

Now you should be able to cycle through the focusable elements and the image should be included.

## listbox & option

Let's look at another example:

```html
<h2 id="label_fruit">Available Fruit</h2>
<ul role="listbox" aria-labelledby="label_fruit">
  <li role="option">Apples</li>
  <li role="option">Bananas</li>
  <li role="option">Watermelon</li>
  <li role="option">Grapes</li>
</ul>
```

Here, we are using the `role` attribute to identify this as a listbox. We also use the `aria-labelledby` attribute to associate the listbox with the heading. A listbox is a list of options that can be selected. In this case, the screen reader will announce "Available Fruit listbox". We then added the role of `option` to each list item. This will make the screen reader announce each list item as an option.

## region

The `region` role is used to define a large section of content that is important to the page. It is used to define a region of the page that is important for the user to be aware of. This can be used to define the main content area, a sidebar, a footer, or any other section of the page that is important. Use these sparingly only where you need to and there is not a semantic tag that fits.

Here is an example:

```html
<div role="region" aria-labelledby="region-heading">
  <h2 id="region-heading">FAQ</h2>
  This is the FAQ content
</div>
```

We created a region with the heading "FAQ". We also added the `aria-labelledby` attribute to associate the region with the heading. This will make the screen reader announce the heading as the heading of the region.

## tooltip

Here is an example of the `tooltip` document structure role:

```html
<button aria-describedby="notifications-desc">Notifications</button>
<div role="tooltip" id="notifications-desc">View and manage notifications</div>
```

## alert

This is an example of a Live Region role as it is content that is dynamic and changes:

```html
<div role="alert">
  <p>Post saved</p>
</div>
```

## dialog

This is an example of a Window role:

```html
<div role="dialog" aria-labelledby="dialog-label">
  <h2 id="dialog-label">My Dialog</h2>
  <p>This is the dialog content</p>
  <button>Close</button>
</div>
```

Here, we are using the `role` attribute to identify this as a dialog. We also use the `aria-labelledby` attribute to associate the dialog with the heading. A dialog is a window that is used to display content. In this case, the screen reader will announce "My Dialog dialog".
