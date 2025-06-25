
## Setup:
- when you set up git on a machine, you are supposed to set up your name and email as follows:
```bash
git config --global user.name "John Doe"
git config --global user.email "myemail@gmail.com"
```
- this edits the global gitconfig file (more on that later)

## Initialize a Git Repo:
```bash
git init # makes the current folder a git repository
```




- will break the following chunk of basic information into manageable blocks soon TODO

## Staging Changes:
- only those files will be committed (saved in history) which are in the staging area while performing a commit operation

- add all possible files
```bash
git add .
```
- add only a single file:
```bash
git add file-name.extension
```

| `git add .`                                                                  | `git add --all`                                                                                    |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| adds changes to staging area of current working directory and subdirectories | adds changes to staging are for the entire git repository regardless of which subfolder you are in |

## Status:
- shows which files will and will not be committed
```bash
git status
```


## Adding a Remote Repository to sync changes to:

 
## Pushing Changes:
- useful when you want to upload all the changes to the remote origin (remote repository, on providers like github)
```bash
git push
```

## Cloning:
- it means to copy a remote repository onto your local machine
- note that if you just download a github repository, it does not contain the .git folder (the .git folder tells that our project is a git repo)

Ways to Clone:
#### 1\. https
```md
git clone <url>
```
- you will be prompted to log into your github account for this

#### 2\. ssh
i. Generate an SSH RSA Key-Pair (this is a linux command):
```bash
ssh-keygen -t rsa
# when it asks you where to save the key, you will need to enter full filepath
# eg: /home/user/...

# it might ask you for a passphrase (that is the password to access the ssh keys, and it is optional)
```

ii. Read the contents of the ssh key file:
```bash
cat <path where your ssh key is stored>
```
iii. copy the contents of the ssh key file

iv. go to:
```
github -> settings -> ssh and GPG keys -> add new SSH Key
```

iv. you are now free to clone using the ssh link that you copied from the repo you wanted to clone
```bash
git clone git@github.com/... # only able to do this if it's a public repo. If it's private, you would need to have your credentials
```

#### 3\. GitHub CLI
- visit https://www.github.com/cli/cli to view download instructions (to download gh cli)

- authenticate to gh cli
```bash
gh auth login
```
- perform your cloning operations:
```bash
gh repo clone user-name/repo-name
```

## Reset:
- allows to move staged changes to become unstaged changes
- this is useful when you want to make not all files to be committed (pick and choose which to revert)

## Gitconfig file:
- this is what stores your git configurations such as email, name, editor, etc
- could be for local folder or for globally

- showing the contents of the gitconfig file
```bash
git config --list
```

## Viewing Commit History:
```bash
git log
```


## Explore your Git Repository:
- cd into .git folder:
```bash
cd .git
```
- config file will be important