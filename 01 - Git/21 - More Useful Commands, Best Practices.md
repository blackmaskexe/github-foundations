
## File and Directory Operations
#### 1. Remove File from Git but Keep Locally
```bash
git rm --cached filename.txt
```
#### 2. Remove Directory from Git but Keep Locally
```bash
git rm -r --cached directory/
```

## Branch Management
#### 1. Delete Remote Branch
```bash
git push origin --delete branch-name
```
#### 2. See All Branches (Local and Remote)
```bash
git branch -a
```
#### 3. Rename Current Branch
```bash
git branch -m new-branch-name
```

## Commit Fixes
#### 1. Change Last Commit Message
```bash
git commit --amend -m "New commit message"
```
#### 2. Add Files to Last Commit
```bash
git add forgotten-file.txt
git commit --amend --no-edit
```
#### 3. See What Changed in a Commit
```bash
git show commit-hash
git show HEAD~1  # Show previous commit
```
#### 4. See Who Changed What (Who to Blame)
```bash
git blame filename.txt
```
#### 5. Pretty Log with Graph
```bash
git log --oneline --graph --all --decorate
```

## Remote Operations
#### 1. Sync Fork with Original
```bash
git fetch upstream
git checkout main
git merge upstream/main
```
#### 2. Change Remote URL
```bash
git remote set-url origin new-url
```

## Search Operations
#### 1. Find Text in All Files
```bash
git grep "search-term"
```
#### 2. Find in Specific Files
```bash
git grep "search-term" -- "*.js"
```
#### 3. Search in Git History
```bash
git log --grep="bug fix"
```
#### 4. Find When Text Was Added/Removed
```bash
git log -S "function-name" --oneline
```

## Configuration
#### 1. Set Default Editor
```bash
git config --global core.editor "code --wait"  # VS Code
git config --global core.editor "vim"          # Vim
```

## Emergency Fixes
#### 1. Committed to Wrong Branch
```bash
git log --oneline -1     # Note the commit hash
git reset HEAD~1         # Undo the commit
git checkout correct-branch
git cherry-pick commit-hash
```
#### 2. Accidentally Committed Sensitive Data
```bash
# If not pushed yet:
git reset HEAD~1
git add .
git commit -m "Fixed commit"

# If already pushed - contact your team immediately!
```

## Emergency/Force Commands ⚠️
#### 1. Force Push (Overwrite Remote with Local)
```bash
# DANGER: Overwrites remote with your local repo
git push --force-with-lease origin main
# Or the more dangerous version:
git push --force origin main
```
#### 2. Force Pull (Overwrite Local with Remote)
```bash
# DANGER: Overwrites your local changes with remote
git fetch origin
git reset --hard origin/main
```
#### 2. Nuclear Option: Start Fresh from Remote
```bash
# DANGER: Deletes everything, starts fresh from remote
git fetch origin
git reset --hard origin/main
git clean -fd  # Removes untracked files and directories
```

## Best Practices 🏆
#### 1. Commit Messages
```bash
# Good commit messages:
git commit -m "Add user authentication feature"
git commit -m "Fix: Handle null pointer in login"
git commit -m "Refactor: Extract validation logic"

# Bad commit messages:
# "fix stuff", "wip", "asdf", "updates"
```
#### 2. Branch Naming
```bash
# Good branch names:
feature/user-authentication
bugfix/login-error
hotfix/security-patch
feature/payment-integration

# Bad branch names:
# "stuff", "test", "john-branch", "new"
```
#### 3. Daily Workflow
```bash
# Start of day:
git checkout main
git pull origin main
git checkout -b feature/new-feature

# End of day:
git add .
git commit -m "Progress on new feature"
git push origin feature/new-feature
```
#### 4. Before Merging
```bash
# Always do this before creating PR:
git checkout main
git pull origin main
git checkout your-branch
git rebase main  # Fix any conflicts
git push --force-with-lease origin your-branch
```
#### 5. Repository Hygiene
```bash
# Clean up merged branches:
git branch --merged | grep -v main | xargs git branch -d

# Clean up remote tracking branches:
git remote prune origin
```

## Quick Reference Commands

| Situation | Command |
|-----------|---------|
| "I want to undo everything" | `git reset --hard HEAD` |
| "Save my work temporarily" | `git stash` |
| "Get my work back" | `git stash pop` |
| "I committed to wrong branch" | `git reset HEAD~1` |
| "Force push safely" | `git push --force-with-lease` |
| "Get latest from remote" | `git pull --rebase` |
| "See what I changed" | `git diff` |
| "See commit history" | `git log --oneline` |
| "Clean untracked files" | `git clean -fd` |
| "Ignore tracked file" | `git rm --cached file` |
