# Website Builder

**The gist**: Build out a web app that lets users create simple web pages graphically with no coding knowledge. This allows people to build simple web pages with a variety of content to meet their needs.

This is a complex project with the need for a really rich front-end experience for it to feel smooth. It's a good project for learning a front-end web framework.

Blocks to start with:

- Header
- Text with Markdown
- Image
- YouTube Embed
- Button

Ideally blocks would be able to be reordered within a given page.

The selected blocks for the page would get persisted in a database associated with the user's site.

And then, finally, that page would be able to be rendered and viewable in the browser.

## Mock-Ups

![Website builder mobile mock-ups. First view: top row with site and platform name; second row with "Add Page" heading and "Save" button; title field; block editor block with title, text and image options; "Add Block" button. Second view: a block has been added after clicking the button. Third view: an image selection input has replaced the top block editor block. Fourth view: rendered page with site name, menu button, page title, image, main content and platform reference](./img/sitebud.webp)

## Specs

- Sign up for an account
- Create a site
- Add pages
- Add blocks to pages
- Public can view pages rendered from the configured blocks

## Concepts

There's so much here!

- Defining a data model for the blocks, which is decently complex
- Storing the built pages which have a pretty complex data model
- Building a complex UI
- Rendering a complex page from stored data that needs to be processed properly
- Authentication
- Authorization

## Extra Credit

- Configurable menus
- Add more block types
  - Audio
  - Rich text editor
  - List
    - Ordered
    - Unordered
  - Code
  - Contact form
  - Image gallery
  - Other embeds
- Page visibility like public, draft, password protected

## Reference

- [Gutenberg, Wordpress's editor](https://wordpress.org/gutenberg/)

## See Also

- [Content Management System](./content-management-system.md) — similar in concept
