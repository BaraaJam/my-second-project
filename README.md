# my-second-project's Commands

## To create and setup
```bash
# Create project folder
mkdir my-second-project

# Initialize git
git init

# Setup documentation
echo "# my-second-project's Commands" >> README.md

# Setup basic webpage
echo Hello World > index.html

# Setup gitignore FIRST to block secrets
echo .env > .gitignore

# Setup secrets file safely AFTER gitignore
echo API_KEY=my_secret_password_123 > .env
```

## Local Repository
```bash
# Check status of files
git status

# Stage all files safely (will ignore .env)
git add .

# Optional: Unstage files if needed
git rm --cached README.md
git rm --cached index.html

# First commit
git commit -m "Initial commit: Simple index and README"

# Stage code and styles together
git add index.html style.css
git commit -m "Add styling and connect external CSS stylesheet"

# Stage gitignore file
git add .gitignore

# Update documentation
git add README.md
git commit -m "Update README with formatted Git commands"
git commit -m "Docs: Restructure guide, fix typos, and add .gitignore"
```

## Remote Repository
```bash
# Link local project to GitHub
git remote add origin https://github.com/BaraaJam/my-second-project.git

# Verify connection
git remote -v

# Push for the first time (sets upstream)
git push -u origin main

# Standard push for all future updates
git push
```
