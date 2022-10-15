# Linkbud

**The gist**: build an app that allows users to define lists of links that can be viewed publicly on the web.

This is useful for people linking to various profiles on social media, sharing an album on multiple streaming services, or even serving as a simple home page for someone. Sometimes referred to as "Link in Bio" sites, I think they're pretty nifty as simple directories people create for their projects.

## Mock-Ups

Here's what the user interface and user experience could be like:

![Linkbud mobile mock-ups. First view: horizontally-aligned title/logo and user button; list of link lists each with a view link, edit link and visibility indicator; "Add a Link List" button. Second view: "Create a Link List" form; inputs for name, description and slug, plus a repeatable group of inputs for each link (name and URL); "Add a Link" and "Create" buttons. Third view: public view with the list title, a short description, a list of styled links, a reference to the platform and a link to follow the list creator on the platform](./img/linkbud.webp)

When a user is signed in, they can view a list of their Link Lists. They can edit their existing ones or add a new one. The form has fields for everything that'd could be entered. And then when they create (or update) a Link List, they can view the public link on the web with the rendered links.


## Specs

Users should have the ability to:

- Sign up / sign in
- Create a list of links with a name
- Add, edit, delete, and reorder links on their list
- View the list publicly based on account and list slugs
- Support multiple lists for an account

## Concepts

- Authentication
- Authorization (access control)
- A non-trivial UI
- Data modeling
- Rendering a web page from user entered data

## Stretch Goals / Extra Credit

- Add description with a rich text editor or Markdown support to lists to give more context
- Display icons for links to common locations like YouTube, Twitter, Reddit, etc.
- Upload an image for a list
- Email verification if signing up via email
- Sign up / sign in via a third-party service like Twitter, Facebook, Google, etc.
- Customize the list's display with a photo, colors, font, etc.
- Support deleting a list or making a list private
- Ensuring the URLs are properly formatted
- Sanitizing input for potential non-safe data

## References

- [Linktree](https://linktr.ee)

## See Also

- [Link List](../websites/link-list.md) — not quite ready for a full stack web app? That's okay! What if you instead just build a static website?
