# Custom Markup Language

There are a lot of these, like TOML, YAML, Markdown, etc. But it'd be a worthwhile exercise to write your own so that you understand how they work. Whether the language is for authoring content intended to be HTML or a key-value configuration language, that's up to you. Just pick what sounds found and what you're interested in.

You'd want to:

1. define the spec
2. write out some examples
3. build code that can read it and load it and do whatever with it

## Concepts

- Processing text by converting from one language to another
- File IO

## An Example

Let's pretend that Markdown doesn't exist. Poof! It's gone. Who's Mark Down? Never met 'em.

Imagine I wanted a plain text way to describe some richer text that converts to HTML. Okay, let's define the spec.

Imagine there's a file in a fictional language called Brettdown (ugh, terrible name). The file is named `hello.bd`:

```
Hi, my name is Brett. Brettdown is my new minimal language for writing. !Bold! and ~italic~ are both quite nice.

Content can be lists:

* Twin Peaks
* X-Files

You can even add order, like my favorite fruits:

1) Apples
2) Dates
3) Blueberries

Links look like this: ^My Website{https://example.com}
```

Write a command-line tool that converts that file into HTML that looks something like this:

``` html
<p>Hi, my name is Brett. Brettdown is my new minimal language for writing. <strong>Bold</strong> and <em>italic</em> are both quite nice.

<p>Content can be lists:</p>

<ul>
  <li>Twin Peaks</li>
  <li>X-Files</li>
</ul>

<p>You can even add order, like my favorite fruits:</p>

<ol>
  <li>Apples</li>
  <li>Dates</li>
  <li>Blueberries</li>
</ol>

<p>Links look like this: <a href="https://example.com">My Website</a></p>
```

## See Also

- [Markdown Processor](./markdown-processor.md)
