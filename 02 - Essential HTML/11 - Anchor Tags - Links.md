# Anchor Tags - Links

In this lesson, we'll delve into the versatile world of anchor tags in HTML, commonly known as links. Anchor tags allow us to create hyperlinks, enabling users to navigate between different web pages, sections within the same page, email addresses, and even files. Let's explore the different types of links we can create using anchor tags.

## External Links

External links are hyperlinks that direct users to a different website. To create an external link, we need to specify the URL of the destination website in the `href` attribute of the anchor tag. Here's an example:

```html
<h2>External Link</h2>
<p><a href="https://www.google.com">Visit Google</a></p>
```

When you click this link, the page will navigate to google.com. This means that you will leave the current website and be redirected to the specified URL.

## Link With Target

There may be times where you want to link to another website but keep your current website open. You can achieve this by using the `target` attribute in the anchor tag. The `target` attribute specifies where to open the linked document. Here's an example:

```html
<h2>Link With Target</h2>
<p><a href="https://www.google.com" target="_blank">Visit Google</a></p>
```

In this example, the `target="_blank"` attribute opens the linked document in a new tab or window, depending on the user's browser settings. This way, the user can navigate to the external website while keeping the current website open.

## Relative Links

Relative links are hyperlinks that point to a file or resource within the same website or directory. They are specified relative to the current page's URL. Here's an example of a relative link:

```html
<h2>Relative Link</h2>
<p><a href="about.html">About Us</a></p>
```

Create a page in the same directory called `about.html`, and clicking this link will navigate to the `about.html` page. Relative links are useful when linking to pages within the same website or directory structure.

There may be a slash at the beginning of the URL to indicate the root directory. For example, `/about.html` would point to the `about.html` file in the root directory. If there is no slash, the link is relative to the current directory.

## Internal Links

Internal links are hyperlinks that direct users to different sections within the same web page. To create an internal link, we need to specify the `id` attribute of the target section in the `href` attribute of the anchor tag. Here's an example:

```html
<h2>Internal Link</h2>
<p><a href="#section2">Jump to Section 2</a></p>
```

If you have an element with the `id="section2"` attribute on the same page, clicking this link will scroll the page to that section. This is a common practice for long web pages with multiple sections.

## Email Links

Email links allow users to send emails to a specified email address. To create an email link, we need to specify the email address in the `href` attribute of the anchor tag. Here's an example:

```html
<h2>Email Link</h2>
<p><a href="mailto:example@example.com">Send an Email</a></p>
```

When you click this link, your default email client will open with the specified email address pre-filled in the "To" field. Users can then compose and send an email to the specified address.

## File Links

File links allow users to download files from a website. To create a file link, we need to specify the file path in the `href` attribute of the anchor tag. Here's an example:

```html
<h2>Link to File</h2>
<p><a href="invoice.pdf">Download Document</a></p>
```

When you click this link, the browser will download the `invoice.pdf` file from the website. Make sure the file is accessible and located in the same directory or a subdirectory of the website. I included a mock invoice in the starter code.

## Title Attribute

The `title` attribute in the anchor tag allows you to provide additional information about the link. When users hover over the link, the title text appears as a tooltip. Here's an example:

```html
<h2>Link with Title Attribute</h2>
<p>
  <a href="https://www.example.com" title="Visit Example Website"
    >Visit Example Website</a
  >
</p>
```

When you hover over the link, a tooltip with the text "Visit Example Website" will appear. This is useful for providing context or additional information about the link.
