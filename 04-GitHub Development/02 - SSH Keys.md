
- used to authenticate into github for performing git operations on your remote repository
- uses SSH Keys

## Steps Overview:
1. generate ssh key (ssh-keygen on linux-based systems)
2. add the ssh key in Github Settings -> SSH and GPG Keys section
3. Use ssh style address while cloning a repo

## Detailed Steps to use SSH Keys to access GitHub:

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
