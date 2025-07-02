
## Why would you even need this?
- you can link issues to a pull request, and once this pull request is approved and merged, these issues will automatically close
- therefore, you won't have to manually specify "Fixes #21" in the message of your commits

## How to Link Issues to PRs:
1. in the description of the pull request, specify the issue number with a particular set of keywords
```md

Link issues with prs in pr description by specifying a keyword + issue #

- close
- closes
- closed

- fix
- fixes
- fixed

- resolve
- resolves
- resolved

example: fixes #21. or resolves #21
```
- you can have the above keyword usage ANYWHERE in the description for the pull request

1. You can also select the issue from the development selection option when editing or creating a pull request