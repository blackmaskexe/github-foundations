# 10 Things to Get Started with Git

1. **What is Git?**
   - Git is a tool that helps you keep track of changes in your code, work with others, and go back to earlier versions if something breaks. Think of it as a "save point" system for your projects. Every time you commit, you create a checkpoint you can return to later.
   - Git is called "distributed" because every developer has a full copy of the project history on their own computer.

2. **Initialize a Repository**
   - To start using Git in a project, open your project folder in the terminal and run:
     ```bash
     git init
     ```
   - This creates a hidden `.git` folder that stores all your version history.

3. **Configure User Info**
   - Before making commits, set your name and email so your work is properly credited:
     ```bash
     git config --global user.name "Your Name"
     git config --global user.email "your@email.com"
     ```
   - Use your GitHub no-reply email if you want commits to show up on your GitHub profile.

4. **Staging and Committing Changes**
   - Git uses a "staging area" to let you choose which changes to save. Add all changes:
     ```bash
     git add .
     # Or add a specific file
     git add filename.txt
     ```
   - Save your staged changes as a commit (a checkpoint):
     ```bash
     git commit -m "Describe your changes"
     ```
   - Tip: Write clear commit messages so you and your teammates know what changed.


5. **Branching for Environments**
   - Branches are one of the most important features in Git. They let you work on different stages of your project without interfering with each other. In our workflow, we use three main branches:
     - `main`: This is the stable, production-ready branch. Only thoroughly tested code should be merged here. Think of it as the "live" version of your project.
     - `dev`: This is where all new development happens. You and your team write and test new code here. It's normal for this branch to be a bit messy as you experiment and build features.
     - `test`: This branch is for testing code before it goes to `main`. Once something is ready in `dev`, you merge it into `test` to make sure everything works as expected. Only after passing tests does code move to `main`.
   - Why use this workflow?
     - Keeps the main branch clean and stable for releases.
     - Lets you experiment and develop freely in `dev` without breaking the main product.
     - Provides a dedicated place (`test`) to catch bugs before they reach users.
   - How to create and switch between these branches:
     ```bash
     git branch dev      # create a dev branch (if it doesn't exist)
     git branch test     # create a test branch (if it doesn't exist)
     git checkout dev    # switch to dev branch
     # Or use the new command (recommended)
     git switch dev
     ```
   - Typical workflow:
     1. Start on `dev` and make your changes.
     2. When ready, merge `dev` into `test` for testing:
        ```bash
        git checkout test
        git merge dev
        ```
     3. After testing, merge `test` into `main` for release:
        ```bash
        git checkout main
        git merge test
        ```
   - If you no longer need a branch, you can delete it:
     ```bash
     git branch -d branch-name
     ```

6. **Merging Branches**
   - When your feature or fix is ready, merge it into the main branch:
     ```bash
     git checkout main
     git pull origin main   # get the latest main branch from remote
     git merge dev          # merge dev branch into main
     git push origin main   # upload changes to GitHub
     ```
   - Always pull the latest changes before merging to avoid conflicts.

7. **Undoing Mistakes**
   - Git makes it easy to fix mistakes:
     - Undo the last commit but keep your changes:
       ```bash
       git reset --soft HEAD~1
       ```
     - Undo the last commit and remove the changes (careful!):
       ```bash
       git reset --hard HEAD~1
       ```
     - Revert a specific commit (safe for shared branches):
       ```bash
       git revert <commit-hash>
       ```
     - If you committed to the wrong branch:
       ```bash
       git reset HEAD~1
       git checkout correct-branch
       git cherry-pick <commit-hash>
       ```
   - For more advanced fixes, see the "More Useful Commands" section in the docs.

8. **Viewing History and Status**
   - Check what’s changed and see your project’s history:
     ```bash
     git status    # see what files changed and what’s staged
     git log       # see all past commits
     git diff      # see what’s different between versions
     git log --oneline --graph --all --decorate  # pretty graph view
     ```

9. **.gitignore**
   - Use a `.gitignore` file to tell Git which files or folders to ignore (not track). This is useful for things like `node_modules/`, build folders, or secret files.
   - Example `.gitignore`:
     ```
     node_modules/
     *.log
     .env
     dist/
     ```
   - If you already committed a file, remove it from Git but keep it locally:
     ```bash
     git rm --cached filename.txt
     ```

10. **Diagramming Branches in Markdown**
    - You can draw simple diagrams in Markdown to show how branches relate:
    ```
    main
     |
    dev
     |\
    test beta
    ```
    Or use a code block for ASCII art:
    ```text
    *--*--* main
       \
        *--* dev
           \
            * test
            * beta
    ```
    - For more advanced diagrams, check out GitHub Flavored Markdown features in the docs.
