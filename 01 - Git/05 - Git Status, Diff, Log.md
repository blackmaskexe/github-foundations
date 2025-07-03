
NOTE:
- All of the following commands are used to see the state of the git repository in many meaningful ways
- All the commands below do not do any changes, and only display information about git repo: There are no accidental downsides / side effects of using these commands.


## Git Status:
- this should be your go-to command to check the overall status of your github repository
- This command tells you what's going on in your working directory as well as the staging area
- compares the latest commit with the previous one
- tells you what branch you are on

```bash
git status
```

## Git Diff:
- shows all differences between files in the staging area and the working directory
- basically, shows what changes you have not yet added to the staging area

- to show ALL of the differences between staging and working directory:
	- note that to exit the git diff changelogs, you can simply press q on your keyboard
```bash
git diff
```

- to show differences between staging and working directory ONLY for a particular file:
```bash
git diff relative/link/to/file
```

- Main use case for using git diff: verify changes before committing them

## Git Log:
- shows all past commits, and the following information associated with each of them:
	1. author name & email
	2. date
	3. commit message
	4. branch

```bash
git log
```
