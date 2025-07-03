

## The Staging Area:
- this is the place where YOU add changes that you make before committing them: It is like the area you find just before you hit a checkpoint
- Only the changes that are in the staging are are committed (become a checkpoint)
- YOU need to manually add changes to this staging area so that they can be committed later


## Staging Changes / Adding Files to the Staging Area:
- only those files will be committed (saved in history) which are in the staging area while performing a commit operation

- add all possible files to the staging area (files that have had changes to them & not mentioned in the .gitignore) (more on .gitignore later)
```bash
git add .
# OR
git add --all
```
- add only a single file to the staging area:
```bash
git add file-name.extension
```

| `git add .`                                                                  | `git add --all`                                                                                    |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| adds changes to staging area of current working directory and subdirectories | adds changes to staging are for the entire git repository regardless of which subfolder you are in |
