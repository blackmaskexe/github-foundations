
- we can link our local repository to a remote repository

## Scenarios to link Local and Remote:
#### 1. you want to commit changes to a blank repository:
```bash
git remote add origin <.git https url of your repo>
git branch -M main
git push -u origin main
```

#### 2. You have a project that you cloned from a repo, and you want to sync changes
- no need to add remote, all information is already in your .git config file for the remote repository, simply use commands like git push, pull, etc