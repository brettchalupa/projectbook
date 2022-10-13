# Image Gallery

The idea here is to take a folder of images or a collection of links to images and render them in a grid and then be able to tap a given image to view a large version of it.

When viewing a single image, the user could use the left and right arrows to progress through the images in the gallery.

## Mock-Ups

![Mock-ups of image gallery grid and single image display. The former has a heading and a two-column grid of images with captions. The latter a larger image, caption and previous/next buttons](./img/image-gallery.webp)

## Spec

```html
<ig-gallery>
  <ig-img src="https://example.com/foo.jpg" alt="description of image" />
  <ig-img src="https://example.com/bar.jpg" alt="description of this image" />
</ig-gallery>
```

## Concepts

- Rendering images
- Grid rendering
- State changing from grid to single image viewing
- Handling user input, from tapping to keyboard

## Resources

Need a zip of images? Okay, [here's a zip of four images you can use](./photos.zip).

## Stretch Goals

- Play / pause to cycle through the images on an interval, maybe someone wants to display their favorite photos on rotation like a digital picture frame
