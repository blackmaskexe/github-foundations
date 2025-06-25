
- it is the divergence of a state of a repository

![[Pasted image 20250624161554.png]]
- in the above example, the person working on feature branch 1 merges their changes with the main branch, and then merge their branch with the main branch. This allows multiple people to work on the same repository together (but on different features)














- get a list of all branches
```bash
git branch
```
- create a new branch:
```
git branch branch-name
```
- checkout a branch:
```bash
git checkout branch-name
```
- create new branch + checkout in same command:
```bash
git checkout -b branch-name
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

