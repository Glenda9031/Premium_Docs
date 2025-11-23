# Lists

Lists are a way to display information in a structured way. There are two types of lists in HTML: ordered and unordered lists.

## Unordered Lists

Unordered lists are used when the order of the items is not important. They are created using the `<ul>` tag. Each item in the list is created using the `<li>` tag, which stands for "list item". Here's an example of an unordered list:

```html
<h1>Unordered List</h1>
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

This will display as:

- Item 1
- Item 2
- Item 3

By default, the items in an unordered list are displayed with a bullet point. You can change the style of the bullet point or remove it altogether using CSS.

Unordered lists are often used for navigation menus, where the order of the items is not important. When you see a horizontal navigation menu on a website, it is likely implemented using an unordered list. You have to add quite a bit of CSS to make it look like a navigation menu, but the underlying HTML structure is an unordered list.

## Ordered Lists

Ordered lists are used when the order of the items is important. They are not as common as unordered lists. They are created using the `<ol>` tag. Each item in the list is created using the `<li>` tag, which stands for "list item". Here's an example of an ordered list:

```html
<h1>Ordered List</h1>
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ol>
```

This will display as:

1. Item 1
2. Item 2
3. Item 3

By default, the items in an ordered list are displayed with numbers. You can change the style of the numbers or remove them altogether using CSS.


## Definition Lists

Definition lists are the least common but I think you should still know what they are. They are used to display a list of terms and their definitions. They are created using the `<dl>` tag. Each term in the list is created using the `<dt>` tag, which stands for "definition term", and each definition is created using the `<dd>` tag, which stands for "definition description". Here's an example of a definition list:

```html
<h1>Definition List</h1>
<dl>
  <dt>Item 1</dt>
  <dd>Description 1</dd>
  <dt>Item 2</dt>
  <dd>Description 2</dd>
  <dt>Item 3</dt>
  <dd>Description 3</dd>
</dl>
```

## Nested Lists

You can also nest lists inside other lists. Here's an example of a nested list:

```html
<h1>Nested List</h1>
<ul>
  <li>
    Item 1
    <ul>
      <li>Subitem 1</li>
      <li>Subitem 2</li>
    </ul>
  </li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

This will display as:

- Item 1
  - Subitem 1
  - Subitem 2
- Item 2
- Item 3

You can nest lists as deep as you want. Just make sure to indent the nested list to make it clear which items are part of the parent list item.
