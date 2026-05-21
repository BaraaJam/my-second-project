# my-second-project's Commands

Following [To-Do List](./Workshop-Git-Github.md)

### Project Progress
[████████████████████████████████████████] 100% Done 🎉

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

# Stage all files
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

## **Collaborating with Pull Requests**
```bash
# 1. Clone a forked repository to my machine
git clone https://github.com/ihabau/lexicon-hello-world

# 2. Check my changes before staging
git status

# 3. Stage and commit my improvements
git add .
git commit -m "Improvement: Fix layout spacing and typos in README"

# 4. Push changes back to my fork before opening a PR on GitHub
git push
```

## **Tagging & Releases**
```bash
# 1. Download approved PR changes from GitHub to my machine
git pull

# 2. Create a version tag with a release description
git tag -a v1.0.0 -m "Release version 1.0.0: Stable HTML and CSS with classmate contribution"

# 3. View all local tags to confirm it was created
git tag

# 4. Explicitly push the tag to GitHub
git push origin v1.0.0
```

## **Branching, Merging, and Cleaning Up**

```bash
# 1. Create and switch to a new feature branch
git checkout -b add-button

# 2. Stage and commit my changes locally on my feature branch
git add index.html style.css
git commit -m "Add double fistbump button and styles"

# 3. Push the feature branch to my GitHub
git push origin add-button

# 4. Switch back to my main branch
git checkout main

# 5. Merge the feature branch changes directly into main locally
git merge add-button

# 6. Push the updated main branch to GitHub
git push origin main

# 7. Delete the local feature branch now that it is fully merged
git branch -d add-button
```