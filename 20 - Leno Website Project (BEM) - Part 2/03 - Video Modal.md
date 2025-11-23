# Video Modal

Now we want to be able to click the button and show a video from YouTube in the modal. The video itself does not matter. I am just going to use my web dev guide from my channel.

## HTML

Let's add the HTML for the modal. You can put this right above the preview section:

```html
<!-- Modal -->
<div id="videoModal" class="modal">
  <div class="modal__content">
    <span class="modal__close-button">&times;</span>
    <iframe
      id="videoPlayer"
      width="560"
      height="315"
      src=""
      frameborder="0"
      allowfullscreen
    ></iframe>
  </div>
</div>
```

We are creating a modal with a close button and an iframe for the video. The iframe is empty because we are going to add the video source with JavaScript.

## CSS

Let's add the CSS for the modal:

```css
/* Modal */
.modal {
  /* display: none; */
  position: fixed;
  z-index: 999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent background */
}

.modal__content {
  background-color: rgba(0, 0, 0, 0.5);
  margin: 10% auto;
  padding: 20px;
  border: 1px solid #888;
  border-radius: 10px;
  max-width: 600px;
  position: relative;
}

.modal__close-button {
  position: absolute;
  top: 10px;
  right: 20px;
  font-size: 40px;
  cursor: pointer;
}
```

We will keep the display of the modal as `none` for now so that we can see it. We are positioning the modal to the top left corner of the screen and making it full screen. We are also adding a semi-transparent background to the modal.

## JavaScript

Now let's add the JavaScript to open the modal when we click the play button. We want this inside of the event listener for when the DOM is loaded. Your entire JS file should look like this:

```javascript
document.addEventListener('DOMContentLoaded', function () {
  // Get hamburger button and mobile menu items
  const toggleButton = document.querySelector('.navbar__mobile-menu-toggle');
  const mobileMenu = document.querySelector('.navbar__mobile-menu-items');

  // Add click event listener to toggle mobile menu visibility
  toggleButton.addEventListener('click', function () {
    mobileMenu.classList.toggle('active');
  });

  // Video modal functionality
  const modal = document.getElementById('videoModal');
  const videoButton = document.querySelector('.preview__video-button');
  const closeButton = document.querySelector('.modal__close-button');

  // Open the modal when the button is clicked
  videoButton.addEventListener('click', function () {
    modal.style.display = 'block';
    // Replace the src attribute of the iframe with your video URL
    document.getElementById('videoPlayer').src =
      'https://www.youtube.com/embed/8sXRyHI3bLw';
  });

  // Close the modal when the close button is clicked
  closeButton.addEventListener('click', function () {
    modal.style.display = 'none';
    // Pause the video when the modal is closed
    document.getElementById('videoPlayer').src = '';
  });

  // Close the modal when clicking outside of it
  window.addEventListener('click', function (event) {
    if (event.target == modal) {
      modal.style.display = 'none';
      // Pause the video when the modal is closed
      document.getElementById('videoPlayer').src = '';
    }
  });
});

// Change navbar background color on scroll
window.addEventListener('scroll', function () {
  var navbar = document.querySelector('.navbar');
  if (window.scrollY > 0) {
    navbar.classList.add('navbar--transparent');
  } else {
    navbar.classList.remove('navbar--transparent');
  }
});
```

When we click the play button, the modal will open and the video will start playing. When we click the close button or click outside of the modal, the modal will close and the video will stop playing.

Now uncomment the `display: none;` property in the CSS file for the modal. You should now be able to click the play button and see the video in the modal.

It should look like this:

<img src="../images/leno-video-modal.png" />

## Responsive Design

On small screens, we want the video to be full width. Add this to the `768px` media query:

```css
.modal__content {
  margin: 40% auto;
  padding: 10px;
  width: 90%; /* Adjust width to fit smaller screens */
}

.modal__content iframe {
  width: 100%;
}
```
