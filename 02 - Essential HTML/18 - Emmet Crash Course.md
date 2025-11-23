# Emmet Crash Course

Emmet is a powerful toolkit for web developers that greatly improves the speed and efficiency of writing HTML and CSS. It allows you to write HTML and CSS code faster and more efficiently by using abbreviations. Emmet is built into many code editors, including Visual Studio Code, Sublime Text, and Atom. There are some editors and IDEs that don't have Emmet built-in, but you can install it as an extension.

In this crash course, we will cover the basics of Emmet and how to use it to write HTML faster. You can also use it for CSS, but we're going to focus on HTML right now. I realize that we haven't covered things like divs, ids and classes yet, but I think it's important to introduce Emmet early on because it will make writing HTML easier and I'll be using it when we get to that stuff.

## Document Structure

With Emmet, you can quickly generate the basic structure of an HTML document. To create an HTML document, type `!` and press `Enter` or `Tab`. This will generate the following code:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

So we get the basic structure of an HTML document with the doctype, html, head, and body elements as well as some meta tags and a title. This is a great way to quickly generate the basic structure of an HTML document and this is what I will be using when I create new HTML files.

## Abbreviations

Emmet uses abbreviations to generate HTML code. You can use Emmet abbreviations to quickly create HTML elements, classes, IDs, and more. Here are some examples of Emmet abbreviations:

### HTML Elements

To create an HTML element, you can simply type the name of the element and press `Enter` or `Tab`. For example, typing `div` and pressing `Tab` will generate the following code:

```html
<div></div>
```

For a paragraph element, you can type `p` and press `Tab`:

```html
<p></p>
```

### Classes and IDs

You can also create classes and IDs using Emmet. To create a class, use a `.` followed by the class name. For example, if we want a paragraph with a class of `text-xl`:

```html
p.text-xl
<p class="text-xl"></p>
```

If we want a `div`, which is usually the case, we can do `div.text-xl`, however, we don't even need to type `div` because it's the default element. So, we can just type `.text-xl` and press `Enter` or `Tab`:

```html
.text-xl
<div class="text-xl"></div>
```

You can do multiple classes as well:

```html
.text-xl.text-center
<div class="text-xl text-center"></div>
```

For ids it is the same idea, but you use a `#` instead of a `.`. For example, if we want a `div` with an ID of `main`:

```html
#main
<div id="main"></div>
```

If we wanted an id and a class, we can do `#main.text-xl`:

```html
#main.text-xl
<div id="main" class="text-xl"></div>
```

## Nesting Elements

You can also nest elements using Emmet. For example, if we want a `div` with a `p` inside of it:

```html
div>p
<div>
  <p></p>
</div>
```

## Numbering

If we want a `div` with two `p` elements inside of it:

```html
div>p*2
<div>
  <p></p>
  <p></p>
</div>
```

If we want an ordered list with 5 list items:

```html
ol>li*5
<ol>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
  <li></li>
</ol>
```

We can also nest elements with classes and ids:

```html
div#main>p.text-xl*2
<div id="main">
  <p class="text-xl"></p>
  <p class="text-xl"></p>
</div>
```

## Siblings

You can also create sibling elements using Emmet. For example, if we want a `div` followed by a `p`:

```html
div+p
<div></div>
<p></p>
```

## Grouping

We can create entire layouts. This is a bit advanced, especially for where you're at in the course, but just to give you an idea:

```html
div>(header>ul>li*2>a)+footer>p
<div>
  <header>
    <ul>
      <li><a href=""></a></li>
      <li><a href=""></a></li>
    </ul>
  </header>
  <footer>
    <p></p>
  </footer>
</div>
```

## Content

We can even insert content into elements. For example, if we want a `p` with some text:

```html
p{Hello World}
<p>Hello World</p>
```

#### Dummy Content

You can also generate dummy content. For example, if we want a `p` with some lorem ipsum text:

```html
p>lorem
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.</p>
```

You can even specify a length. For example, if we want a `p` with 10 words of lorem ipsum text:

```html
p>lorem10
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
```

## Attributes

You can also add attributes to elements. For example:

```html
<!-- a:link -->
<a href="http://"></a>

<!-- script:src -->
<script src=""></script>
```

Alright, so that's a quick crash course on Emmet. It's a very powerful tool that can greatly improve your workflow. There are more things we can do, but this should give you a good idea of how it works. For more, check out the cheat sheet [here](https://docs.emmet.io/cheat-sheet/)
