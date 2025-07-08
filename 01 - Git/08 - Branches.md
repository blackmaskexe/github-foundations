- When you create a branch in Git, you are copying all the code files from the main branch to the newly created branch
  - the main branch can be thought of as the trunk of a tree, where all code was worked on at the start of the repo creation
- You can have as many branches in your codebase as you want

- ⭐Analogy: Branching in git can be thought of as parallel universes when making choices. Suppose you choose to study this git documentation, then the ideal path would be you completing this documentation. However, if you deviate from this behavior and decide to quit reading this documentation at this exact moment, you are creating a parallel universe in which you did not read the documentation. You can do different things in this parallel universe like meeting with a friend, have fun, etc, but it all started with you reading the documentation. The point where you quit reading the documentation is the point when two different branches were created (branching point): the one where you read the documentation, and one where you didn't. Branch 1 can be named as read-documentation / main, and Branch 2 can be named fun-implementation-in-life.

## Examples of real world use cases of creating branches for specific tasks:

- you can have specific environments: dev, test main:
  - this is the practice where you write code in the dev branch, test for bugs in the test branch, and release code that you will use to serve customers in main
- you can have branches to specific developers: `prath`, `basch`, ...
  - different people work on files at the same time
- you can have branches for features: `redbull-wing-irl-implementation`, etc.:
  - a good practice is to create a new branch for each feature, and combine (merge) the changes to the main when you are done

## Most Important Git Branch Commands:

```bash
git branch # list all local branches

git branch branch-name # create a new branch under the name branch-name

git checkout branch-name # switch to the branch-name branch

git checkout -b branch-name # creating + switching to a branch branch-name

git branch -d branch-name # delete a branch

git branch -m old-branch-name new-branch-name # rename a branch locally

git branch -a # list all branches locally + REMOTE
```

## Branch Switching: Old vs New Syntax

- **Old way:**  
  `git checkout` was used for both switching branches and restoring files.
  ```bash
  git checkout branch-name         # switch to branch
  git checkout -b new-branch       # create + switch to new branch
  ```

- **New way (recommended):**  
  Git introduced `git switch` (for branches) and `git restore` (for files) to make things clearer.
  ```bash
  git switch branch-name           # switch to branch
  git switch -c new-branch         # create + switch to new branch
  git restore file.txt             # restore file from last commit
  ```

- **Summary:**  
  - Use `git switch` for branch operations (clearer, less error-prone)
  - Use `git restore` to undo file changes
  - `git checkout` still works, but is more ambiguous

- If you’re new to Git, prefer `switch` and `restore` for clarity!
- or don't care or use whatever you like

## Remote Branch Syncing:

- when you create a branch locally and try to push, there is no such branch on remote yet (the branch is only on your local computer, not online)
- you would have to sync your branch to remote:

```
git push -u origin branchname
```

- -u is short for --set-upstream

