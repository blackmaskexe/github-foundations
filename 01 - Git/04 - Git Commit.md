
- a git commit represents incremental changes to a codebase (a checkpoint)
- can be seen in a git tree (graph)
![[../00 - Resources/Pasted image 20250620233543.png | 400]]
## What is inside a commit:
- tracking of additions, modifications and deletions of files
- does not contain the files itself (therefore, lightweight), but only the additions and deletions
- each commit has a SHA hash id (commit hash), used to identify particular commits
- has the author email and name (that you set in the gitconfig)
- could contain commit messages (It is important to write descriptive commit messages)
- timestamp
- parent commit hashes
- snapshot of content (reference of files at the time of doing the commit)

## Commit Commands:
i. add the files if you haven't
```bash
git add path/to/file
```

ii. use the commit commands:
```bash
git commit -m 'commit message' # ⭐️ make a commit with a message

git commit -a -m 'commit message' #automatically stage all tracked, modified files before commmit. Essentially git add --all + git commit -m. NOTE: DOES NOT GIT ADD FOR NEWLY CREATED FILES, ONLY THE OLD ONES

git commit --amend # modify the most recent commit

git commit -m 'commit message' --allow-empty # creates an empty commit, mainly used for a placeholder

git commit -m 'commit message' --author="Author Name <email@example.com>" # commits with a specified author
```