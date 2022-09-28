# Video Player

**The gist**: build out a video player component that makes use of the browser APIs to control the video.

I picture this as building a UI for dealing with a video, a lot like YouTube's or Vimeo's player. It would allow you to pause the video, change the volume, scrub to a specific timestamp, and make the video fullscreen.

The native video player is fine in most operating systems and browsers, but that doesn't mean more functionality couldn't be added. Also, we're here to learn!

## Spec

```html
<video-player src="/path/to/video.mp4" />
```

## Concepts

- UI
- Events
- Working with media

## Resources

- [MDN docs on the `<video>` embed element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)

## Reference

YouTube player:

![youtube player](./img/youtube.webp)

![vimeo player](./img/vimeo.webp)

## Extra Credit

- Buttons for 10s back, 10s forward
- Make the video display responsive
- Support multiple video formats and choose what to play based on browser and OS support

## See Also

- [Music Player](./music-player.md)
