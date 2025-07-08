## The Problem: "I Made a Mistake!"

Sometimes you need to undo changes in Git. There are two main ways:

- **Reset**: Go back in time (like it never happened)
- **Revert**: Create a new commit that undoes previous changes

## Git Reset

- Reset moves your branch pointer backwards, like rewinding a movie.

### Basic Reset Commands

```bash
# Undo last commit, keep changes in your files
git reset --soft HEAD~1

# Undo last commit, unstage changes (most common)
git reset HEAD~1

# Undo last commit, delete all changes (CAREFUL!)
git reset --hard HEAD~1
```

### What HEAD~1 Means

- `HEAD` = your current commit
- `HEAD~1` = one commit before current
- `HEAD~2` = two commits before current

### Reset Examples

**Before reset:**

```
* c3 (HEAD -> main) Oops, bad commit
* c2                Good commit
* c1                Initial commit
```

**After `git reset HEAD~1`:**

```
* c2 (HEAD -> main) Good commit
* c1                Initial commit
```

The bad commit (c3) is gone!

## Git Revert - Creating an "Undo" Commit

- Revert creates a new commit that undoes previous changes. **Safer** for shared repositories.

### Basic Revert Command

```bash
# Undo the last commit with a new commit
git revert HEAD

# Undo a specific commit
git revert abc123f
```

### Revert Example

**Before revert:**

```
* c3 (HEAD -> main) Bad changes
* c2                Good commit
* c1                Initial commit
```

**After `git revert HEAD`:**

```
* c4 (HEAD -> main) Revert "Bad changes"
* c3                Bad changes
* c2                Good commit
* c1                Initial commit
```

The bad changes are undone, but the history is preserved!

## Safety Tips

#### 1. Before Using Reset --hard
```bash
# See what you're about to lose
git log --oneline -5

# Create a backup branch first
git branch backup-branch
git reset --hard HEAD~2
```
#### 2. Check Your Status
```bash
# Always check where you are
git status
git log --oneline -5
```
