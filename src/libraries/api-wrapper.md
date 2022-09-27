# API Wrapper

**The gist**: write a wrapper for an HTTP API to make it easier to work the endpoints and returned data.

When consuming an API, especially a foundational one to your application, it can be much easier to interact with a library written in the programming language you're using rather than making HTTP requests and parsing the response every single time. By building an API wrapper, you'll be able to create a more idiomatic API for the language you're using in, make configuring the API easier, and have more control over consistently manipulating the response.

## Spec

- [Pick an API](https://github.com/public-apis/public-apis) or [write one](../web-apis/read-only-api.md)
- Write code to make it easy to interact with the available endpoints
- Use the code you wrote wherever you want to fetch and display it

## Concepts

- API design (for those using your library)
- Consuming an HTTP API
- Packaging up and sharing code

## Mock-Up

Let's say I want to display a random dog photo in my application whenever a user views a given page. I could use [the Dog API](https://dog.ceo/dog-api/) for that. If I'm working with Ruby, I could make the request using:

``` ruby
require 'net/http'
require 'json'
url = URI('https://dog.ceo/api/breeds/image/random')
response_body = Net::HTTP.get(url)
res = JSON.parse(response_body)
res["message"]
```

That's kind of a bummer to use every time I want a random dog image! Sure, [an HTTP client](./http-client.md), would reduce that burden, but maybe I want to display different dog photos throughout my app and want to reuse that code. I'd introduce something like:

``` ruby
require 'net/http'
require 'json'

class DogApi
  RANDOM_URL = 'https://dog.ceo/api/breeds/image/random'.freeze

  def self.random_image_url
    response_body = Net::HTTP.get(URI(RANDOM_URL))
    JSON.parse(response_body)["message"]
  end
end
```

Then in my application, all I would have to do is call `DogApi.random_image_url` to have a URL returned for a dog image. Much simpler.

The above code is a bit... naive. It doesn't handle errors, which could certainly happen. What if the API is down or we get rate limited? We'd want something useful to happen for those using the wrapper. That's part of the joy of using an API wrapper. The best API wrappers handle errors and respond in a away appropriate for the language. For Ruby code, it could raise an exception.

Even within just one class and a class method, there are some design decisions I made. I called the wrapper `DogApi` instead of just `Dog` because it's more specific, and `Dog` is too generic of a name in my opinion. I wouldn't want to inadvertantly interfere with it. I also named the method `.random_image_url` because it makes it clear what's returned—a URL to the image. If it was just called `.random`, it wouldn't be clear what's returned—is it a hash, a `Dog` object, or an image URL?

There is a fine line to walk when developing an API wrapper. You want to remain true to the API you're wrapping so that the patterns and names aren't wildely inconsistent, but you also want to be clear and use the idioms of the language you're using.

## Examples

- [sferik/twitter](https://github.com/sferik/twitter) — Twitter API wrapper written in Ruby
- TODO: add more!

## Extra Credit

- Document the available interfaces for your library
- Publish your wrapper if one doesn't exist already and if the API is public
- Support all of the API endpoints
- Support the params that can be passed into the requests

## See Also

- [Read-Only API](../web-apis/read-only-api.md)
- [Client App](../general-graphical-apps/client-app.md)
- [HTTP Wrapper](./http-wrapper.md)
