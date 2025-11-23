# Font Awesome

Font Awesome is a popular icon library that you can use in your projects. It is a great way to add icons to your projects without having to create them yourself. I know this is a little detour from the CSS path, but I think it is important to know about Font Awesome because it is so widely used and it is so easy to use.

You can read more about font awesome [here](https://fontawesome.com/). You can also find the icons that you want to use [here](https://fontawesome.com/icons).

### How to Use Font Awesome

To use Font Awesome, you need to include the Font Awesome CSS file in the head of your HTML document. This file is hosted on a CDN (Content Delivery Network), so you don't need to download it.

To find the link, you can use [http://www.cdnjs.com](http://www.cdnjs.com) and search for Font Awesome. You can then copy the link and paste it in the head of your HTML document.

It will look like something like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!-- Font Awesome Link -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
      integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A=="
      crossorigin="anonymous"
      referrerpolicy="no-referrer"
    />
    <link rel="stylesheet" href="styles.css" />
    <title>HTML & CSS Sandbox</title>
  </head>
  <body></body>
</html>
```

Now you can use any of the free fonts in your project. You can find the icons that you want to use on the Font Awesome website. You can then copy the class name and paste it in your HTML document.

For example, if you want to use the check icon, you can use the following code:

```html
<i class="fas fa-check"></i>
```

Here are some other examples:

```html
<h3>Icon Examples</h3>
<i class="fas fa-check"></i>
<i class="fas fa-times"></i>
<i class="fas fa-exclamation"></i>
<i class="fas fa-exclamation-triangle"></i>
<i class="fas fa-exclamation-circle"></i>
<i class="fas fa-info"></i>
<i class="fas fa-info-circle"></i>
<i class="fas fa-question"></i>
<i class="fas fa-question-circle"></i>
```

Notice they all have the class of `fas` which stands for Font Awesome Solid. There are other classes that you can use as well. For example, `fab` stands for Font Awesome Brands.

Here are some social media examples. These use the `fab` class:

```html
<h3>Social Media Icons</h3>
<i class="fab fa-facebook"></i>
<i class="fab fa-twitter"></i>
<i class="fab fa-instagram"></i>
<i class="fab fa-linkedin"></i>
<i class="fab fa-youtube"></i>
<i class="fab fa-github"></i>
```

You can also change the size of the icons by using the `fa-2x`, `fa-3x`, `fa-4x`, `fa-5x`, `fa-6x`, `fa-7x`, `fa-8x`, `fa-9x`, `fa-10x` classes.

Here is an example:

```html
<h3>Icon Sizes</h3>
<i class="fas fa-check fa-2x"></i>
<i class="fas fa-check fa-3x"></i>
<i class="fas fa-check fa-4x"></i>
<i class="fas fa-check fa-5x"></i>
<i class="fas fa-check fa-6x"></i>
<i class="fas fa-check fa-7x"></i>
<i class="fas fa-check fa-8x"></i>
<i class="fas fa-check fa-9x"></i>
<i class="fas fa-check fa-10x"></i>
```

These icons are actual fonts, they are not images. So we can use CSS to style them. For example, we can change the color of the icons by using the `color` property.

Here is an example:

```html
<h3>Icon Colors</h3>
<i class="fas fa-check fa-2x" style="color: red;"></i>
<i class="fas fa-check fa-3x" style="color: blue;"></i>
<i class="fas fa-check fa-4x" style="color: green;"></i>
<i class="fas fa-check fa-5x" style="color: orange;"></i>
<i class="fas fa-check fa-6x" style="color: purple;"></i>
```

So now, whenever you want to use icons, you simply bring in the Font Awesome CSS file and use the class names that you find on the Font Awesome website.
