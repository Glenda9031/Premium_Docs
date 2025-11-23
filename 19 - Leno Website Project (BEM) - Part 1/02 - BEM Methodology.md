# BEM Methodology

In this project, we will be using the BEM methodology to structure our CSS. BEM stands for Block Element Modifier. It is a naming convention for classes in HTML and CSS. It is not a framework or library or anything like that. It is just a way to write CSS that is easy to read and understand as well as maintainable. It is great for really large projects where you have a lot of CSS and a lot of people working on it.

## Blocks, Elements and Modifiers

BEM is structured around three main concepts: Blocks, Elements and Modifiers.

### Blocks

A block is a standalone entity that is meaningful on its own. For example, a header, footer, button, etc. Blocks are the top-level abstraction in BEM. A block can contain elements and other blocks.

```html
<div class="hero"></div>
```

### Elements

An element is a part of a block that has no standalone meaning and is semantically tied to its block. For example, a button that is part of a hero block. Elements are denoted by two underscores `__`.

```html
<div class="hero">
  <div class="hero__text">Welcome to the website</div>
  <a href="more.html" class="hero__button">Read More</a>
</div>
```

### Modifiers

A modifier is a flag on a block or element. It is used to change appearance or behavior. For example, a button that is disabled. Modifiers are denoted by two hyphens `--`.

```html
<div class="hero">
  <div class="hero__text--lg">Welcome to the website</div>
  <a href="more.html" class="hero__button hero__button--disabled">Read More</a>
</div>
```

## BEM Naming Convention

The naming convention for BEM is `block__element--modifier`. The block name should be unique and descriptive. The element name should be unique within the block. The modifier name should be unique within the block or element.

```css
.hero {
  background-color: #f0f0f0;
}

.hero__text {
  font-size: 24px;
}

.hero__button {
  background-color: #007bff;
}

.hero__button--disabled {
  background-color: #ccc;
  cursor: not-allowed;
}
```

You may have blocks with more than one word in the name. In that case, you should use a hyphen `-` to separate the words as we would normally do in CSS.

```html
<div class="header-nav"></div>
```

```css
.header-nav {
  background-color: #333;
}
```

## Benefits of BEM

#### Modularity

Block styles are never dependent on other elements on a page, so you will never experience problems from cascading.

You also get the ability to transfer blocks from your finished projects to new ones.

#### Reusability

Composing independent blocks in different ways, and reusing them intelligently, reduces the amount of CSS code that you will have to maintain.

With a set of style guidelines in place, you can build a library of blocks, making your CSS super effective.

#### Structure

BEM methodology gives your CSS code a solid structure that remains simple and easy to understand.

## Drawbacks of BEM

#### Long Class Names

One of the biggest drawbacks of BEM is the long class names. This can make your HTML code look cluttered and hard to read.

#### Repetitive Code

BEM can lead to a lot of repetitive code. For example, if you have a block with a lot of elements and modifiers, you will end up writing a lot of CSS.

#### Lots of Classes

BEM can lead to a lot of classes in your HTML code. We basically add a class to just about every element on the page. This is helpful in that it makes it easy to see what is going on, but it can also make your HTML code look cluttered.

BEM may or may not be for you. You could easily build this project without BEM as well.
