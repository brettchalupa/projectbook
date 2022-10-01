# SSG GUI

**The gist**: build a desktop application for managing the content of a static site generator.

I've never been more ashamed of myself for titling something "SSG GUI" but here I am. Ashamed. And with a title of something called SSG GUI.

Hold your horses for a minute before you throw your reading device in the trash at the gall of someone to create anything with a title as obtuse and terrible as SSG GUI.

I actually think this is a really good idea. Hear me out.

There are at least a million static site generators. There's probably not a great reason for having so many, but it seems like it's the proving ground for any modern language to have a fast SSG. Overall, I love SSGs, especially as a developer who spends a lot of time thinking in plain-text. To have a lightweight website tool that generates files that can be hosted pretty much anywhere without having to manage a database and server is fantastic.

But command line SSGs aren't the most friendly thing in the world, even though I think a lot of people would be interested in authoring content in Markdown and publishing their website using one. What if it was possible to do that without the need for the command line?

I think wrapping a static site generator in a GUI would be possible _and_ valuable. The GUI would essentially be a Markdown editor that sites on top of the sites files. The app could use Git under the hood for creating and managing versions. Hosting and deploying could be configured for the host of choice, all within the GUI. Image uploads would be as simple as copying the selected into the proper directory and referencing it with Markdown. And! If the person ever wants to look under the hood and modify things directly, they could, since I think this GUI would aim to maintain full compatibility with whatever SSG it sits on top of.

There's a lot here to process! Maybe something like this already exists. I sort of don't want to know. Even if it does, it'd still be a great learning exercise.

## Mock-Ups

TODO

## Concepts

- Integrating with an existing command line tool/library
- A mildly complex GUI
- Publishing

## Spec

TODO

## Tech of Interest

gtk-rs + Zola

## See Also

- [Static Site Generator](../command-line-interfaces/static-site-generator.md)
