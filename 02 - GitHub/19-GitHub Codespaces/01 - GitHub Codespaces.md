
@ github.com/codespaces

- Cloud Developer Environment (CDE) integrated with your GitHub Repo
- a codespace runs:
	  - ubuntu linux docker container
	  - on a virtual machine
	  - hosted and managed by GitHub
	  - clones your repo before working into your workspaces folder

## Interactions with CodeSpaces:
1. SSH via GitHub CLI
2. VsCode browser, desktop
3. JetBrains IDE

## GitHub CLI Commands for Codespaces:
```md
- gh codespace code
- gh codespace cp
- gh codespace create
- gh codespace delete
- gh codespace edit
- gh codespace jupyter
- gh codespace list
- gh codespace logs
- gh codespace ports
- gh codespace rebuild
- gh codespace ssh
- gh codespace stop
- gh codespace view
```

## Options presented to you when you create a new CodeSpace:
1. repo
2. branch
3. region
	   - us east
	   - us west
	   - europe west
	   - southeast asia
	   - australias
4. machine type
	   - 2 core (8g ram, 32 gb)
	   - 4 core (16g ram, 32g)
	   - 8 core (32g ram, 64g)
	   - 16 core (32g ram, 128g)
- note that you can change the machine type from within the codespace using the command palate options

## Running a Codespaces from Within a Repo:
- `repo -> code dropdown -> codespaces -> create codespace on branch-name`
  ![[Pasted image 20250629120004.png]]
- alternatively, you can click on the plus icon to customize the machine

NOTE: There is a limit of concurrent codespaces allowed to run