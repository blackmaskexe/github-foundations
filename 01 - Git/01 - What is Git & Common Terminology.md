
## Git is a Distributed Version Control System:
- Git is an example of a distributed version control system (DVCS), created by Linus Torvald (who is also creator of the linux kernel)
- Git is called a version control system because it allows a user to keep track of different versions, create new versions, revert to old versions, and much more for a given codebase (a codebase is simply a combination of all the files that you use in your project)
- Git is called "Distributed" because many developers can work on a Git project (repository) at once locally, and each developer can access the history of the changes made in their projects

## Why do we use Git:
- "Let's work together on this project": Git makes it effortless for multiple people to work and collaborate on the same codebase. People can make their own changes and work on different features, and combine (merge) them at the end of the day
- "Undo Button": revert to old versions of the projects when you mess things. You can define many checkpoints (known as commits) along the way, and you can return back to these checkpoints on demand. Therefore, Git is also very helpful for non-collaborative projects as well.
- "Who did this change": when working on a project in collaboration, you often times need to be able to point to the person who made the changes on the code. This is where you can easily see the history of changes (commits) to see what person contributed what part of the code

## Common Git Terms:
- just glance over these, they will be covered in detail in the upcoming pages

1.  ⭐️ **Repository**: A logical container holding the codebase. Can also be called a "repo" for convenience.
2.  **Commit**: A way to save the changes that you make to a local projects.
3.  **Tree**: The history of a repo (a list of commits, branches, etc)
4.  **Remote**: A version of a project hosted on a remote cloud (this is exactly what GitHub is)
5.  **Branches**: Divergent paths of development, allowing for isolated changes.
    * **Main branch**: The primary branch (the older, less popular term was "master").
6.  **Clone**: Creates a complete local copy of a repo from the remote, including its history (tree).
7.  **Checkout**: Switch between different branches or commits.
8.  **Pull**: Downloads changes from a remote repo and merges them with the current branch. Requires credentials only if the remote repository is private.
9.  **Push**: Uploads local repo changes to a remote repo. Requires credentials to do so. 
10. **Fetch**: Downloads data from a remote repo without merging or integrating it with the local codebase.
11. 13. **Staging files / area**: A location where all of the files that will be committed (changes will be saved) are stored. Files need to be added to the staging area for them to be able to get committed later.
    * **commit**: Saves changes as a snapshot in the local repo.
    * **add**: Adds changes to the staging area for the next commit.
12. **Reset**: Undoes local changes with options to unstage files or reverse commits.
13. **Merge**: Combines two branches into one, giving rise to a single branch that has the changes from both branches

## Graphic visualizing the above Common Terms (Git Workflow):

![[../00 - Resources/Pasted image 20250620233917.png]]















































- each commit (change in code) can be tracked through the history (git tree)
![[Pasted image 20250620233543.png]]

