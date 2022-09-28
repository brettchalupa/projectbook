# Web Components

Web components are a modern way to define custom HTML elements that can encapsulate mark-up, styles, and JavaScript.

I find the idea of portable web components to be particularly compelling because they could be used and loaded on an as-needed basis and be much easier to integrate into a web page. In the past, when libraries would be primarily loaded via a JS `<script>` tag and then be available globally, you had to ensure you set them up and configured and structured the DOM appropriately. Otherwise it would break. This is pretty brittle. 

But with web components, the styles, logic, and DOM structure can be quite a bit more contained. How data gets passed into the component can vary and does require knowing the DOM strucutre, but I find it to be quite a bit more clear and simpler.

There are lots of web component libraries out there, but some primary ones to look at would be React, Vue, Lit, and Stencil. Or even just use what the DOM gives you natively without any sort of library.

These projects cover dealing with state, data, browser APIs, user interactions, and more.

## Technologies

- Vanilla JS! There's [an API for custom elements](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements) that modern browsers support.
- Stencil.js — thin wrapper of the native component API
- Vue
- Lit
- Svelte
- React

## Resources

- [MDN docs on Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components)
