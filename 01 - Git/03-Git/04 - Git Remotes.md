
- a git remote represents the reference to a remote location where a copy of the repository is hosted
- you can have multiple remote entries for your git repo
	- "origin" is the most common remote name for a remote repo, represents the repo from which everyone is working
	- this is most likely the name of your remote repository if you cloned it or something like that
- remote references are stored inside the .git/config file

## Most Important Git Remote Commands:

```bash
git remote -v # lists all remote repos along with their links

git remote add remote-name <remote url> #add a remote repository

git remote remove remote-name # remove a remote repo

git remote rename old-remote-name new-remote-name # rename

git push remote-name branch-name # push a brand and it's comits to a specific remote

git pull remote-name branch-name # pulls updates from a remote branch

git fetch remote-name # fetch updates without pulling changes
```

## Difference between Git Pull and Git Fetch

| `git pull`                                                                                                                                                 | `git fetch`                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| downloads new data from remote repo, integrates / merges with your existing files<br><br>( it is git fetch + git merge / rebase combined into one command) | downloads new data from remote repo into your git repo without integrating / merging changes |
| updates local copy of branch AND current local branch                                                                                                      | updates the local copy of your remote branch (eg origin/main instead of main)                |
| use case: when you are ready to incorporate the changes made in the remote repo                                                                            | use case: to see what the changes have been without applying                                 |
| usually only use when you are confident about the changes that you want to incorporate                                                                     | safest option to get the changes from a remote repo                                          |
- tip: when you want to sync projects between two computers (eg, work and personal), you can store your project on a remote repo, push the changes on your work computer, and pull it on your personal computer to have continuity of work


## Git Remote: Upstream vs Downstream:

![[Pasted image 20250625153149.png]]













## Scenarios to link Local and Remote:
#### 1. you want to commit changes to a blank repository:
```bash
git remote add origin <.git https url of your repo>
git branch -M main
git push -u origin main
```

#### 2. You have a project that you cloned from a repo, and you want to sync changes
- no need to add remote, all information is already in your .git config file for the remote repository, simply use commands like git push, pull, etc