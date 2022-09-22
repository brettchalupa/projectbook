# Spell Checker

CLI for checking a document or given folder of documents of plain text for typos.

An exercise in leveraging an existing dictionary and then reading files, checking them, and letting the user know about the issue and where it is.

If a typo is found, the program should exit with a non-zero status so it could be used as part of a CI pipeline or something.

It'd also be great if it could text in text via stdin via piping and such too!

## Spec / Examples

```
sc blog/2020-10-23-my-favorite-albums.md
```

If it has no detected typos, then it would exit with a 0 status and not output anything. Silence is golden/no news is good news.

Let's say it has a typo, then it'd be non-zero and output to stderr:

```
Typos found:
- Line 4, Col 45: "teh" appears to be a typo
- Line 8, Col 4: "Borwsre" appears to be a typo
```

## Stretch Goals

- Add the ability for the user to specify custom words and phrases that shouldn't trigger an error
- Smart detection of metadata and technical things like links and HTML and CSS and code fences in Markdown
- Make it interactive with corrections
- Make a GUI
