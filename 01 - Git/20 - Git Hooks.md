# Git Hooks

## What are Git Hooks?

Git hooks are **scripts that run automatically** when certain Git events happen.

Think of them like alarms - they trigger when something specific occurs (like making a commit).

## Common Hook Types

- **pre-commit**: Runs before you commit (check code quality)
- **post-commit**: Runs after you commit (send notifications)
- **pre-push**: Runs before you push (run tests)

## Where to Find Hooks

```bash
# Hooks live in this folder
ls .git/hooks/
```

## Simple Example

Create a hook that prints "Hello!" after every commit:

```bash
# Create the hook file
echo 'echo "Hello! You just committed!"' > .git/hooks/post-commit

# Make it executable
chmod +x .git/hooks/post-commit
```

Now every time you commit, you'll see "Hello! You just committed!"
