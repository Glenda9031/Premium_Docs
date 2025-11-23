# Nesting

CSS Has recently added a very powerful feature called nesting. This allows you to nest selectors inside of other selectors. This is very useful for keeping your CSS organized and easy to read. This is something that has been available for a while if you use a CSS preprocessor like Sass or Less, but now it is available in vanilla CSS. It is a newer feature and is supported in the latest version of the major browsers, however, there may not be support in some mobile browsers and older versions of desktop browsers.

This is another one of those things that comes down to personal preference. Some people love it and some people hate it. I personally like it because it keeps things organized and easy to read. It is the main reason that I use Sass, however since it's so new to CSS and there are some differences, I haven't really used it much in production yet. We're not going to use it widely in this course because I think it's important for you to learn CSS without them first, but I wanted to show you how it works. We may use it in a few examples.

We're going to build a little landing page project using nesting. Let's get started.

Let's use the following HTML:

```html
<header class="header">
  <h1>Welcome Aboard</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Provident, id.
    <a href="#main">Read More</a>
  </p>
</header>

<main id="main">
  <div class="container">
    <section class="section section-1">
      <div class="card">
        <h3>Lorem, ipsum dolor.</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Error natus
          dolorem non aspernatur quia adipisci, eum soluta porro velit voluptas
          asperiores in nihil libero rem dicta esse ex beatae iste?
        </p>
      </div>
    </section>
    <section class="section section-2">
      <div class="card">
        <h3>Lorem, ipsum dolor.</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Error natus
          dolorem non aspernatur quia adipisci, eum soluta porro velit voluptas
          asperiores in nihil libero rem dicta esse ex beatae iste?
        </p>
      </div>
    </section>
    <section class="section section-3">
      <div class="card">
        <h3>Lorem, ipsum dolor.</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Error natus
          dolorem non aspernatur quia adipisci, eum soluta porro velit voluptas
          asperiores in nihil libero rem dicta esse ex beatae iste?
        </p>
      </div>
    </section>
  </div>
</main>
```

We have a header with a title and a paragraph with a link to the main content. The main content has 3 sections with a card in each section. Each card has a title and a paragraph.

Let's add the base CSS:

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
  margin: 0 auto;
  padding: 0 20px;
}
```

Notice I added the scroll-behavior on the universal selector. This also works in addition to putting it on the `html` root. This will make the scrolling smooth when you click on a link that goes to an anchor tag.

Let's style the header. I want it to take up the entire viewport. You could add a background image if you want to make it look a bit cooler.

```css
.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
  background: lightcoral;
  padding: 0 20px;
}
```

The header will take up the entire viewport height and be centered. The text will also be centered. The background will be lightcoral.

This is where we can start to nest. I want to style the h1 and the p tag inside the header. I can nest the h1 like this:

```css
.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
  background: lightcoral;
  padding: 0 20px;

  h1 {
    font-size: 4rem;
  }
}
```

Now if you were to have another h1 outside of the header, it would not be affected by this style. This is a great way to keep your CSS organized and easy to read.

Let's add the paragraph styles:

```css
.header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
  background: lightcoral;
  padding: 0 20px;

  h1 {
    font-size: 4rem;
  }

  p {
    font-size: 2rem;
    margin: 25px 0px 25px;
  }
}
```

Only the p tag inside the header will have these styles.

Let's add the link styles:

```css
a {
  color: #fff;

  &:hover {
    color: lightyellow;
  }

  &::after {
    content: '🚀';
  }
}
```

So, here I wanted to show you how you can nest pseudo-elements. The `&` symbol is used to reference the parent selector. So, `&:hover` will target the link when hovered over. `&::after` will add a rocket emoji after the link text.

Now let's style the main content and cards. The sections just need some margin for spacing:

```css
.section {
  margin: 50px 0;
}
```

For the cards, I could choose to nest the card styles inside the section styles, but I'm going to keep them separate to show you that you can nest as much or as little as you want.

```css
.card {
  background: #fff;
  padding: 20px;
  margin: 20px 0;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);

  h3 {
    font-size: 1.5rem;
    margin-bottom: 10px;
  }

  p {
    font-size: 1rem;
  }
}
```

We nested the h3 and p tags inside the card class. So these only apply to cards.

We can add a media query as well for small screens:

```css
@media (max-width: 768px) {
  .header {
    height: 30vh;
    h1 {
      font-size: 3rem;
    }

    p {
      font-size: 1.5rem;
    }
  }

  .card {
    h3 {
      font-size: 1.2rem;
    }
  }
}
```

That's it. We have a basic landing page. You can use nesting as little or as much as you want. Like I said, I am not going to focus on them too much in this course just because they are so new and I think it's important that you learn the basics first. But I wanted to show you how they work.
