# GitHub

## Authentication
```sh
# Log in to GitHub CLI
gh auth login

# Check authentication status
gh auth status
```

## Repository Management
```sh
# Create a new repository on GitHub
gh repo create <repo_name> --public --source=.

# Clone a GitHub repository
git clone <repo_url>

# List repositories
gh repo list
```

## Working with Issues
```sh
# Create a new issue
gh issue create --title "Bug: Something is broken" --body "Description of the issue"

# List issues
gh issue list

# View an issue
gh issue view <issue_number>

# Close an issue
gh issue close <issue_number>
```

## Working with Pull Requests
```sh
# Create a new pull request
gh pr create --title "Feature: Add new functionality" --body "Description of changes"

# List pull requests
gh pr list

# View a pull request
gh pr view <pr_number>

# Merge a pull request
gh pr merge <pr_number> --merge

# Close a pull request without merging
gh pr close <pr_number>
```

## Releases
```sh
# Create a new release
gh release create <tag_name> --title "Release Title" --notes "Release notes here"

# List releases
gh release list

# View a release
gh release view <tag_name>
```

## Gists
```sh
# Create a new gist
gh gist create <file> --public

# List gists
gh gist list

# View a gist
gh gist view <gist_id>
```

## Actions
```sh
# View GitHub Actions runs
gh run list

# View details of a specific run
gh run view <run_id>

# Re-run a workflow
gh run rerun <run_id>
```

## Forking and Starring
```sh
# Fork a repository
gh repo fork <repo>

# Star a repository
gh repo star <repo>

# Unstar a repository
gh repo unstar <repo>