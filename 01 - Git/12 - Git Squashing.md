# Git Squashing

- Squashing means combining multiple commits into a single commit.
- Used to clean up your branch history before merging into `main` (or any base branch).

## Why squash commits?
- Keeps your project history clean and readable (no "fix typo", "oops", etc. scattered everywhere)
- Makes code review easier (one commit = one logical change)
- Useful for feature branches with lots of WIP (work in progress) commits

## Visualizing with `git log --graph`

**Before squashing:**
```
* C5 (feature)
* C4 (feature)
* C3 (feature)
* B2 (main)
* B1
```

**After squashing:**
```
* S1 (feature, squashed)
* B2 (main)
* B1
```
- All your feature branch commits are now a single commit (S1) on top of main.

## How to squash using interactive rebase
1. Make your multiple commits:
```bash
# make a change:
git add .
git commit -m 'Squash Commit #1'

# make another change
git add .
git commit -m 'Squash Commit #2'

# make another commit for example purposes
git add .
git commit -m 'Squash Commit #3'
```

2. Make sure your branch is up to date:
   ```bash
   git fetch origin
   git rebase origin/main
   ```
3. Start an interactive rebase for the last N commits (replace N with the number of commits you want to squash):
   ```bash
   git rebase -i HEAD~N
   ```
4. In the list that appears, leave the first commit as `pick` and change the rest to `squash` (or just `s`).
	- most probably, this will open in a vim editor. Basic navigation in this file:
	- press `esc` -> press `i` key to enter insert mode
	- make the changes to commits (have one pick, and all other squash commits)
	- to save changes, press `esc` -> type `:wq!`
![[Pasted image 20250707141826.png]]


5. Save and close the editor. Git will ask you to write a commit message for the new squashed commit.
6. Save and close again to finish. Done!

- If you get stuck or see a conflict, Git will tell you what to do next (usually fix the file, then run `git rebase --continue`).


## Squashing vs regular commits
- Regular commits: every change is a separate commit (can be messy)
- Squashed: all changes are combined into one commit (clean history)

## Best practices
- Squash before merging feature branches into main
- Don’t squash commits that are already shared with others (can cause problems for teammates)
- Use clear, descriptive commit messages for squashed commits

## When to squash and when not to
- **Squash:**
  - Before merging a feature branch
  - When you want a single logical change in history
- **Don’t squash:**
  - On shared branches (unless everyone agrees)
  - If you want to preserve detailed history for debugging purposes

---
