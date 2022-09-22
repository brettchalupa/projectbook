# Static Site Generator

There are _so_ many of these. Nearly every modern language has one. It's largely a solved problem, but I bet there's still some space for innovation and experimentation. Plus, it's a really great learning project.

There's basically no GUI. It's a command line app. Or well I guess you could have a GUI, that'd be a unique offering that most of the static site generators don't offer since their command line apps. 

But the gist is that a static site generator takes a collection of text files and generates HTML pages that form a website. There's usually some form of processing from the input language to HTML (parsing) and then handling the templating.

You could only use the standard library for this or make use of existing packages by other developers. Whatever you want to learn.

But the output of the command would be site's HTML and any other assets that are needed and could then be deployed to a server and accessed.

There's also usually a need for specifying metadata as part of a given file.

The benefits of a static site generator is that the people building the site can author the content in a friendly, less cumbersome format than HTML like Markdown. And then the generated files can be hosted pretty much anywhere. You don't need to run a server yourself and deal with various requests. 

Let's say the tool is called `ssg` and you had a folder with the following files for a band website:

```
index.md
about.md
albums.md
tour.md
merch.md
```

When you run `ssg .` or just `ssg` it takes those files, converts them to HTML, and outputs them into the `build` directory or `site` dir or `_build`. Whatever you want to call it. Then that folder could be pushed somewhere for access.

There'd be:

```
build/
  index.html
  about.html
  albums.html
  tour.html
  merch.html
```

And they'd be rendered with the proper semantic HTML with support for speciying metadata for the page. Starting with `title` and the meta `description` is enough to get started!

## Concepts

- Reading files from the file system
- Processing them with some sort of language
- Writing the files to the disk
- Command-line interface

## Features

- Markdown (or whatever) in
- HTML out
- Layout with a templating language that the Markdown for each page gets rendered in
- Ability to specify metadata for a given page like `title` and the meta description

## Stretch Goals

- Support external CSS and JS, maybe even processors for those like Sass and TypeScript
- Add support for a server command, like `ssg serve` that watches for changes to the site on the filesystem, regenerates the site, and then serves the build dir over HTTP
- Handle multiple input types and processors or define your own mark-up language! That'd be fun

## References

- Jekyll
- Zola
- Hugo
- That JAMStack website

## Examples

- [Soy](https://github.com/brettchalupa/soy) -- a functional but barebones static site generator I made in Ruby; I had intentions for it being more finished, but a useful exercise in learning
