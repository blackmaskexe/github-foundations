
- it is a specific file in a repo to define individuals or teams that are responsible for specific code in a repo
- ==codeowners specified in the file are automatically assigned pull request reviewing==
- CODEOWNER files uses a similar syntax to .gitignore file
- when a pr is opened that modifies any files matching patterns in the CODEOWNERS file, github automatically requests a review from the specified code owners.

```md
# CODEOWNERS is the name of the file


* @global-owner1 @global-owner2
*.js      @js-owner
*.go      docs@example.com
*.txt     @octo-org/octocats
/build/logs/ @doctocat
docs/* docs@example.com
apps/ @octocat
/docs/ @doctocat
/scripts/ @doctocat @octocat
**/logs @octocat
/apps/ @octocat
/apps/github
/apps/ @octocat
/apps/github @doctocat
```

## Placement of the `CODDEOWNERS file`
Could go either in the following:
- project root
- .github directory
- docs directory