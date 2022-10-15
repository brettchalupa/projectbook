# HTTP Client

**The gist:** wrap the language you're learning's HTTP interface with a more friendly API.

Many programming languages come with libraries for making HTTP requests since it's such a common need for programmers. Sometimes the interfaces that the standard libraries provides aren't that intuitive.

## Mock-Up

Let's look at what this could be like with Ruby. Ruby provides the [`net/http` library](https://ruby-doc.org/stdlib-3.0.3/libdoc/net/http/rdoc/Net/HTTP.html) for making HTTP requests.

You would use it like this to fetch the JSON from a URL and return it as a Hash in Ruby:

``` ruby
require 'net/http'
require 'json'
url = URI('https://openlibrary.org/books/OL7353617M.json')
response_body = Net::HTTP.get(url)
res = JSON.parse(response_body)
```

`res` (truncated) is a Ruby Hash that looks like:

``` ruby
{
  "publishers"=>["Puffin"],
  "number_of_pages"=>96,
  "isbn_10"=>["0140328726"],
  "covers"=>[8739161],
  "key"=>"/books/OL7353617M",
  "authors"=>[{"key"=>"/authors/OL34184A"}],
  "ocaid"=>"fantasticmrfoxpu00roal",
  "contributions"=>["Tony Ross (Illustrator)"],
  "languages"=>[{"key"=>"/languages/eng"}]
}
```

Instead of repeating those three lines of code for every single request you want to make to get the parsed body, you could write a library for it.

Let's say the library is called `Hyper`, for the "Hyper" in HTTP. It might look like:

``` ruby
require 'net/http'
require 'json'

class Hyper
  def self.get(url)
    url = URI(url)
    response_body = Net::HTTP.get(url)
    JSON.parse(response_body)
  end
end
```

All you would have to do is:

``` ruby
Hyper.get('https://openlibrary.org/books/OL7353617M.json')
```

To have the same output as before.

You'd then package that code up and share it as a library to use it in your various projects and for others to use.

This is a very simplified example, but I think it illustrates what this project could look like. A good library would validate the input, provide helpful errors, and allow specifying the needed options.

In the case of Ruby, if this was published as a Gem, people would install it in their `Gemfile` and use it throughout their code. Pretty neat!

## Extra Credit

- Add support for POST, PUT, and DELETE methods
- Support specifying authentication headers
- Raise errors when the HTTP response is not successful
- Follow redirects
- An HTTP library is quite nice. Something even neater would be a library that specifically makes making GraphQL requests easier since they're always to the same endpoint but the request body varies. Seems like a good case for a library!

## See Also

- [HTTPal](../command-line-interfaces/httpal.md) — write a CLI for making HTTP requests; could use the library written here!
- [API Wrapper](./api-wrapper.md) — write wrapper for an API to make it easier to consume the API
