# Learning Git

## Tips

* `git init <name>` - creates a folder with the given name and starts git in it.
* `git checkout -- <file>` to go back to last commit status of a given file.
* `git config --global alias.<command_name> "<command>"` to create a new git command.
    * e.g.: `git config --global alias.history "log --oneline --graph --decorate --all"` creates `git history` command.
    * It doesn't prevent you from adding arguments after it. E.g. `git history -- <file>`
* `git config --global --list` to list global configuration.
* `git log -- <file>` shows history only for the given file.
* `git mv <file>` to change a file name, avoiding side-effects of doing it manually. Same for `git rm`.


## Installation notes
How to set up VSCode as diff and merge tool:

```
git config --global difftool.code.path "$(which code)"

git config --global difftool.prompt false

git config --global merge.tool code

git config --global mergetool.code.path "$(which code)"

git config --global mergetool.prompt false
```