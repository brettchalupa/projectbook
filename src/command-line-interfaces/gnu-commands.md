# GNU Utilities

[TODO: verify GNU Utilities is the proper name for these]

When working with the command line, it's likely you have used of the core GNU utilities like `grep`, `cat`, `less`, `tail`, `sort`, and more.


One way to learn a language is to rewrite those existing tools' functionality. Who knows, you might end up making a faster or better version.

One of the main concepts is being able to pipe data and chain together the commands. `cat foo.txt | grep bar`, that sort of thing.

Here are some simpler utilities that would be good candidates for building:

- `cat` -- output the contents of a file, line by line, to stdout
- `ls` -- list the files of the current or passed in directory
- `less` -- read-only file viewer, particulary useful for longer files
- `sort` -- order lines alphanumerically
- `search` -- idk what that does
- `tail` -- print last n lines of a file, can follow output, useful for logs
