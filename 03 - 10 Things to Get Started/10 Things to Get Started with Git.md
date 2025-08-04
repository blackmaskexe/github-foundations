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
   - Branches let you work on different features or environments (like dev, test, main, beta) without messing up the main code. Create and switch branches:
     ```bash
     git branch dev      # create a dev branch
     git branch test     # create a test branch
     git branch beta     # create a beta branch
     git checkout dev    # switch to dev branch
     # Or use the new command
     git switch dev
     ```
   - Use branches to safely experiment or develop features before merging them into main.

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
