
## Installation:
- follow the instructions on the [Official Git Download Page](https://git-scm.com/downloads)
- note: should come pre-installed in Linux-based systems

## Setup:
- when you set up git on a machine, you are supposed to set up your name and email as follows:
```bash
git config --global user.name "John Doe"
git config --global user.email "myemail@gmail.com"
```
- this edits the global gitconfig file (See [[Gitconfig file]] for more info)

- NOTE: For commits to count under your GitHub Account, you would need to enter the no-reply email that GitHub assigns to you
	1. Make sure you are logged into github.com in your browser
	2. Visit https://github.com/settings/emails
	3. Look for the "Keep my email address private" section, and look for your no-reply email id (It should look something like 123456+your-github-username@users.noreply.github.com)
	4. run `git config --global user.email = "123456+your-github-username@users.noreply.github,com"`
	5. Now, any commits that you make to github repos will show under your github profile
	6. You can put the user.name as anything (Either your github username or your actual name, it does not matter)

## Initialize a Git Repo:
```bash
git init # makes the current folder a git repository
```
- makes the current folder you are in (found using running `pwd` on the terminal) ready for Git Version Control
- Make sure to run this command before running any other git commands and operations

## Optional: Explore your Git Repository Configuration:
- cd into .git folder:
```bash
cd .git
```
- The config file inside the .git folder will store important information regarding your repo, such as:
	- the name of your default branch
	- names of your remote
	- and much more (you should explore for yourself)
	- you can also simply type `git config --list` to view the contents of the ./git/config file without having to actually navigate to it













## Reset:
- allows to move staged changes to become unstaged changes
- this is useful when you want to make not all files to be committed (pick and choose which to revert)

