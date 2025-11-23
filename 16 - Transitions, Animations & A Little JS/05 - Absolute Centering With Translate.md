# Absolute Centering With Translate

We saw that we can use the `transform` property along with `translate` to move an element along the x and y axis. I want to show you one of those things that we use pretty often, which is putting something in the center when it is positioned absolute. The issue with this is if you set something to let's say, `top: 50%` and `left: 50%`, it will put the top left corner of the element in the center of the parent element. We don't want that. We want the center of the element to be in the center of the parent element. We can use `transform` and `translate` to do this.

Let's start with this HTML:

```html
<header class="header">
  <div class="container">
    <h1>Welcome Aboard</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Provident, id.
      <a href="#main">Read More</a>
    </p>
  </div>
</header>
```

It is similar to the project we did on nesting.

And the base CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  font-family: 'Poppins', sans-serif;
  line-height: 1.6;
}

a {
  text-decoration: none;
}

.container {
  max-width: 900px;
  padding: 0 20px;

  h1 {
    font-size: 3rem;
  }

  p {
    font-size: 1.5rem;
    margin: 25px 0px 25px;

    a {
      color: #fff;
      &:hover {
        color: lightyellow;
      }

      &::after {
        content: '🚀';
      }
    }
  }
}
```

So we have most of the styling done. But let's say we want the container in the middle both horizontally and vertically. Yes we could use flexbox and margins, but I want to show you how to do it with something positioned absolute.

Let's make the container absolute:

```css
.container {
  max-width: 900px;
  padding: 0 20px;
  position: absolute;
}
```

Now, we want it in the middle, so you would think this would do it:

```css
.container {
  max-width: 900px;
  padding: 0 20px;
  position: absolute;
  top: 50%;
  left: 50%;
}
```

This does what it is supposed to. It moves the top left corner of the container to the center of the parent element. But we want the center of the container to be in the center of the parent element. We can use `transform` and `translate` to do this.

```css
.container {
  max-width: 900px;
  padding: 0 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

What we are doing here is moving the container 50% to the left and 50% up. This will put the center of the container in the center of the parent element.

And that's how you can center something absolutely using `transform` and `translate`.

Very simple, but you will be using this a lot, so I wanted to dedicate a lesson to it.
