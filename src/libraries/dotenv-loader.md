# .env Loader

**The gist**: build a library that loads a `.env` file from disk and sets environment variables from the specified files.

When working on software, especially web servers, there's a need to configure global settings. Whether it's an API URL or a secure token, you won't want those values committed in the source. So people configure their applications via environment variables.

When working on your own computer, it's a pain to manage environment variables for all of the various applications you may be working on. So a common pattern is to specify a `.env` file that's ignored by Git and have that be loaded into the environment variables for your application.

The goal of this project is to write a library that loads and parses a `.env` and loads those values into the environment that your application can then access. If the file is missing, don't load it.

## Mock-Ups

Here's what a simple `.env` file would be like. The syntax is that each line is `KEY=value` where the key is SCREAMING_SNAKE_CASE, and = sign to separate, and the value is any chars following that.

```
FAV_SNACK=donuts
USERNAME=agentcooper
```

When the library runs, it should parse that file and insert those keys and values into the environment.

## Specs

- Write a function or entry-point into the lib for loading the `.env` file in the project root
- Ensure the environment keys and values are properly set and accessible within the code using the lib
- Support custom path to the `.env` file
- Don't load the `.env` if it's not present
- Error if any line is improperly formatted
    - But be okay with empty lines

## Concepts

- Parsing files
- Validating file is correct
- Working with the environment

## Extra Credit

- Support per-environment configs (`.env.test`, `.env.dev`, etc.)
- Explore setting the environment variables just for the program that uses the library or globally for the entire running OS. What are the pros and cons of this?
- Allow for comments with lines that start with `#` or `//`
- Are there other formats you'd prefer over this simple approach like JSON or TOML or YAML? Support it!
- While sensitive data is often configured via environment variables, sometimes you have config data that isn't sensitive. What if you extended this library or made a separate library that loads config settings via a JSON, YAML, or TOML and made them easily accessible within the codebase? That'd be useful!
