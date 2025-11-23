# Screen Reader & Accessibility Attributes

In this lesson, we will go over some HTML and test it with a screen reader and see what issues we have and how we can make things more accessible. We will learn about and use attributes like `role` and `aria-label`.

Use the starter code for this lesson. Here is the HTML:

```html
<body>
  <div class="header">
    <a class="logo" href="/">My Website</a>
    <div class="nav">
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/contact">Contact</a></li>
        <li>
          <a href="https://facebook.com"
            ><i class="fa-brands fa-facebook"></i
          ></a>
        </li>
      </ul>
      <div class="search">
        <input type="text" />
        <button>Search</button>
      </div>
    </div>
  </div>
</body>
```

Here is the CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Lato', sans-serif;
  line-height: 1.6;
}

.header {
  background-color: #333;
  color: #fff;
  padding: 10px 0;
  justify-content: space-between;
  align-items: center;
}

.logo {
  text-align: center;
  font-size: 24px;
  font-weight: bold;
  color: #fff;
  text-decoration: none;
  display: block;
}

/* Styling the navigation */
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
}

.nav ul {
  list-style-type: none;
  display: flex;
}

.nav ul li {
  margin-right: 20px;
}

.nav ul li a {
  color: #fff;
  text-decoration: none;
  padding: 5px 10px;
  transition: all 0.3s ease;
}

.nav ul li a:hover {
  background-color: #555;
  border-radius: 5px;
}

.search {
  display: flex;
  align-items: center;
}

.search input[type='text'] {
  padding: 8px;
  border: none;
  border-radius: 5px 0 0 5px;
  font-size: 14px;
  outline: none;
}

.search button {
  padding: 8px 15px;
  background-color: #4caf50;
  color: #fff;
  border: none;
  border-radius: 0 5px 5px 0;
  cursor: pointer;
  font-size: 14px;
  transition: background-color 0.3s ease;
}

.search button:hover {
  background-color: #45a049;
}
```

Open the Skilltide extension and click on "Screen Reader".

It should read the title of the page first. So the title is important not only for SEO, but also for people who are using a screen reader.

Click "Next"

It says "Link Logo". Here, we can use an attribute called `role`. This is an attribute that is used to define the purpose of the element or section. Let's add a role of **banner**. We should also use a semantic element here. Let's change the `div` to a `header` tag.

```html
<header class="header" role="banner"></header>
```

Now, start the screen reader again and it should say something like "Entering Banner".

Now click next again and it says "Link My Website". So it just reads the link text. We want the user to know this is the logo. We can use and ARIA attribute called `aria-label` to provide an accessible name for an element.

```html
<a class="logo" href="/" aria-label="logo and link to homepage">My Website</a>
```

Now it will let the user know that this is the logo with a link to the homepage.

Click "Next"

It says 'List with 3 items'. That is not very helpful. It just says a list and not navigation. We can fix that by changing the `div` to a `nav`, which is a semantic tag. We can also add a role of navigation to the `nav` tag.

```html
<nav class="nav" role="navigation">//...</nav>
```

Now start over and click "Next". It should say "Entered Navigation". So the use knows this is a list of navigation links.

Now click "Next" and step through the links. The home, about and contact are fine, but when we get to the facebook link, it just says "Link". We can add an `aria-label` to this link to let the user know that this is a link to Facebook.

```html
<a href="https://facebook.com" aria-label="Facebook page"
  ><i class="fa-brands fa-facebook"></i
></a>
```

Now it will read out "Facebook page"

Click "Next" and it says "Textbox". Obviously, that doesn't tell us much.

Let's add a role to the div letting the user know this is a search area. It's also good practice to give your input fields a label. In some cases, such as this, you may not want a label to be displayed. We have a couple options. We can use the `aria-label` attribute on the input itself. Or we can use the `label` tag and hide it with CSS. Let's add a label tag and hide it:

```html
<div class="search" role="search">
  <label for="search-term" class="visually-hidden">Search Term</label>
  <input type="text" name="search" placeholder="Search" id="search-term" />
  <button>Search</button>
</div>
```

I added a label with a class of `visually-hidden`. Let's add the following CSS.

## Hiding Elements From View

The way that we hide the label matters. If we simply set the label to `display: none` or `visibility-hidden` or even set the height/width to 0, it takes the element out of the flow of the document. Most screen readers will then not see it. So there is a specific way to remove it from view but keep it in the document. This is a very common snippet used for this reason. Add this to your CSS:

```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
```

Now your label should be hidden but still in the document for screen readers.

To explain this CSS,

- We position it absolutely to take it out of the document flow.
- We set the width and height to 1px to make it take up as least space as possible.
- We then set the margin to -1px, which helps to further hide the element from view while ensuring it remains technically on the page.
- Set the padding inside the element to 0, ensuring no extra space inside the 1px dimensions.
- Set the overflow to hidden to hide any content that overflows the dimensions of the element.
- rect(0, 0, 0, 0) specifies no visible area, effectively hiding the element's content.
- Sets the element's border to 0, ensuring no visible border.

The button has the text of "Search", so we don't really need to add any labels or anyting here. Just like with the 3 navigation links.

It's important to not overuse the `aria-label` and other aria attribute. It's a good way to provide a label for some elements, but it should be used sparingly. The best way is to actually test your websites with a screen reader.

Let's Run the accessibility checker. We have 2 issues remaining:

- Missing H1
- Text Contrast

It is reccomended that you have a descriptive H1 on your pages. This is important for SEO and for screen readers. If you don't want it physically there, just use the `visually-hidden` class.

I don't mind having an H1 here, so let's add this under the header:

```html
<main class="container">
  <h1>Welcome To My Website</h1>
</main>
```

Run the checker again. We still have the text contrast issue. It is talking about the search button. The white text on the light green background has low contrast. I think it looks fine and readable, however there are people with visual issues that may not be able to read it. So let's change the color in the CSS:

```css
.search button {
  //..
  background-color: #2b5429;
}

.search button:hover {
  //..
  background-color: #37803a;
}
```

Now you should pass the checker.

I do just want to say that not every site you build needs to pass this thing. You may very well had wanted to use that color and that's fine. It's just a suggestion.
