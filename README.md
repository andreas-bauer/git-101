# git-101

## Configuration (global and project scope)

### Global gitconfig

Configure non-default behavior once on a global scope to use it in all repositories.

Create the file `~/.gitconfig` or `~/.config/git/config`.

```shell
[user]
  email = andreas.bauer@bth.se
  name = Andreas Bauer
[core]
  autocrlf = input
  excludesfile = ~/.gitignore
```

This settings can also be set via the `git config` command:

```shell
git config --global user.name "Andreas Bauer"
git config --global user.email andreas.bauer@bth.se
```

[Example global gitconfig](https://github.com/andreas-bauer/dotfiles/blob/master/gitconfig)

For more information see the [official documentation](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration).

### Repository gitconfig

Sometimes you want to use a different email addresses in different repositories,
e.g., one for work related repositories and one for private repositories.
You can change (override) global settings on a repository level by
using the `--local` parameter when setting git configs.

```shell
git config --local user.email myname@work.com
```

You can check your local configuration by displaying the config file in the repository:

```shell
cat .git/config
```

## Gitignore

### Global gitignore file

A global `.gitignore` file allows you to ignore files and directories in all
git repositories.
This is especially useful when the OS creates files or directories that are not
related to the git project at all,
like the `.DS_Store` files in macOS or `.Trash` folder in Linux.

Create a `~/.gitignore` file and reference it in the global config (see example above).

```gitignore
# KDE directory preferences
.directory

# Linux trash folder
.Trash-*<Paste>

# macOS DS_Store files
.DS_Store
```

[Example global gitignore file](https://github.com/andreas-bauer/dotfiles/blob/master/gitignore)

### Gitignore templates

If you are not sure what the `.gitignore` file for a specific language/technology
should contain you either can use a generator or existing templates.

- [gitignore-generator](https://mrkandreev.name/snippets/gitignore-generator/)
- [collection of .gitignore templates](https://github.com/github/gitignore)

## Commit size

[TBA]

## Commit messages

[TBA]

## Working in branches

[TBA]

## Discard changes

[TBA]

## Merge branches

[TBA]

## Fix ups (rebase)

[TBA]

## Aliases

[TBA]

## License

Copyright (c) 2022 Andreas Bauer

This work is licensed under [CC BY-SA 4.0](./LICENSE).
