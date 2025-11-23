# Meta Tags & Search Engines

In this lesson, we are going to look at meta tags. These are essential elements in HTML that provide metadata about a web page or about the content of a web page. They are not visible on the web page and they're placed within the head tags. Search engines utilize meta tags to understand the content of a web page and they can even play a role in search engine optimization (SEO), determining how your page appears in search engine results.

Back in the early 2010s, meta tags held a lot of weight when it came to search engine rankings. For example, keywords were really importat when it came to where you site ranked. These days keywords don't hold any weight in terms of placement, but they do still inform the search engines what is on that page.

Title tags do still hold some weight as they're what is displayed in the results along with the meta description. SEO has it's own science and is different scope than what this course is about, but just know some of this stuff can play a role.

So we're gonna look at some of the common meta tags. I'm definitely not going to go over all of them. There's actually a lot of obscure ones, but we'll look at the ones that you should use. We'll go over them within the slide and then we'll jump into the sandbox.

## Charset Meta Tag

The charset meta tag specifies the character encoding for the HTML document. It is essential to include this tag to ensure that the browser displays the text correctly. The HTML5 specification encourages web developers to use the UTF-8 character set, which covers almost all of the characters and symbols in the world! It is recommended (but not required) that the meta charset tag be the first child tag of the head element.

```html
<meta charset="UTF-8" />
```

In this case, we are using the attribute 'charset' and setting it to UTF-8. Most meta tags use a name and content attribute. This one doesn't though.

## Viewport Meta Tag

The viewport meta tag controls the layout of the web page on different devices and screen sizes. It's important for creating responsive web designs that work well on mobile devices. Responsive design means the layout responds to whatever screen size it's being viewed on and is one the most important parts about web design and frontend development. So this tag is neccesary for all pages.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

There are two attributes being used here and those are `name` and `content`.

The `name` attribute is used to specify the purpose of the meta tag, in this case, indicating that it controls the viewport. The `content` attribute is where specific instructions or settings for the viewport are provided. In this case, it is defining the width of the viewport to the width of the device. Then it's setting the initial zoom level to 1.0 (initial-scale=1.0). This ensures that the webpage will be displayed at the correct width on all devices, without any unwanted zooming or scaling applied by default. It's a fundamental part of creating responsive web designs. If you've ever went to a website on a mobile device and had to scroll sideways to see the entire layout, chances are, that website didn't have the correct initial scale and didn't have this meta tag.


Don't let these tags overwhelm you because you actually don't even need to remember these or type them out. We can use a tool called **Emmet** to generate these tags along with a basic structure of html, head and body tags in Visual Studio Code. I am going to give you a crash course in Emmet once we talk a little bit more about HTML tags in general.

The next few tags are not mandatory, but they can help search engines understand the content of your web page.

## Description Meta Tag

The description meta tag provides a brief description of the page. This description is often displayed in search engine results to give users an idea of what the page is about. It should be concise and relevant to the content of the page.

```html
<meta
  name="description"
  content="Learn HTML, CSS, and JavaScript with our beginner-friendly tutorials."
/>
```

The description meta tag should be unique for each page and accurately describe the content of the page. It should be around 150-160 characters long.

## Keywords Meta Tag

The keywords meta tag used to be a critical element for SEO, but it has lost its importance over the years. Search engines no longer use this tag to determine the content of a page. However, it doesn't hurt to include it with relevant keywords.

```html
<meta name="keywords" content="HTML, CSS, JavaScript, web development" />
```

The keywords meta tag should contain a list of 4-10 relevant keywords separated by commas. It's best to keep it short and focused on the main topics of the page.

## Author Meta Tag

The author meta tag specifies the author of the page. It's a good practice to include this tag to give credit to the author and provide additional information about the content.

```html
<meta name="author" content="John Doe" />
```

You can replace "John Doe" with the actual name of the author. This tag is not used by search engines but can be helpful for users who want to know more about the author.

## Robots Meta Tag

The robots meta tag controls how search engines index and display the page. It can be used to prevent search engines from indexing the page or following links on the page.

```html
<meta name="robots" content="index, follow" />
```

The `index` value tells search engines to index the page, while the `follow` value tells search engines to follow links on the page. You can use `noindex` and `nofollow` values to prevent indexing and following links.

There are other tags as well, but these are the most important ones.
