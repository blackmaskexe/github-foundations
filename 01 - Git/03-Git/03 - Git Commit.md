
- a git commit represents incremental changes to a codebase
- can be seen as a git tree (graph)

## What is inside a commit:
- tracking of additions, modifications and deletions of files
- does not contain the files itself (therefore, lightweight), but only the additions and deletions
- each commit has a sha hash id (commit hash), used to identify particular commits
- has the author email and name
- could contain commit messages (It is important to write descriptive commit messages)
- timestamp
- parent commit hashes
- snapshot of content (reference of files at the time of doing the commit)

## Commit Commands:
i. add the files if you haven't
```bash
git add file

```

ii. use the commit commands:
```bash
git commit -m 'commit message' # make a commit with a message

git commit -m -a 'commit message' #automatically stage all tracked, modified files before commmit. Essentially git add --all + git commit -m

git commit --amend # modify the most recent commit

git commit -m 'commit message' --allow-empty # creates an empty commit, mainly used for a placeholder

git commit -m 'commit message' --author="Author Name <email@example.com>" # commits with a specified author
```