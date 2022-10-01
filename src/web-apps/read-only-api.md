# Read-Only API

**The gist**: build out a public, read-only API that serves a variety of requests.

When first learning how to build an HTTP API, it can be helpful to just focus on the structure of the requests and responding with data. This project is focused on fetching data from a database and responding to HTTP requests with that data, in whatever format you want. It could be a GraphQL API or a JSON API you design yourself.

Then, once you have this read-only API, you can build clients that render the data returned from the API. That's a great way to learn how to build GUIs driven by data from an API.

## Spec

- Set up your database and sceham for your application to read from
- Have some way to load the data that your API serves; maybe you ingest the data from a spreadsheet
- Define read-only API endpoints to fetch and return the data

## Concepts

- Data schema
- API design
- Building an API

## Example

I'd like to build out a GraphQL API that returns the albums with songs by _Guided By Voices_. They have such an extensive catalog, that'd it'd be fun to build out a GUI to browse them.

```graphql
query albumsWithSongs {
  albums {
    title
    year
    coverUrl

    songs {
      trackNo
      title
    }
  }
}
```

Which would return something like:

```json
{
  "data": {
    "albumsWithSongs": {
      "albums": [
        {
          "title": "Bee Thousand",
          "year": 1994,
          "coverUrl": "https://example.com/bee-thousand.jpg",
          "songs": [
            {
              "trackNo": 1,
              "title": "Hardcore UFO's"
            },
            {
              "trackNo": 2,
              "title": "Buzzards and Dreadful Crows"
            }
          ]
        },
        {
          "title": "Alien Lanes",
          "year": 1995,
          "coverUrl": "https://example.com/alien-lanes.jpg",
          "songs": [
            {
              "trackNo": 1,
              "title": "A Salty Salute"
            },
            {
              "trackNo": 2,
              "title": "Evil Speakers"
            }
          ]
        }
      ]
    }
  }
}
```

I could imagine there also being support for:

- an argument that returns the albums released in a given year
- searching by album name and song name and returning results
- sorting results alphabetically or by release year

I've been interested in Rust and TypeScript lately, so I'd probably use one of those for building out this API.

## Resources

- [GraphQL](https://graphql.org)
- [Open API Spec](https://spec.openapis.org/oas/v3.1.0)
- [JSON Schema Spec](https://json-schema.org/specification.html)
- [JSON API Spec](https://jsonapi.org)
- [public-apis List on GitHub](https://github.com/public-apis/public-apis) — helpful reference for similar examples

## Extra Credit

- Support pagination for large data sets
- Document the API so that it's clear how to others how to use it
- Add support for params like search query or filtering, whatever would be useful for the data you're loading
- Host it somewhere for others to use (especially if it's useful or you publish libraries publicly for others to use)

## See Also

- [Client App](../general-graphical-apps/client-app.md) — build a GUI for rendering the data returned by your API
- [API Wrapper](../libraries/api-wrapper.md) — write a wrapper for consuming the API you just built in a given language to make it easy for others to integrate with
