# System Fonts vs Web Fonts

When it comes to using fonts in CSS, you have two main options: **system fonts** and **web fonts**.

## System Fonts

System fonts are the default fonts that are installed on a user's device by default. These fonts are available to all websites and applications, and they are designed to be highly readable and legible. Some common system fonts include Arial, Helvetica, Times New Roman, and Georgia.

We can apply these fonts without importing them into our project. Here's how you can use system fonts in CSS by using the `font-family` property:

```css
body {
  font-family: Arial, sans-serif;
}
```

In this example, we are setting the font family of the `body` element to Arial. If Arial is not available on the user's device, the browser will fall back to the default sans-serif font. The font set on the body element will be inherited by all other elements on the page unless overridden.

## Web Fonts

Web fonts, on the other hand, are custom fonts that are not installed on a user's device. These fonts need to be imported into your project using a `@font-face` rule or a font service like Google Fonts or Adobe Fonts.

You may have other fonts on your system. You can see which fonts are available on your system by going to your system settings and looking at the fonts installed on your device.

**For Windows:**

- Open Control Panel.
- Navigate to Appearance and Personalization.
- Click on Fonts. This will display all the fonts installed on your system.

**For Mac:**

- Open Finder.
- Go to the Applications folder.
- Open the Font Book application.

**For Linux:**

- Open a terminal.
- Type fc-list | grep -i <font_name> and press Enter. Replace <font_name> with the name of the font you're interested in.

#### Using Google Fonts

Google Fonts is a popular service that allows you to easily add custom fonts to your website. There are two ways to use Google Fonts in your project: the standard method and the import method.

The standard method involves adding a link to the Google Fonts stylesheet in the `<head>` section of your HTML file. Here's an example:

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap"
  rel="stylesheet"
/>
```

In this example, we are importing the Poppins font (My favorite font) with 6 different weights (300 - 800) using the standard method.

You don't have to type this out, you can go to the Google Fonts website, select the fonts you want, and copy the link provided.

The 2 preconnect links are used to establish a connection to the Google Fonts server before the browser requests the font files. This can help improve performance by reducing the time it takes to load the fonts.

The import method involves using the `@import` rule in your CSS file to import the font. Here's an example:

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
```

This gives us the same result as the standard method, but it allows us to keep all our styles in one place. I prefer the standard method because I don't like adding the `@import` rule in my CSS file but it's up to you.

Now you can use the imported font in your CSS like this:

```css
body {
  font-family: 'Poppins', sans-serif;
}
```

The browser will download the font from Google Fonts and apply it to the `body` element.

You'll come to have certain font families that you use in your projects. Here are some of my favorite fonts and fonts we will use in this course:

- Poppins
- Montserrat
- Roboto
- Open Sans
- Lato

These are some of the cleanest looking fonts in my opinion.

## Serif vs Sans-Serif Fonts

Fonts can be broadly classified into two categories: serif and sans-serif.

- **Serif fonts** have small lines or strokes attached to the ends of the main strokes of the characters. These fonts are often considered more traditional and formal. Examples of serif fonts include Times New Roman, Georgia, and Garamond.

- **Sans-serif fonts** do not have these small lines or strokes, giving them a cleaner and more modern look. Sans-serif fonts are often used for digital content and are considered more readable on screens. Examples of sans-serif fonts include Arial, Helvetica, and Verdana.

<img src="../images/serif-sans-serif.png" alt="Serif vs Sans-Serif Fonts" />

When choosing fonts for your website, consider the tone and style you want to convey. Serif fonts are often used for more formal or traditional websites, while sans-serif fonts are popular for modern and clean designs.

I will be using the Poppins fonts for a lot of the sandbox projects. The Google font link will be included in the HTML file by default.

In the next lesson, we will look at some font properties in CSS.
