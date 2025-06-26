
NOTE: When using the CLI, you will be prompted for your username and password. Your github password won't work here, and you MUST use a personal account access token in place of the password. The method to do so is listed as follows:

- these are an alternative way of using passwords for authenticating with GitHub and GitHub API in CLI
- Access Secret equivalent in AWS

## How to obtain a PAT:
- find it in: `GitHub -> Settings -> Developer Settings`
- 

## Types of PATs in GitHub:

1. Classic Tokens:
	   - legacy, less secure

2. Fine-grained personal access tokens:
	   - grant specific permissions
	   - must have an expiry date
	   - can only access specific repos
	   - can only use this to access resources owned by a single user or organization

##  When are these PATs used?
1. Push commits from the CLI
2. Clone a git repo using https
3. When using GitHub SDKs to authorize API call