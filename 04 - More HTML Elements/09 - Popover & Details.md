# Popovers and Details Elements

Now we're going to get into some very recent additions to HTML. These are cool because they give us dynamic interactive functionality without any JavaScript. Although most of these types of elements have a JavaScript API to use with them. We're just going to look at the basic usage.

## Popovers

We can create popovers, which allow us to do something like click a button and show and hide an element. We can do this without any JavaScript, which is really cool. You can make them look a lot better with CSS, but since we have not got into CSS yet, we'll stick with the markup.

## popovertarget Attribute

We can create a button with a popover target by adding the `data-popover-target` attribute to the button. This will tell the browser that the button is a popover target.

```html
<button popovertarget="popover-1">Open Popover 1</button>
```

Now we need to create the popover itself. We do this by adding a popover element with the `popover` attribute. We also need to give it an ID, which we do by adding the `id` attribute:

```html
<div popover id="popover-1">This is Popover 1</div>
```

Now when we click the button, the popover will show and hide. We can also add multiple popovers to the same page. We can also put whatever other elements we want inside:

```html
<button popovertarget="popover-2">Open Popover 2</button>
<div popover id="popover-2">
  <h3>This Is Another Popover</h3>
  <p>Hello</p>
</div>
```

By default, the popover content will be in the middle of the page, however, we can use CSS to style and position it where we want. We'll look at that later.

## Details

The details element is used to create a disclosure widget from which the user can obtain additional information or controls. The details element is used in conjunction with the summary and can be used to create an accordion.

```html
<details>
  <summary>Details</summary>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate, officia.
</details>
<br />
<details>
  <summary>More Details</summary>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate, officia.
</details>
```

You can also style these with CSS.
