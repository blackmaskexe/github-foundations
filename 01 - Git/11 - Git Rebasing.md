# Git Rebase

- Rebasing is a way to move or combine a sequence of commits to a new base commit.
- It’s often used to make your branch history cleaner before merging into `main`.

## What does rebase do?
- Takes all your branch’s commits and “replays” them on top of another branch (usually `main`).
- This makes it look like you started your work from the latest commit on `main`.

## Visualizing with `git log --graph`

**Before rebase:**
```
* C3 (feature)
* C2 (feature)
| * B3 (main)
| * B2
|/
* B1
```

**After rebase (feature rebased onto main):**
```
* C3' (feature, rebased)
* C2'
* B3 (main)
* B2
* B1
```
- Now your feature branch is “on top” of the latest `main` commits.

## Rebase vs Merge
- **Merge:** Keeps all branch history, creates a merge commit.
- **Rebase:** Makes history linear, no merge commit.

## How to rebase
```bash
git checkout feature
git rebase main
```

## Pro tips
- Use rebase for local, unpublished branches to keep history clean.
- Don’t rebase shared branches (can mess up your teammates).
- If you hit conflicts, resolve them, then continue:
  ```bash
  git rebase --continue
  ```
