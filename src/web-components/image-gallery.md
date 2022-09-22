# Image Gallery

The idea here is to take a folder of images or a collection of links to images and render them in a grid and then be able to tap a given image to view a large version of it.

When viewing a single image, the user could use the left and right arrows to progress through the images in the gallery.

Learning areas:

- Rendering images
- Grid rendering
- State changing from grid to single image viewing
- Handling user input, from tapping to keyboard

Platforms/Tools/Technology:

- Web would be good! You could take a collection of URLs. I think it'd make a particular good web component that anyone could drop in and use. Something like:

```html
<image-gallery>
  <img src="https://example.com/foo.jpg"/>
  <img src="https://example.com/bar.jpg"/>
</image-gallery>
```

Or the data could be passed in through a property. Really up to you there.

- Desktop/mobile -- desktop would prob be a little easier since accessing the file system isn't as cumbersome as on mobile apps, but still possible on things like iOS and Android for sure!


[wireframes]

[examples]

Need a zip of images? Okay, here ya' go!

## Stretch Goals

- Support a bunch of different image formats like .TIFF, .PNG, .JPG, .BMP, .WEBP, the iPhone one
- Play / pause to cycle through the images on an interval, maybe someone wants to display their favorite photos on rotation like a digital picture frame
- Web
  - Support captions and alt text
