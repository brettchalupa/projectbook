# Story Publishing Platform

**The gist**: build an application that allows writers to publish their stories online.

As a writer of all sorts of words, from short stories to novels to poems, I'd love an open platform and community for sharing my stories online. This is also a great project for learning because it's got similar needs to a [blogging platform](./blogging-platform.md) but a bit more complex.

I also think a community-supported, ad-free, open-source platform for something like this could thrive!

I call this idea **StoryHub**.

## Mock-Ups

![StoryHub mock-ups](./img/storyhub.webp)

## Specs

Even if the accounts are the same, I think there are two distinct usecases here. One for the writer who publishes stories. And one for the reader experience.

### Writer

- Create books
    - Title
    - Description
- Add chapters to a story (and edit and delete)
    - Title
    - Body of Markdown

### Reader

- Read stories
- Navigate between chapters

## Thoughts on Tech

I really think this project would benefit from being driven by an API and being built with the idea of supporting multiple clients. Reading on a mobile device with an app is a great experience. As can reading on the web. I'd build this with a GraphQL API.

Because the UI needs are ultimately pretty simple (centered around rendering long-form text), it could also be a good project for experimenting with tools like React Native, Ionic, etc.

## Extra Credit

- Image upload for a book
- User photos
- Support additional metadata for a story (tags could be nice, license too)
- Reorder chapters
- Generate RSS feeds for a given book and author
- Easily export epub and PDF versions of stories
- Reader account feaders
    - Follow stories and/or authors
    - Feed of new chapters for followed stories
- Mobile apps for reading (and even authoring)
- Tipping support or Patreon integration

## Concepts

- Authentication
- Authorization
- Content authoring and publishing
- Content-driven UI

## References

- [Wattpad](https://www.wattpad.com)

## See Also

- [Prose Renderer](../web-components/prose-renderer.md)
