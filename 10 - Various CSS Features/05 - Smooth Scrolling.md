# Smooth Scrolling

In CSS, we can use the `scroll-behavior` property to create smooth scrolling effects. This property can be applied to specific elements or the entire document by using the `html` selector.

We already know that if we link to a specific section on a page using an anchor tag, the browser will jump directly to that section. With the `scroll-behavior` property set to `smooth` on the `html` element, the browser will smoothly scroll to the target section instead of jumping directly to it. Let's create a small project to demonstrate this.

Let's use the following HTML as an example:

```html
<header class="header">
  <nav class="menu">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#project-1">Project 1</a></li>
      <li><a href="#project-2">Project 2</a></li>
      <li><a href="#project-3">Project 3</a></li>
      <li><a href="#project-4">Project 4</a></li>
    </ul>
  </nav>
</header>

<main class="container">
  <section id="home" class="section">
    <h2>Welcome</h2>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quia cumque cum
      aliquid deserunt, omnis officiis, corporis nesciunt quos numquam
      consequuntur sint blanditiis nobis vero explicabo distinctio ducimus
      doloremque voluptatem, possimus quis commodi repellat magnam fugiat
      cupiditate assumenda. Corrupti nulla quos, dignissimos mollitia deleniti
      adipisci illo aliquid nesciunt atque vel facilis?
    </p>
  </section>

  <section id="project-1" class="section">
    <h2>Project 1</h2>
    <img src="./project1.jpg" alt="" />
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quia cumque cum
      aliquid deserunt, omnis officiis, corporis nesciunt quos numquam
      consequuntur sint blanditiis nobis vero explicabo distinctio ducimus
      doloremque voluptatem, possimus quis commodi repellat magnam fugiat
      cupiditate assumenda. Corrupti nulla quos, dignissimos mollitia deleniti
      adipisci illo aliquid nesciunt atque vel facilis?
    </p>

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita minus
      nesciunt temporibus hic fugiat enim ullam, sed minima tempore non,
      voluptas molestias culpa fugit autem alias odio a! Maxime numquam amet
      doloribus voluptatum, provident odio, rerum iste illo ipsa dolorem error
      dolor totam voluptas omnis quis! Fugit labore cupiditate assumenda.
      Voluptates dolorem dignissimos, id odit nobis provident omnis deserunt eos
      ratione quidem, eaque magnam, quibusdam doloribus obcaecati rem dolor quis
      quaerat perferendis porro debitis dolore.
    </p>
  </section>

  <section id="project-2" class="section">
    <h2>Project 2</h2>
    <img src="./project2.jpg" alt="" />
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quia cumque cum
      aliquid deserunt, omnis officiis, corporis nesciunt quos numquam
      consequuntur sint blanditiis nobis vero explicabo distinctio ducimus
      doloremque voluptatem, possimus quis commodi repellat magnam fugiat
      cupiditate assumenda. Corrupti nulla quos, dignissimos mollitia deleniti
      adipisci illo aliquid nesciunt atque vel facilis?
    </p>

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita minus
      nesciunt temporibus hic fugiat enim ullam, sed minima tempore non,
      voluptas molestias culpa fugit autem alias odio a! Maxime numquam amet
      doloribus voluptatum, provident odio, rerum iste illo ipsa dolorem error
      dolor totam voluptas omnis quis! Fugit labore cupiditate assumenda.
      Voluptates dolorem dignissimos, id odit nobis provident omnis deserunt eos
      ratione quidem, eaque magnam, quibusdam doloribus obcaecati rem dolor quis
      quaerat perferendis porro debitis dolore.
    </p>
  </section>

  <section id="project-3" class="section">
    <h2>Project 3</h2>
    <img src="./project3.jpg" alt="" />
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quia cumque cum
      aliquid deserunt, omnis officiis, corporis nesciunt quos numquam
      consequuntur sint blanditiis nobis vero explicabo distinctio ducimus
      doloremque voluptatem, possimus quis commodi repellat magnam fugiat
      cupiditate assumenda. Corrupti nulla quos, dignissimos mollitia deleniti
      adipisci illo aliquid nesciunt atque vel facilis?
    </p>

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita minus
      nesciunt temporibus hic fugiat enim ullam, sed minima tempore non,
      voluptas molestias culpa fugit autem alias odio a! Maxime numquam amet
      doloribus voluptatum, provident odio, rerum iste illo ipsa dolorem error
      dolor totam voluptas omnis quis! Fugit labore cupiditate assumenda.
      Voluptates dolorem dignissimos, id odit nobis provident omnis deserunt eos
      ratione quidem, eaque magnam, quibusdam doloribus obcaecati rem dolor quis
      quaerat perferendis porro debitis dolore.
    </p>
  </section>

  <section id="project-4" class="section">
    <h2>Project 4</h2>
    <img src="./project4.jpg" alt="" />
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quia cumque cum
      aliquid deserunt, omnis officiis, corporis nesciunt quos numquam
      consequuntur sint blanditiis nobis vero explicabo distinctio ducimus
      doloremque voluptatem, possimus quis commodi repellat magnam fugiat
      cupiditate assumenda. Corrupti nulla quos, dignissimos mollitia deleniti
      adipisci illo aliquid nesciunt atque vel facilis?
    </p>

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita minus
      nesciunt temporibus hic fugiat enim ullam, sed minima tempore non,
      voluptas molestias culpa fugit autem alias odio a! Maxime numquam amet
      doloribus voluptatum, provident odio, rerum iste illo ipsa dolorem error
      dolor totam voluptas omnis quis! Fugit labore cupiditate assumenda.
      Voluptates dolorem dignissimos, id odit nobis provident omnis deserunt eos
      ratione quidem, eaque magnam, quibusdam doloribus obcaecati rem dolor quis
      quaerat perferendis porro debitis dolore.
    </p>
  </section>
</main>
```

The images are included in the project files (sandbox).

And some base CSS:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  font-size: 18px;
  line-height: 1.6;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
}

p {
  margin-bottom: 20px;
}

img {
  width: 100%;
  margin-bottom: 40px;
}

.container {
  max-width: 700px;
  margin: 0 auto;
}
```

We are just setting up the base styles for the project. The images will take up the full width of the container and have a margin at the bottom. There is a container with a max-width of 700px and centered on the page.

Let's first style the header and the navigation:

```css
.header {
  background: linear-gradient(45deg, #f00, #00f);
  color: #fff;
  padding: 10px 0;
  margin-bottom: 80px;
}

.header .menu ul {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 3rem;
}

.header .menu a {
  color: #fff;
}

.header .menu a:hover {
  color: #f00;
}
```

This will create a header with a gradient background and white text. The navigation links will be centered and have a gap of 3rem between them. The links will turn red when hovered over.

Let's style the sections:

```css
.section {
  margin: 30px 0;
}

.section h2 {
  margin-bottom: 20px;
  text-align: center;
  font-size: 45px;
  background: linear-gradient(45deg, #f00, #00f);
  color: #fff;
}

.section#home {
  margin-bottom: 100px;
}
```

The sections will have a margin of 30px on the top and bottom. The `h2` elements will have a margin of 20px on the bottom, be centered, and have a gradient background with white text. The `#home` section will have a margin of 100px on the bottom.

Right now, if you click on a navigation link, the browser will jump directly to the target section. Let's add the smooth scrolling effect by setting the `scroll-behavior` property to `smooth` on the `html` element. We can add the `html` selector to the same section as the `body` selector in the CSS file:

```css
html,
body {
  font-family: 'Poppins', sans-serif;
  font-size: 18px;
  line-height: 1.6;
  scroll-behavior: smooth;
}
```

You can also put it on the universal selector. Sometimes I will add it along with my reset:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}
```

Thats it! Now when you click on a navigation link, the browser will smoothly scroll to the target section instead of jumping directly to it. We used to have to use JavaScript and even jQuery to achieve this effect, but now it's as simple as adding a single CSS property.

Now it would be convenient to make the navbar stick to the top as well as add a back to top button. Let's do that in the next lesson.
