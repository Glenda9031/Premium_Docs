# How Forms & Inputs Work

In HTML, forms are used to collect user input. They are essential for creating interactive web pages that allow users to submit data. Forms and inputs can be used for a variety of purposes, such as logging in, signing up, and submitting feedback. HTML on it's own can't do much with the data, but when combined with a server-side language like PHP, Python or JavaScript using Node.js, you can process the data and store it in a database. You can also use front-end JavaScript to validate the data and submit to an API. That's beyond the scope of this course though. We're going to focus on creating the form itself and later we will learn how to style it with CSS.

The `<form>` tag itself does not show anything in the browser. It is used to group form elements and define the action that should be taken when the form is submitted. The form tag has several attributes that control its behavior:

- `action`: The URL of the server-side script that will process the form data.
- `method`: The HTTP method used to submit the form data (GET or POST).
- `enctype`: The encoding type used to submit the form data (application/x-www-form-urlencoded, multipart/form-data, or text/plain).
- `target`: The name of the window or frame where the form response should be displayed.

Let's say there was a server-side script called `submit.php` that would process the form data. You would set the `action` attribute to `submit.php` and the `method` attribute to `POST`:

```html
<form action="submit.php" method="POST">
  <!-- Form elements go here -->
</form>
```

## Front-End JavaScript

You can also use front-end JavaScript to do things like validate and make requests to APIs. To do this, you can use the `onsubmit` event handler to run a JavaScript function when the form is submitted:

```html
<form onsubmit="myFunction()">
  <!-- Form elements go here -->
</form>
```

Then you would define the `myFunction` function in your JavaScript.

In our case, since we are focused on just creating and later styling the form and not any type of functionality, we won't actually need to use any of these attributes. We will just create the form and inputs.

## Inputs

Inputs are the building blocks of forms. They allow users to enter data such as text, numbers, and dates. There are several types of inputs available in HTML, each with its own purpose. Here are some common input types:

- `text`: A single-line text input field.
- `password`: A single-line text input field that hides the characters.
- `email`: A single-line text input field that validates the input as an email address.
- `number`: A single-line text input field that only accepts numbers.
- `select`: A dropdown list that allows users to select one option from a list.
- `date`: A single-line text input field that allows users to select a date from a calendar.
- `checkbox`: A checkbox that allows users to select multiple options.
- `radio`: A radio button that allows users to select one option from a list.
- `file`: A file input field that allows users to upload files.
- `range`: A slider input field that allows users to select a value from a range.
- `submit`: A button that submits the form data to the server.
- `reset`: A button that resets the form to its initial state.
