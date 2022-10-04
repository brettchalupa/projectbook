# Content Management System (CMS)

**The gist**: build a web app that allows people to define a content model and create records that follow it.

Ah, yes, the good ole Content Management System. Nearly as generic as the todo list and similarly as elusive in terms of finding an actually good one. But they are fun to build because they're essentially like a more complex [blogging platform](./blogging-platform.md) and something most businesses (and people) find they need at some point or another.

To me, a CMS does more than allowing blog posts or pages to be defined. It allows the actual data model to be defined. This is mildly complex, as you have to have composable chunks (fields) that can be put together and then used to build the Admin GUI for managing the content. This is really powerful.

This essentially allows people to build complex, content-driven websites. The platform would have less of a focus on the design of the website and more on being able to create user-configured forms for the data.

## Specs

- User authentication
- Authorization for access
- Define content models
- Users can manage data for the configured content models
- Render public site based on the created content

## Extra Credit

- Templates for commonly used content models
- Optional and required fields

## References

- [Contentful](https://www.contentful.com/)
- [Drupal](https://www.drupal.org)
