# Learning Git


## Installation notes
How to set up VSCode as diff and merge tool:

```
git config --global difftool.code.path "$(which code)"

git config --global difftool.prompt false

git config --global merge.tool code

git config --global mergetool.code.path "$(which code)"

git config --global mergetool.prompt false
```