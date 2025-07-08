# Git Aliases

## What are Git Aliases?

Git aliases are **shortcuts** for long Git commands. Instead of typing the full command every time, you can create a short nickname.

Think of it like creating a speed dial for your phone - instead of typing the full number, you just press one button.

## How to Create Aliases

```bash
git config --global alias.SHORTCUT "FULL COMMAND"
```

## Useful Aliases to Try

### Basic Shortcuts

```bash
# Instead of typing "git status" every time, just type "git st"
git config --global alias.st "status"

# Short for "git commit"
git config --global alias.ci "commit"

# Short for "git checkout"
git config --global alias.co "checkout"

# Short for "git branch"
git config --global alias.br "branch"
```

### Pretty Log Display

```bash
# Beautiful one-line log with graph
git config --global alias.lg "log --oneline --graph --all"

# Detailed pretty log
git config --global alias.tree "log --graph --pretty=format:'%h - %s (%cr) <%an>' --abbrev-commit"
```

### Quick Operations

```bash
# Quick add and commit
git config --global alias.ac "!git add -A && git commit -m"

# Undo last commit (keep changes)
git config --global alias.undo "reset HEAD~1"
```

## How to Use Your Aliases

After creating aliases, use them like regular Git commands:

```bash
# Instead of: git status
git st

# Instead of: git log --oneline --graph --all
git lg

# Instead of: git add -A && git commit -m "message"
git ac "my commit message"
```

## See Your Current Aliases

```bash
# List all your aliases
git config --global --get-regexp alias
```

## Remove an Alias

```bash
# Remove the "st" alias
git config --global --unset alias.st
```
