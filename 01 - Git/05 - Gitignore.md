# .gitignore

- `.gitignore` is a file in your git repository that tells Git which files or folders to ignore in a project (they won’t be tracked or committed)
- Useful for ignoring build artifacts, logs, OS files, IDE configs, secrets, etc.

## How it works:
- Place a `.gitignore` file in your repo root (or any subfolder)
- Add patterns (one per line) for files/folders to ignore
- Example:  
  ```
  node_modules/
  *.log
  .env
  dist/
  .DS_Store
  ```

## Common Patterns:
- `*.log` – ignore all `.log` files
- `node_modules/` – ignore the `node_modules` folder (Node.js projects)
- `dist/` or `build/` – ignore build output
- `.env` – ignore environment variable files
- `.DS_Store` – macOS system file

## Global .gitignore:
- You can set a global `.gitignore` for your user (applies to all repos)
- Example (Windows):
  ```bash
  git config --global core.excludesfile %USERPROFILE%\.gitignore_global
  ```
- Add patterns to `%USERPROFILE%\.gitignore_global`

## Pro tips:
- `.gitignore` only affects untracked files. If you already committed a file, you need to remove it from the repo:
  ```bash
  git rm --cached filename
  ```
- You can have multiple `.gitignore` files in subfolders for more granular control

---

## Sample .gitignore files for popular languages

> Copy the relevant section below and use it as your `.gitignore`!

### Python
```gitignore
# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class

# Distribution / packaging
build/
dist/
*.egg-info/

# Virtual environments
.venv/
env/
venv/

# IDEs
.vscode/
.idea/

# OS files
.DS_Store
Thumbs.db
```

### JavaScript / Node.js
```gitignore
# Node modules
node_modules/

# Logs
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# Build output
dist/
build/

# Environment variables
.env

# IDEs
.vscode/
.idea/

# OS files
.DS_Store
Thumbs.db
```

### Java
```gitignore
# Compiled class files
*.class

# Log files
*.log

# BlueJ files
*.ctxt

# Mobile Tools for Java (J2ME)
.mtj.tmp/

# Package Files #
*.jar
*.war
*.ear

# IDEs
.vscode/
.idea/
*.iml

# OS files
.DS_Store
Thumbs.db
```