
- it is the divergence of a state of a repository

![[Pasted image 20250624161554.png]]
- in the above example, the person working on feature branch 1 merges their changes with the main branch, and then merge their branch with the main branch. This allows multiple people to work on the same repository together (but on different features)

- you can have specific environments: dev, test main
- you can have branches to specific devs: prath, basch, ...
- you can have branches for features: redbull-wing-irl-implementation, etc

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









## Remote Branch Syncing:
- when you create a branch locally and try to push, there is no such branch on remote yet
- you would have to sync your branch to remote:
```
git push -u origin branchname
```
- -u is short for --set-upstream

## Viewing your Git Tree:
- good extension is Git Graph for VSC

i. Download Git Graph for Visual Studio Code
ii. navigate to Source Control on the left strip of the IDE
iii. click on the second last icon, which will say "View Git Graph (git log)" upon hovering
	![[Pasted image 20250624152950.png]]

iv. you will see a neatly formatted git commit tree


## Checking out to a Commit instead of a Branch
```bash
git checkout <commit hash>
```

