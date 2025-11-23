# JavaScript & CSS

I realize that this is not a JavaScript course and it is absolutely fine if you know 0 JavaScript. But I want to show you a little bit of how we can use JavaScript to interact with CSS. I will try and explain, but if you can't grasp it, that's okay. You can always come back to this later. My Modern JS From The Beginning course is a great place to start if you want to learn JavaScript. I also have a 20 and 50 project course with HTML/CSS/JS projects.

Let's start with a simple example. We are going to create a button that toggles a class on the body. When the class is toggled, the background color of the body will change.

Here is the HTML:

```html
<div class="container">
  <button class="btn">Toggle Colors</button>
</div>
```

And the CSS:

```css
body {
  font-family: Arial, sans-serif;
}

.container {
  max-width: 600px;
  margin: 30px auto;
}

.btn {
  display: inline-block;
  cursor: pointer;
  padding: 10px 20px;
  background-color: lightblue;
  color: #333;
  text-decoration: none;
  border-radius: 5px;
  margin: 10px;
}
```

## Including JavaScript

To add JavaScript to your project, you can either add `<script>` tags to your HTML file or create a separate JavaScript file and include it in your HTML file. I suggest the latter.

Create a new file in your project folder called `main.js`.

Now include it in your HTML. You usually want to put this just before the closing `</body>` tag.

```html
<!-- Rest of your html -->
  <script src="main.js"></script>
</body>
```

Now let's add some JavaScript to `main.js`:

```js
console.log('Hello from JavaScript');
```

The console is a tool that developers use to log information. You can open it in your browser by opening your devtools or right-clicking on the page and selecting "Inspect" or "Inspect Element". Then go to the "Console" tab. You should see the message "Hello from JavaScript".

## Variables

Variables are used to store data. You can think of them as containers. You can store any type of data in a variable. Here are some examples:

```js
const name = 'John Doe';
const age = 30;
const isCool = true;
```

The `const` keyword is used to declare a variable that cannot be reassigned. If you want to reassign a variable, you can use the `let` keyword:

```js
let name = 'John Doe';
name = 'Jane Doe';
```

I use `const` by default and only use `let` when I know that I will be reassigning the variable.

## Selecting Elements

We can select elements in JavaScript using the `document.querySelector` method. This method takes a CSS selector as an argument and returns the first element that matches the selector.

I want to select the button element. I can do that by using the class of `.btn`:

```js
const button = document.querySelector('.btn');
```

Now you can console log the button:

```js
console.log(btn);
```

You should see the element in the console.

## Using IDs

I much prefer using IDs to select elements. It is faster and more specific. Let's add an ID to the button element:

```html
<div class="container">
  <button id="toggleBtn" class="btn">Toggle Colors</button>
</div>
```

Now we can select the button using the ID:

```js
const button = document.querySelector('#toggleBtn');
```

## Adding Event Listeners

We can add event listeners to elements to listen for events like clicks, hovers, etc. We can do this by using the `addEventListener` method. This method takes two arguments: the event you want to listen for and a function that will run when the event occurs.

Let's add a click event listener to the button:

```js
button.addEventListener('click', function () {
  console.log('Button clicked');
});
```

Now when you click the button, you should see the message in the console. Cool right?

## Selecting the Body

In JavaScript, we can get the body element by using the `document.body` property. Let's log it:

```js
console.log(document.body);
```

You should see it in the console. You can delete the log now.

## Toggling a Class

We can toggle a class on an element by using the `classList.toggle` method. This method takes a class name as an argument and toggles it on the element.

Let's toggle a class on the body when the button is clicked:

```js
button.addEventListener('click', function () {
  document.body.classList.toggle('dark');
});
```

Open your devtools and look at the body element. You should see the class being toggled.

## Styling the Body

Now let's add some styles to the body when the class is toggled. Add the following CSS:

```css
.dark {
  background-color: #333;
  color: #fff;
}
```

Now when you click the button, the background color of the body should change.

## Adding a Transition

We can add a transition to the body element to make the color change smoother. Add the following CSS:

```css
body {
  font-family: Arial, sans-serif;
  transition: background 0.5s;
}
```

Now it will transition over 0.5 seconds. You can adjust the duration to make it faster or slower.

This is the essence of how JavaScript and CSS can work together. It is mostly adding, removing and toggling classes and styles as well as the content itself. You can do a lot more with JavaScript and CSS, but this is a good starting point.
