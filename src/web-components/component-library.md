# Component Library

**The gist**: build a collection of web components for common rendering needs in any given website.

When building out websites and web apps, there are some really common needs that basic HTML doesn't give you out of the box. The goal with this project is to extend HTML by giving developers some more of the commonly used elements. The library should be responsive, provide sensible defaults, be easy to override, and semantic.

Historically, Bootstrap or Foundation accomplish similar tasks: provide styles and JS for commonly used patterns in websites. They work fine and are widely used, but they're pretty brittle. You have to rely on having just the right DOM structure and classes for it to work.

What if instead all someone had to do to get an image gallery was use the `<cl-gallery>` tag or to get a card display they use `<cl-card>`? That'd allow the component library (cl) to provide the needed defaults with the ability for them to be overriden or themed as needed.

In many ways, this project is about creating a generic-ish design system for building websites and web applications.

## Spec

Here are some of the foundational components I'd add:

- The other components in the Web Components section of _Projectbook_, of course!
- Button
- Card
- Navigation menu
- Grid
- Inputs & related form elements

## Resources

- [Shoelace](https://shoelace.style) — an open source component library built using Lit
- [Atlassian Design System](https://atlassian.design/components) — component library built using React

## Extra Credit

- Add more components, like `<cl-icon>` for easy icons
- Ensure styles can be overidden easily to customize it. CSS variables would be a good fit for this!
- Write (or auto-gen) documentation for the components
- Build out some websites and web apps using it! See it feels and what could be improved.
