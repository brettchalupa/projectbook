# Unix Utilities

When working with the command line, it's likely you have used of the core Unix programs like `grep`, `cat`, `less`, `tail`, or `sort`.

A great learning exercise is to rewrite those existing tools. Who knows, you might end up making a faster or better version.

One of the main concepts in Unix is being able to pipe data and chain together the commands. `cat foo.txt | grep bar`, that sort of thing. As part of rewriting these commands, you'll need to learn about `stdin`, `stdout`, and more.

Here are some simpler utilities that would be good candidates for building:

- `cat` — output the contents of a file, line by line, to stdout
- `ls` — list the files of the current or passed in directory
- `grep` — search through the contents of target files for a match
- `less` — read-only file viewer, particulary useful for longer files
- `sort` — order lines alphanumerically
- `tail` — print last n lines of a file, can follow output with `-f`, useful for logs
- `wc` — displays the number of lines, words, and bytes in a file

## Resources

- [Learning Rust by Writing a Command Line App in 15 Minutes](https://rust-cli.github.io/book/tutorial/index.html#learning-rust-by-writing-a-command-line-app-in-15-minutes)
- [Grep from First Principles, in Golang](https://willdemaine.ghost.io/grep-from-first-principles-in-golang/)

## Examples

- [brettchalupa/werds](https://github.com/brettchalupa/werds) — a (poor) clone of `wc` I made to help learn Rust
