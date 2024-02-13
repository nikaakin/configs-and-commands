# fzf-find-directories

find directories using linux `find` command and search with `fzf` for interactive selection.

## Prerequisite:

- [fzf](https://github.com/junegunn/fzf) - It's an interactive Unix filter for command-line that can be used with any list; files, command history, processes, hostnames, bookmarks, git commits, etc.
- [find](https://man7.org/linux/man-pages/man1/find.1.html) - search for files in a directory hierarchy.

## Usage:

- This script will give you the interactive interface on the directories you chose and after searching it will give you back the path to it which you can then use to cd to it.

```bash
cd $(fzf-find)
```

## Customize:

```bash
find ~ ~/Desktop ~/Desktop/javascript ~/Desktop/javascript/react ~/Desktop/javascript/node -mindepth 1 -maxdepth 1 -type d | fzf
```

- You can customize the directories you want to search. `~`, `~/Desktop/javascript`, ... change or add the directories you want to search.
- update the `mindepth` and `maxdepth` as per your need.

## Examples:

- `fzf-find` - will give you the interactive interface to search for directories and gives you back the path to the selected directory.
- `cd $(fzf-find)` - will change the directory to the selected directory.
