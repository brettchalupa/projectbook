# Simple Podcast Hosting

Bring Your Own Hosting Podcast Tool

Podcasts are a truly wonderfully simple format. They leverage a feed, usually RSS, that can be consumed by clients who check regularly for new episodes and then add them to a library for a user to listen to.

The RSS feed contains the episodes and a link to the audio file and a bunch of metadata.

So what if there was a simple way to build and host a podcast RSS feed and files (and any other files, like a simple website) all from the command line without using a hosting platform?

It's sort of like the [Static Site Generator] but more focused on podcasts in particular and less on written content in Markdown.

## Spec

Directory contains something like:

```
podcast.toml
assets/
  audio/
    1-title-slug-here.mp3
  images/
    1-title-slug-here.jpg
    artwork.jpg
episodes/
  1-title-slug-here.toml
  2-title-slug-here.toml
  3-title-slug-here.toml
README.md
```

The `podcast.toml` contains the global show details and info.

When the program is run, let's say it's called `podbud build` or something like that, then it would generate a `_build` directory that contains the RSS feed, the audio and image assets, and the episode TOML files.

The program would then have support for something like `podbud deploy` that would push the generated directory to something like Amazon AWS S3 or your own server or whatever for public consumption.

The process and flow would be ideal for using with some sort of CI service that builds and deploys whenever the show source is pushed somewhere or an episode is marked as published.

`show.toml`:

``` toml
title = "Roderick on the Line"
description = "Merlin Mann's frank & candid weekly phone call with John Roderick of The Long Winters"
url = "http://www.merlinmann.com/roderick/"
artwork = "assets/images/artwork.jpg" # defaults to this
language = "en"
# more of the required ones
```

an `episode.toml`:

``` toml
title = "Episode 00: Suit of Vomit"
publish_date = # proper format
description = """
Our pilot episode.

Steak, Babies, Hitler, Molecules, Hearing Loss, and the Best of the Liberal Arts.

Pretty much what you’d expect.
""" # supports Markdown, HTML, or just plain ole text
```

[TODO: flesh out all of the details and those that are supported]

## References

- https://help.apple.com/itc/podcasts_connect/#/itcb54353390
- https://podcasters.apple.com/support/823-podcast-requirements
- http://feeds.feedburner.com/RoderickOnTheLine
- https://toml.io/en/

## Concepts

- RSS feed generation
- Reading from file system

## Technologies

I'm particular interested in using Rust and TOML for this as I think it'd make it nice and portable. Go would be a good fit too, but really any general purpose programming language would work.

## Stretch Goals

- Support different hosts and make it configurable
- Add commands to CLI for creating an episode file
- Add support for an audio compressor/processor into the publishing chain to reduce audio file size load
- GUI that makes it even easier to work with and manage ones podcast.
- Add the ability to render the episodes on a website with a page for each episode and a general layout (maybe parse the RSS feed or just do it as part of the RSS building process)
- Newer Podcast metadata attrs