
- you can configure GitHub codespacest o use dotfilesf rom a specific repository that will be used for all codespaces that you start
  ![[Pasted image 20250629121227.png]]

## Behind the scenes for using this feature:
1. GitHub clones your selected dotfiles repo to the codespaces env
2. looks for one of the following files to setup the environment:
	   - install.sh
	   - instal
	   - bootstrap.sh
	   - bootstrap
	   - script/bootstrap
	   - setup.sh
	   - setup
	   - script/setup