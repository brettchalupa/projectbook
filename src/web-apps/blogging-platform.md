# Blogging Platform

**The gist**: Allow users to author long form content in Markdown and render the posts as web pages.

Ah, is there anything more generic than a blogging platform? Well, I guess a todo list. But there's something about blogging and blogging tools that I always go back to and find comforting. It must be something about the joy of publishing something online with relative ease.

This project is great for those learning a language and/or a framework and who would be interested in maintaining their own blog. The data model is often pretty simple for getting started, and you can always expand it and add functionality as you need it.

I'd focus just on text to start. Text can get you a long way. Then explore things like uploading and hosting images, that sort of thing.

If I were to build this project, I'd call it **Blogbud** or something like that. Are you sick of the *bud names throughout _Projectbook_? Well, I'm not yet. Sorry.

## Mock-Ups

Here's what a simple interface for managing posts and then viewing a post could look like:

![Blogbud mock-up](./img/blogbud.webp)

## Specs

The following features would be nice to have for the basics:

- Authentication for users (a.k.a. someone signs up)
- Blog creation
- Post creation for a blog
- Post editing
- Post deleting
- Viewing a post as a reader

### Data Model

Here's a simple outline of what the data model could be like:

- **Posts**
  - blog_id — the blog it belongs to
  - created_at
  - published_at
  - updated_at
  - title
  - slug
  - body
  - authors/users association
- **Blogs**
  - name
  - description
  - authors/users association
- **Users**
  - email
  - encrypted_password
  - name
  - photo

## Concepts

- Authentication
- Admin for authoring and managing posts
- Rendering Markdown as HTML
- Access control/permissions/authorization

## Extra Credit

- Allow posts to created as drafts but not yet published
- Schedule posts to be published in the future
- Generate an RSS and/or Atom feed for the posts
- Support image and other file uploads in the post body
- Support attachments to the post object
  - Images for rich sharing data
  - Audio files (with a special RSS feed) and you've got a podcast!
- Allow posts to be tagged for readers to browse posts by tag
- Add an easy mechanism to allow readers to heart a post to show they enjoyed it
  - Unique it by IP or something along those lines
- Support multiple blogs for a given user
- Image uploads
- Caching the pages or even generating a static site
- Search

## References

- Wordpress
- Ghost

## See Also

- [SSG GUI](../general-graphical-apps/static-site-generator-gui.md) — building an app as an interactive front-end for a static site generator, sort of like the Admin aspect of the blog web app project
- [Web Comic Platform](./web-comic-publishing-platform.md) — similar in nature but more focused on hosting image content rather than the written word
