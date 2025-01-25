# Git Basics - Study Notes

## Introduction to Git
Git is a distributed version control system that helps manage changes to files and directories in a project. Below are key commands and their purposes:

---

## Git Commands Overview

### 1. **Initialize a Repository**
- **Command**: `git init`
- **Purpose**: Initializes a Git repository in the directory, creating hidden files and folders to track changes and versions.

---

### 2. **Check Repository Status**
- **Command**: `git status`
- **Purpose**: Checks the status of the directory for:
  - Untracked files
  - Tracked files with changes
  - Files staged for commit

---

### 3. **Add Files for Tracking**
- **Command**: `git add {filename}`
- **Purpose**: Tracks the specified file, moving it from "untracked" to "staged".

- **Command**: `git add .`
- **Purpose**: Tracks all changes in the current directory, staging them for commit.

---

### 4. **Commit Changes**
- **Command**: `git commit -m "message"`
- **Purpose**: Saves the staged changes with a descriptive message. This is a permanent checkpoint in the project history.

---

### 5. **Undo Staged Changes**
- **Command**: `git restore --staged {filename}`
- **Purpose**: Removes the file from the staging area but keeps the changes in the working directory.

---

### 6. **View Commit History**
- **Command**: `git log`
- **Purpose**: Displays the commit history, showing all the commits made with details like author, date, and commit message.

---

### 7. **Remove a Commit**
Commits in Git are like a stack, built one on top of the other. You can’t directly remove a middle commit but can reset to a previous commit.

- **Command**: `git reset {commit-hash}`
- **Purpose**: Resets the repository state to the specified commit. Use this with care as it can discard changes.

---

### 8. **Stashing Changes**
- **Command**: `git stash`
- **Purpose**: Temporarily saves uncommitted changes without committing them.

- **Command**: `git stash pop`
- **Purpose**: Restores stashed changes and removes the stash.

- **Command**: `git stash clear`
- **Purpose**: Permanently deletes all stashed changes.

---

### 9. **Set Upstream Remote**
- **Command**: `git remote add upstream {repository-URL}`
- **Purpose**: Adds a remote repository named "upstream" (commonly used for the original repository when working with forks).

- **Command**: `git fetch upstream`
- **Purpose**: Fetches changes from the "upstream" remote repository.

- **Command**: `git pull upstream {branch}`
- **Purpose**: Fetches and merges changes from a specific branch of the "upstream" remote repository into the current branch.

---

## Branching and Pull Requests

### 1. **Pull Request**
- **Purpose**: Used to merge a feature branch into the main branch.
- A pull request can contain multiple commits and is essential for collaborative development.

### 2. **Working on Features**
- Create a new branch for each feature:
  - **Command**: `git checkout -b {feature-branch}`
  - Commit changes separately in this branch.

### 3. **Why Use Branches?**
- Enables isolated development for multiple features.
- Avoids conflicts in the main branch.

---

## Summary Table

| Command                          | Purpose                                                         |
|----------------------------------|-----------------------------------------------------------------|
| `git init`                       | Initialize a Git repository                                     |
| `git status`                     | Check the status of files                                       |
| `git add {filename}` / `git add .` | Stage specific/all files for commit                             |
| `git commit -m "message"`         | Commit changes with a message                                  |
| `git restore --staged {filename}` | Unstage a file but keep changes                                |
| `git log`                        | View commit history                                            |
| `git reset {commit-hash}`         | Reset to a specific commit                                     |
| `git stash`                      | Temporarily save uncommitted changes                           |
| `git stash pop`                  | Restore stashed changes                                        |
| `git stash clear`                | Permanently delete all stashed changes                         |
| `git checkout -b {branch}`        | Create and switch to a new branch                              |
| `git pull`                       | Fetch and merge changes from a remote repository               |
| `git push`                       | Push local changes to a remote repository                      |
| `git remote add upstream {URL}`   | Add a remote repository named "upstream"                     |
| `git fetch upstream`             | Fetch changes from the upstream repository                     |
| `git pull upstream {branch}`     | Fetch and merge changes from upstream's branch                 |

---

Use these commands to manage changes effectively and collaborate efficiently in your Git projects!

