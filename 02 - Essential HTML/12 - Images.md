# Images

There are many cases where you will want to add images to your website. Images can be added as background images through CSS, or as content images using the `<img>` tag. In this lesson, we will the `<img>` tag and later learn how to add background images.

The `<img>` tag is used to embed images in an HTML document. It is an empty element, meaning it does not have a closing tag. The `<img>` tag has two required attributes:

- `src`: Specifies the path to the image file.
- `alt`: Specifies an alternate text for the image, in case the image is not displayed.

Here is an example of how to use the `<img>` tag:

```html
<img src="path/to/landscape.jpg" alt="alternative text" />
```

The slash in the closing tag is optional. This was required in XHTML, which is an older version of HTML. In HTML5, the slash is optional for void elements like `<img>`, `<br>`, and `<hr>`. You can include it if you prefer, but it is not necessary. I actually prefer to include it because it makes the code more consistent so my editor is set to automatically include it. It's perfectly fine to leave it out though.

The `src` attribute is used to specify the path to the image file. This path can be a relative path or an absolute path. A relative path is a path that is relative to the current file, while an absolute path is a full URL to the image file.

The `alt` attribute is used to provide alternative text for the image. This text is displayed if the image cannot be loaded, or if the user is using a screen reader to access the content. It is important to provide descriptive alternative text for images to ensure accessibility.

Here is an example of an image tag with a relative path:

```html
<img src="images/landscape.jpg" alt="A beautiful landscape" />
```

Usually, when you build your websites, you will have a folder called `images` or `img` where you store all your images. In this case, the image file is located in the `images` folder and is named `landscape.jpg`. It could also be a `.png`, `.gif`, or other image file formats.

And here is an example of an image tag with an absolute path:

```html
<img src="https://picsum.photos/200/300" alt="A cool photo" />
```

**Lorem Picsum**is a service that provides placeholder images for testing purposes. You can specify the width and height of the image by adding them to the URL. In the example above, we are requesting an image with a width of 200 pixels and a height of 300 pixels.

## Image Width and Height

Images can also take the `width` and `height` attributes to specify the dimensions of the image. These attributes are optional, but they can be useful for controlling the size of the image on the page. You can also use CSS to control the size of the image, which we will cover in a later lesson.

Here is an example of how to use the `width` and `height` attributes:

```html
<img
  src="images/landscape.jpg"
  alt="A beautiful landscape"
  width="200"
  height="150"
/>
```

You can also add a `title` attribute to provide additional information about the image. The `title` attribute is displayed as a tooltip when the user hovers over the image.

Here is an example of how to use the `title` attribute:

```html
<img
  src="images/landscape.jpg"
  alt="A beautiful landscape"
  width="200"
  height="150"
  title="A beautiful landscape with mountains and a lake"
/>
```

# `figure` & `figcaption` Tags

Use a `<figure>` element to mark up a photo or other media in a document, and a `<figcaption>` element to define a caption for the media:

```html
<figure>
  <img src="./landscape.jpg" alt="Image" style="width: 100%" />
  <figcaption>Fig.1 - Beautiful Landscape</figcaption>
</figure>
```

The content is self-contained, typically referenced as a single unit from the main flow of the document, and can be moved away from the main flow of the document without affecting the document's meaning.
