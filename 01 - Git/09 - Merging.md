# Git Merging

## What is Merging?
- Merging is the process in which changes from one branch are incorporated into another branch.
- Usually, this is done when, for example, features are completed in the feature branch and they are merged (integrated) into the main / production branch


## Basic Merge Commands

### Merging a Feature Branch into Main
```bash
# Switch to the target branch (main)
git checkout main

# Pull latest changes from remote
git pull origin main

# Merge the feature branch
git merge feature-branch

# Push the merged changes
git push origin main # or if you only have 1 remote connected, simply do git push
```

### Fast-Forward vs. Non-Fast-Forward Merges
- **Fast-forward**:
	- when you created a separate branch and added changes to the new branch, there had been no more changes to the main branch
	- while merging back to main, the entire branch is shifted and added in front of the main branch, acting like there were no branches and the work was directly committed to the main branch
- **Non-fast-forward**: Creates a merge commit to combine divergent histories

## Best Practices

1. **Always pull before merging**: `git pull origin main`
2. **Test before merging**: Ensure feature branch works correctly
3. **Use descriptive commit messages** for merge commits
4. **Delete feature branches** after successful merge: `git branch -d feature-branch`

## Quick Reference

| Command                       | Description                                       |
| ----------------------------- | ------------------------------------------------- |
| `git merge <branch>`          | Merge specified branch into current branch        |
| `git merge --no-ff <branch>`  | Create merge commit even if fast-forward possible |
| `git merge --abort`           | Cancel ongoing merge                              |
