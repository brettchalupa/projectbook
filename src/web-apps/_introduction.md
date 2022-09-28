# Web Apps

Web application projects are great for those learning web frameworks. Most of them are full stack projects, which means they require a database, a back-end to manage the data, and a front-end to render the user interface. They typically require the ability to create, read, update, and destroy (CRUD) a variety of data.

There are so many different technologies to use to build web applications, as well as varying methodologies. From using server-rendered forms to building a single page app (SPA) with an API, how you go about it will depend on what you're building and what you're learning.

The complexity of web applications can be deep, but rudimentary versions of the projects that follow can be built pretty quickly. Polishing, securing, and fleshing out web apps takes time, but something basic can be built in a matter of hours or days.

Whether you want to be a back-end, front-end, or full stack web developer, the ideas will be great for learning as they cover a lot of the common concepts like authentication, authorization, managing data, and building interfaces.

## Technologies of Interest

Modern languages all have at least one web application framework that handles a lot of the core needs and setup. These frameworks will let you get building web applications pretty quickly.

- [Django](https://www.djangoproject.com) —  Python web app framework
- [Express](https://expressjs.com) — Node.js minimal web app framework
- [Laravel](https://laravel.com) — PHP web app framework
- [Phoenix](https://www.phoenixframework.org) — Elixir web app framework
- [Redwood](https://redwoodjs.com) — newer, opinionated TypeScript web app framework
- [Revel](https://revel.github.io) — Go web app framework
- [Rocket](https://rocket.rs) — Rust web app framework
- [Ruby on Rails](https://rubyonrails.org) — Ruby web app framework; I've used this for over a decade, and it does the trick!

Web application frameworks alone might not be enough though, as you may need to pull in libraries from the JS ecosystem, especially for writing the front-end code (styles, mark-up, and JS). If you're wanting to use web components or a front-end framework, check out these libraries:

- [Ember](https://emberjs.com)
- [Lit](https://lit.dev)
- [React](https://reactjs.org)
  - [Next.js](https://nextjs.org)
- [Svelte](https://svelte.dev)
- [Stencil](https://stenciljs.com)

When it comes to building an API, [GraphQL](https://graphql.org) would be my technology of choice because of its flexibility and strong types. But there are some other options out there:

- Roll your own JSON API! This is fine for experimenting and smaller projects.
- [JSON:API spec](https://jsonapi.org)
- [OpenAPI spec](https://spec.openapis.org/oas/v3.1.0)
- [JSON Schema](https://json-schema.org)

## Hosting

Because most web applications require some sort of server and a database, you'll need to configure the app to run _somewhere_. When building a project, you'll typically run what you're building on your own computer, which can serve requests to your web browser. This is great because it doesn't cost anything. The downside is that your project isn't accessible to others then. That's probably all right while you're learning. But if you ever want to make something that others can use, you'll want to deploy your application to a host. How you go about that is beyond the scope of this book, but there are lots of resources out there.
