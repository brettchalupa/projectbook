# Prose Renderer

I tend to think of this as a library or component called `Prose.js` or `Reader.js` that is concerned with taking a nested collection of `<p>` elements in partidular and rendering them in a way that gives the user fine grain control over how it's rendered. Their preferences would be stored in `localstorage` so upon refresh their settings would load and be used across web pages (like chapters in a book).
  
Essentially Kindle's reading options
  
Configuration options:

- Text size
- Text weight
- Font
- Text alignment -- justified or left aligned or right aligned
- Line spacing
- Margins

[wireframe]
[icons/elements]

## Spec

Usage:

1. include the script to load the source
2. just use the component! wrap the output for the prose in the component:

``` html
<Prose>
  <p>It was a dark and stormy night...</p>
  <p>More stuff! More stuff!</p>
</Prose>
```

## Tech

Any of the major web component libraries are appealing for this, in particular ones that can generate a portable component that can be easily loaded and dropped in like Stencil. Svelte and Lit appeal to me too.

## Concepts

- Working with `localstorage` -- writing and reading
- Building out a non-intruisive UI
- Overriding/applying styles to nested content