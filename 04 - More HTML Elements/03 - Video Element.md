# Video Element

Just like the `<audio>` element, the `<video>` element is an element that has a JavaScript API that allows you to control the video. The `<video>` element is used to embed video content in an HTML document.

The `<video>` element has a number of attributes that can be used to control the video, such as `autoplay`, `controls`, `loop`, `muted`, `preload`, and `src`.

Here is a simple example:

```html
<video src="./video1.mov" controls type="video/quicktime"></video>
```

We need controls in this example to be able to play the video. The `type` attribute is optional, but it is recommended to include it to help the browser determine the type of video file.

### autoplay

The `autoplay` attribute is a boolean attribute. When present, the video will automatically start playing as soon as it can do so without stopping to finish loading the data. We don't need controls in this example because the video will start playing automatically. However, if you want to stop the video, you will need to use JavaScript to control the video.

```html
<video src="./video1.mov" controls autoplay></video>
```

### loop

The `loop` attribute is a boolean attribute. When present, the video will automatically start playing again when it reaches the end.

```html
<video src="./video1.mov" controls loop></video>
```

### muted

The `muted` attribute is a boolean attribute. When present, the video will be muted. The volume will be grayed out in the video player.

```html
<video src="./video1.mov" controls muted></video>
```

### figure & figcaption

The `<figure>` element is used to group media content, such as images, videos, and code snippets, with a caption. The `<figcaption>` element is used to define a caption for the `<figure>` element.

```html
<figure>
  <video src="./video1.mov" controls></video>
  <figcaption>Video 1</figcaption>
</figure>
```
