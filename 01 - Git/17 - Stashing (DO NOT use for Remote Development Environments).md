
- only use for local development
- used when you want to work on something else, and want to stash the changes away for some time

```bash
git add .
git stash save stashname
```

- to view a list of all stashed changes:
```bash
git stash list
```

- bring back changes from stash:
```bash
git stash pop
```

- bring back last stash:
```bash
git stash apply
```