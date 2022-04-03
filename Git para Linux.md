# Git para Linux


### Usar `git` en un nuevo ordenador
Utiliza el comando `gh auth login`.
La CLI te ayudará a registrar tu cuenta de usuario Git en tu ordenador.

## Getting started
* Create repo from local: `mkdir <folder> && cd <folder> && git init`
* Download repo from remote: `git clone <url_repo> [folder]`
* Download changes from remote: `git pull`

### Upoloading changes
* Adding changes: `git add <file_or_folder>`
* * You can use `.` to add everything, but this would commit different files together!
* Commit changes: `git commit` (will open a prompt to add a message) or `git commit -m <message>`
* Add stuff to the last commit: `git commit --amend [-m <mesage>]`

### Managing branches
* Change among existing branches: `git checkout <branch_name>`
* List existing branches: `git branch`
* Make new branch (and get in): `git checkout -b <branch_name>`

## Cleaning up
### Combine commits (squashing) and edit them (rewording)
Do `git rebase -i HEAD~<n>` to see a list of the last `n` commits.

## Troubleshooting
### I want to undo a...
* Uncommited `add`: `git reset --hard`
* Unpushed `commit`: `git pull`
* Push: 

### <my_branch> is behind <other_branch>...?
Try using `git rebase <other_branch>`.
You will need to `git push -f` after this, but that is unavoidable, since you have altered the commit history.
