# Comic Reader

The gist: build a program that opens up a zip file of images (without extracting them) and allows the user to flip to the next page until the end of the archive.

DRM-free comic files are generally found in a few different archive formats:
- `.zip` -- just a zip collection of images
- `.cbz` -- just a zip file, from my understanding
- [rar one???]

And then within could be any number of image formats. JPGs, PNGs, even TIFFs.

What this project exercises:

- Inspecting the contents of an archive file
- Rendering images potentially in a variety of formats
- Handling user input to go the next page or previous page


[link to examples of free comics in the format]

[examples of the UI or wireframes]

This project is pretty GUI heavy but has the added complexity of viewing the image files within the archive.

Some ideas for tooling, technology, and platforms:
- iOS/iPad OS/MacOS -- a really good project for learning Swift on those platforms
- Android -- I think a pretty good project for that, like learning Kotlin
- Desktop GUI app -- something like GTK or QT would make a good fit or even Vala or rust-gtk (check name)
- Electron -- this would be a pretty fun little desktop project for Electron if you're a web dev interested in learning how to use it. You could leverage your web skills while learning that.

You could leverage a library to open up an archive and view the files or you could code that yourself using the language's standard library. There's lots of deep dives that could be done here.

## Edge Cases

- What happens if the archive doesn't contain any images?

## Optimizations

- Is the archive being loaded into memory or is there a way to load only the current image into memory?

## Stretch Goals

- Support PDFs since some comics and books are in PDF format
- Make the UI be able to be changed in size while maintaining the original aspect ratio of the page
- Browse mode that renders thumbnails of all of the pages for easy browsing
- Displaying a prompt to open the next archive in the directory when the end of the current file is reached (i.e., read the next issue)
- Single page view vs side-by-side spread view
- Support reading right to left instead of left to right for comics like manga
- Big stretch goal: library that manages comics that have been imported or that exist within a directory and keep track of those that have been read and those that haven't