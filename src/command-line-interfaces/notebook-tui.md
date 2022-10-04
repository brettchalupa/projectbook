# Notebook TUI

**The gist**: build a Terminal User Interface (TUI) for authoring, reading, and managing one's notes on a file system.

This would be a way to manage one's notes all from the terminal but with a bit of an interface to make managing them easier. Mostly a project in learning how to build a non-trivial TUI. But maybe useful. Ideally it'd just store the notes as plain-text files that could be synced/backed-up with any cloud syncing program.

## Specs

- View list of notes (which can be navigable) from file system
- Create notes
- View / edit a note

## Extra Credit

- Search
- Tag viewer

## Technology of Interest

- [Bubbletea](https://github.com/charmbracelet/bubbletea) — Go TUI framework
- [Cursive](https://github.com/gyscos/cursive) — Rust TUI lib
- [tui-rs](https://github.com/fdehau/tui-rs) — Rust TUI lib

## See Also

- [Notebook GUI](../general-graphical-apps/notebook.md)
