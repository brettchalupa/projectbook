# Conventional Committer

**The gist**: build a CLI for authoring Git commits that follow [the Conventional Commits spec](https://www.conventionalcommits.org).

If you use the Conventional Commits spec for Git commits, it'd be nice to have a command you could run for easily creating commits that follows that guide. It could be a TUI or just a CLI.

## Mock-Ups

Run the command with:

``` console
$ gcommit
```

That would open an interactive prompt for entering in the data.

## Specs

- Command for creating a commit, command could even be called `gcommit` or whatever
- Have flags for or ask for:
  - type
  - scope (optional)
  - description — concise
  - body (optional)
  - footer (optional)
- If the required type and description aren't present, error
- If everything's there, create the Git commit

## Extra Credit

- Configurable, per-repo types that are allowed
- Configurable input for custom body & footer data, like maybe each commit needs an issue ID or URL

## Thoughts

This is a great project for an easily distributable binary that can run on any platform regardless of the ecosystem and language a person or team uses. Just like Git can be installed and used for a project with any programming language, so should this tool!

## References

- [commitlint](https://github.com/conventional-changelog/commitlint) — similar tool distributed through npm
