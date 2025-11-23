# Audio Element

HTML5 brought us a few really cool media tags including the `<audio>` tag. This is more than just a tag, it is an element that has it's own JavaScript API. There are different events and methods that are associated with this element so you can create your own custom audio players. etc. That goes beyond the scope of this course, but we can still use the `<audio>` tag to embed a player in the browser to play sound files.

Add the following HTML:

```html
<audio controls src="./song1.mp3" type="audio/mp3"></audio>
```

This will show an audio player with controls. The `src` attribute is the location of the file. I have included a music file called `song1.mp3` in the sandbox folder. The `controls` attribute is what shows the UI. If we leave off that attribute, we will not see the interface. The type attribute is optional, but it is good practice to include it. It tells the browser what type of file it is.

You can also include the source in a nested `<source>` tag. This is useful if you want to include multiple sources for different browsers. Also, you can put some text for browsers that do not support the audio tag.

```html
<audio controls>
  <source src="./song1.mp3" type="audio/mp3" />
  <!-- Fallback content for older browsers -->
  <p>
    Your browser does not support the audio element. Please use a modern browser
    to listen.
  </p>
</audio>
```

### autoplay

You can add the `autoplay` attribute and the song will play automatically. You can even remove the `controls` attribute and it will just play.

```html
<audio controls autoplay src="./song1.mp3"></aud
```

### loop

You can set the `loop` attribute to have the song play over and over.

```html
<audio controls autoplay loop src="./song1.mp3"></audio>
```

### figure & figcaption

We can use the `<figure>` and `<figcaption>` tags to add a caption to the audio player.

```html
<figure>
  <figcaption>Listen to the song:</figcaption>
  <audio controls src="./song1.mp3"></audio>
  <a href="./song1.mp3"> Download audio </a>
</figure>
```
