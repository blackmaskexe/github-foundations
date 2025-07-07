
- used to mark version release of your codebase (for versioning)
- it is a feature of git, and github just implements this feature
- CI/CD pipelines may be configured to deploy on the presence of new tags in the production branch

## Git Tag Commands:
```bash
git tag v1.0.0 # tags a commit
git push --tags # push tags to remote
git checkout v1.0.0 #checkout codebase at a tag
git tag -d v1.0.0 # delete a local tag
git push --delete origin tag-name # delete a remote tag
```

## [Semantic Versioning](https://www.semver.org):
- it is a specific style of naming tags
- it should be followed while naming tags

## Versioning old commits:
- you have to checkout that particular commit by using the commit sha
- then assign the particular tag to that commit