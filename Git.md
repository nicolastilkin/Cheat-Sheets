# Git Cheat Sheet

## Configuration
```sh
# Set user name and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check configuration
git config --list
```

## Basic Commands
```sh
# Initialize a repository
git init

# Clone a repository
git clone <repo_url>

# Check repository status
git status
```

## Working with Commits
```sh
# Add files to staging area
git add <file>
# Add all files
git add .

# Commit changes
git commit -m "Commit message"

# Amend the last commit
git commit --amend -m "Updated commit message"
```

## Branching and Merging
```sh
# List branches
git branch

# Create a new branch
git branch <branch_name>

# Switch to a branch
git checkout <branch_name>
# Or
git switch <branch_name>

# Create and switch to a new branch
git checkout -b <branch_name>
# Or
git switch -c <branch_name>

# Merge a branch into the current branch
git merge <branch_name>

# Delete a branch
git branch -d <branch_name>
# Force delete
git branch -D <branch_name>
```

## Remote Repositories
```sh
# Add a remote repository
git remote add origin <repo_url>

# Show remote repositories
git remote -v

# Push changes to remote
git push origin <branch_name>
# Push all branches
git push --all origin

# Pull changes from remote
git pull origin <branch_name>
```

## Undo Changes
```sh
# Undo changes in the working directory
git checkout -- <file>

# Unstage a file
git reset HEAD <file>

# Revert a commit
git revert <commit_hash>

# Reset to a previous commit
git reset --hard <commit_hash>
```

## Viewing History
```sh
# View commit history
git log

# View commit history in one line
git log --oneline

# View changes between commits
git diff <commit1> <commit2>
```

## Stashing Changes
```sh
# Stash changes
git stash

# List stashes
git stash list

# Apply last stash
git stash apply

# Drop the last stash
git stash drop

# Apply and remove last stash
git stash pop
```

## Tags
```sh
# Create a tag
git tag <tag_name>

# List tags
git tag

# Push tags to remote
git push origin --tags