
- these allow you to attach public keys directly to a git repo
- found within the settings of a repository in github

## Use Case for Deploy Keys:
- when you are using build servers or CI/CD services that need to clone repo to deploy
- single repo access (instead of having a shared key pair, aka the ssh key that we generated in the last page, we just have a key pair for a single git repo)
- avoid using personal account access tokens 