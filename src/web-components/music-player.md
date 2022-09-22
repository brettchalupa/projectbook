# Music Player - Web Component

HTML5 has some rich APIs for interacting with audio. A web component that takes children that are audio files and then can play through them and handle common functionality like:
- Play
- Pause
- Volume
- Next/previous song
- Pick and play a track
- Play the next song in the list

[audio files]
[wire frames]
[icons]

## Concepts

- HTML5 audio API
- Rendering the GUI for listing the tracks
- Rendering the GUI for the actual player
- Callbacks for various audio events

## Spec

This could be something like this:

``` html
<music-player>
  <mp-song>
    <source src="horse.ogg" type="audio/ogg">
    <source src="horse.mp3" type="audio/mp3">
  </mp-song>
</music-player>
```

## Tech

Lit and Stencil and Svetle interest me in particular for this. I think it'd need to be easy to load into any given web page or app.

## Stretch Goals

- Easy download for the files if someone enjoys them