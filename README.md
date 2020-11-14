# Learning Git

## Tips

* `git init <name>` - creates a folder with the given name and starts git in it.
* `git checkout -- <file>` to go back to last commit status of a given file.
* `git config --global alias.<command_name> "<command>"` to create a new git command (alias).
    * e.g.: `git config --global alias.history "log --oneline --graph --decorate --all"` creates `git history` command.
    * It doesn't prevent you from adding arguments after it. E.g. `git history -- <file>`
* `git config --global --list` to list global configuration.
* `git log -- <file>` shows history only for the given file.
* `git mv <file>` to change a file name, avoiding side-effects of doing it manually. Same for `git rm`.
* If you have changes in your working directory and perform a `git checkout -b <new_branch>`, git will carry these changes to the newly created branch.
* `git tag -a <tag_name> -m <tag_message>` - creates annotated tag.
    * `git show <tag_name> to see info about the tag.

### Stashing

* `git stash` to stash (oh, really?).
* `git stash list` to display all stashes.
* `git stash apply` to apply the stashed changes on top of the stash.
* `git stash drop` to drop the stash on to of the stack.
* `git stash pop` combines `apply` and `drop`.
* `git stash clear` to clear the stash stack.

### Resetting

* `git reset <reference>` to *go back in time*.
    * `--soft` moves HEAD to the reference and places all changes that happened after it to the staging area.
    * `--mixed` moves HEAD to the reference, but doesn't add changes after the reference to the staging area.
    * `--hard`  forces HEAD to the specified reference, cleaning the working directory and staging area.
* `git reflog` for a history of all actions taken in the repository (different from `git log`).

## Installation notes
How to set up VSCode as diff and merge tool:

```
git config --global difftool.code.path "$(which code)"

git config --global difftool.prompt false

git config --global merge.tool code

git config --global mergetool.code.path "$(which code)"

git config --global mergetool.prompt false
```