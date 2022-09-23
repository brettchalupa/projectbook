# HTTPal

**The gist:** write a CLI that makes HTTP network requests and responds with the output.

`curl` and `wget` are common programs used to transfer data to or from a server, like downloading a file over HTTP. This project is writing something similar to them. Start with just GET requests and then go from there.

I always call this idea `httpal` because it's kinda fun. It's your buddy for making requests!

## Spec

This could look something like:

```
httpal https://openlibrary.org/books/OL7353617M.json
```

That would make a GET request to that API endpoint for _Fantastic Mr. Fox_ and return the JSON, which could then be output to a file like:

```
httpal https://openlibrary.org/books/OL7353617M.json > fmf.json
```

## Concepts

- Making network requests, often times available within the standard library of a language
- Outputting the response body
- Basic CLI interactions

## Extra Credit

- Follow redirects
- Support different forms of authentication and request headers
- Support other HTTP methods like PUT, POST, and DELETE
- Support specifying a request body file, like a JSON file, to include in the request body
- Support other protocols! Maybe a better name would be `reqbud`. 😬
- What if program specifically catered to those interacting with GraphQL APIs? That means it would always POST to the same endpoint but allow for configurable requests and variables. `gqlpal`???
- What if there was a way to load requests for a project from a variety of spec files and easily make those requests? Like a CLI version of [Postman](https://www.postman.com) or [Paw](https://paw.cloud).

## See Also

- [HTTP Client](../libraries/http-client.md)
