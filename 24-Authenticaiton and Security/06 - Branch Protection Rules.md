
- used to enforce certain workflows or requirements before changes can be merged into a branch
- under `repo settings -> code and automation -> branches -> branch protection rules` (create or edit)

## Different Rules of Branch Protection Rules: ⭐️
- Protect matching branch rules:
	- Require pr before merging
	- require status checks to pass before merging
	- require conversation resolution before merging
	- require signed commits
	- require linear history
	- require deployments to succeed before merging
	- lock branch
	-  do not allow bypassing the above settings

- Rules applied to everyone (including admins):
	- allow force pushes
	- allow deletions