
- TLDR: A commit represents a checkpoint of the changes that you make to the codebase. You can return back to this checkpoint in case things go wrong, or if you would like to access files at the checkpoint from the future

## What Exactly is a Commit?
- It is a snapshot of your project at a specific point of time
- Contains references to additions, modifications, deletions (not the actual files but only references, making a commit extremely lightweight)

## What is inside a commit:
- tracking of additions, modifications and deletions of files
- does not contain the files itself (therefore, lightweight), but only the additions and deletions
- each commit has a SHA hash id (commit hash), used to identify particular commits
- has the author email and name (that you set in the gitconfig)
- could contain commit messages (It is important to write descriptive commit messages)
- timestamp
- parent commit hashes
- snapshot of content (reference of files at the time of doing the commit)





## Making Commits

1. **Stage your changes**  
   Add files to the staging area:
   ```bash
   git add path/to/file
   ```

2. **Create a commit**  
   Save staged changes with a message:
   ```bash
   git commit -m "Your descriptive commit message"
   ```
- TIPS and CONVENTIONS:
	- Make your commit descriptions as descriptive as possible. This not only helps you to find ideal checkpoints to revert back to in the future, but also helps your team mates get a gist of what changes you made without actually looking at the changes in code, saving your and their time
	- **Commit Early and Often**: There is no harm or implications of committing multiple times, this not only safeguards your work, but could also help you pinpoint exact areas of the code that are causing issues
	- Convention to write Commit Messages: use imperative + present tense. For example:
		- Added logic for logging users into the application ❌
		- Add logic for logging users into the application ✅😎
		- The above is just a convention, it is up to you to follow it or not. I won't feel bad if you don't 😉

### Advanced Commit Commands

- **Commit all tracked, modified files**  
	- this is two commands in one: `git add .` + `git commit -m 'message`
	- drawback: new files that are added (newly created files) are not tracked, you have to manually do git add . / --all in that case
  ```bash
  git commit -a -m "Message"
  ```

- **Amend the most recent commit**
  ```bash
  git commit --amend
  ```

- **Create an empty commit**  
  (Useful for triggering CI/CD or marking a point in history)
  ```bash
  git commit --allow-empty -m "Empty commit"
  ```

- **Commit with a specific author**
  ```bash
  git commit -m "Message" --author="Author Name <email@example.com>"
  ```

---


- Visualization of Commits in Git Graph (a VSCode Extension to visualize your commits, branches, etc)
![Pasted image 20250620233543.png](../00%20-%20Resources/Pasted%20image%2020250620233543.png)

