# Iframes

The `<iframe>` element is used to embed another document within the current HTML document. This is useful for embedding maps, videos, and other content from other websites.

Let's look at a few examples:

## Youtube Video

You can embed youtube videos by using the `<iframe>` element. The URL should be the embed code for the video, which looks like this: `https://www.youtube.com/embed/video_id`. Here is an example:

```html
<iframe
  width="500"
  height="315"
  src="https://www.youtube.com/embed/8sXRyHI3bLw"
>
</iframe>
```

## PDF Files

You can also embed PDF files using the `<iframe>` element. Here is an example:

```html
<iframe width="500" height="315" src="./invoicesample.pdf"></iframe>
```

## Web Pages

You can embed other web pages, but it depends on the Content Security Policy (CSP) of the website. If the website allows embedding, you can use the `<iframe>` element to embed the page. You can also embed local pages, such as the following:

```html
<iframe width="500" height="315" src="./test.html"></iframe>
```

## Google Maps

You can embed maps using the `<iframe>` element. The URL should be the embed code for the map. Here is an example:

```html
<iframe
  width="500"
  height="315"
  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3152.0000000000005!2d-122.0841926846827!3d37.42240897982596!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x808f7e3f0b0b8a3d%3A0x7f3f7e3f0b0b8a3d!2sGoogleplex!5e0!3m2!1sen!2sus!4v1605720000000!5m2!1sen!2sus"
></iframe>
```

## Google Calendar

Google Calendar also allows embedding. Here is an example:

```html
<iframe
  width="500"
  height="315"
  src="https://calendar.google.com/calendar/embed?src=en.usa%23holiday%40group.v.calendar.google.com&ctz=America%2FLos_Angeles"
></iframe>
```

## `<embed>` Element

There is also an `<embed>` element, which is used to embed content from other pages and websites. Here is an example of using it for a YouTube video:

```html
<embed
  width="500"
  height="315"
  src="https://www.youtube.com/embed/8sXRyHI3bLw"></embed>
```

## `<object>` Element

The `<object>` element can also be used. Here is an example:

```html
<object
  width="500"
  height="315"
  data="https://www.youtube.com/embed/8sXRyHI3bLw"
></object>
```

Of the 3, the `<iframe>` element is the most versatile. It can be used to embed any type of content, but it is also the most complex. The `<embed>` and `<object>` elements are simpler to use but are more limited in their capabilities. The `<object>` element is also deprecated. I can't really think of a reason why you would use it, but I wanted to share it so you know that it exists.
