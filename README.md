# Git Command Cheat Sheet

This is a quick reference for commonly used Git commands, grouped by functionality. Each command includes descriptions, usage examples, and guidance on when to use it.

---

## 1. Setup and Configuration

### When to Use
Use these commands to configure your Git environment when you set up Git for the first time or want to adjust global settings.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git config --global user.name "Your Name"` | Sets the global name for commits. | `git config --global user.name "John Doe"` |
| `git config --global user.email "your.email@example.com"` | Sets the global email for commits. | `git config --global user.email "john@example.com"` |
| `git config --global core.editor "code --wait"` | Sets a default editor (e.g., VS Code) for Git. | `git config --global core.editor "vim"` |

---

## 2. Starting a Repository

### When to Use
Use these commands to start a new Git repository or clone an existing one.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git init` | Initializes a new Git repository in the current directory. | `git init` |
| `git clone <repository-url>` | Clones an existing repository from a URL. | `git clone https://github.com/user/repo.git` |

---

## 3. Making Changes

### When to Use
These commands help you check the status of changes, stage files, and make commits. Use them as you make edits to your project.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git status` | Shows the current status of files (staged, unstaged, untracked). | `git status` |
| `git add <file>` | Stages changes in the specified file. | `git add index.html` |
| `git add .` | Stages all changed files. | `git add .` |
| `git commit -m "message"` | Commits staged changes with a message. | `git commit -m "Add navbar component"` |
| `git commit --amend` | Updates the last commit (add files or edit message). | `git commit --amend -m "Update navbar component"` |

---

## 4. Branching and Merging

### When to Use
Use these commands to create branches, switch between them, and merge branches. Branching is ideal for developing features independently from the main codebase.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git branch <branch-name>` | Creates a new branch. | `git branch feature/navbar` |
| `git switch <branch-name>` | Switches to the specified branch. | `git switch feature/navbar` |
| `git merge <branch-name>` | Merges the specified branch into the current branch. | `git merge feature/navbar` |
| `git branch -d <branch-name>` | Deletes the specified branch after it’s merged. | `git branch -d feature/navbar` |

---

## 5. Working with Remote Repositories

### When to Use
Use these commands to interact with remote repositories, syncing changes between local and remote branches.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git remote -v` | Lists remote repositories connected to your local repo. | `git remote -v` |
| `git remote add <name> <url>` | Adds a new remote repository. | `git remote add origin https://github.com/user/repo.git` |
| `git fetch <remote-name>` | Fetches changes from a remote repository without merging. | `git fetch origin` |
| `git pull <remote-name> <branch-name>` | Fetches and merges changes from a remote branch. | `git pull origin main` |
| `git push <remote-name> <branch-name>` | Pushes local commits to a remote branch. | `git push origin main` |

---

## 6. Viewing and Undoing Changes

### When to Use
These commands allow you to view commit history, see differences between files, and undo changes as needed.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git log` | Displays commit history for the current branch. | `git log --oneline` |
| `git diff` | Shows differences between the working directory and staging area. | `git diff index.html` |
| `git checkout -- <file>` | Discards changes in the working directory. | `git checkout -- index.html` |
| `git revert <commit-hash>` | Creates a new commit that undoes a specific commit. | `git revert a1b2c3d4` |
| `git reset <commit-hash>` | Resets the current branch to a specific commit. Options: `--soft`, `--mixed`, or `--hard`. | `git reset --hard HEAD~1` |

---

## 7. Stashing and Cleaning

### When to Use
These commands help you temporarily save changes or remove untracked files, allowing you to switch branches or clear clutter in the working directory.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git stash` | Saves changes in a stash to apply later. | `git stash` |
| `git stash apply` | Applies the latest stashed changes to the working directory. | `git stash apply` |
| `git stash clear` | Clears all stashes from the stash list. | `git stash clear` |
| `git clean -f` | Removes untracked files from the working directory. | `git clean -f` |

---

## 8. Additional Commands

### When to Use
These additional commands are useful for specific tasks, like renaming branches, viewing specific commits, or cleaning up commit history.

| Command | Description | Example |
| ------- | ----------- | ------- |
| `git show <commit-hash>` | Displays the changes made in a specific commit. | `git show a1b2c3d4` |
| `git branch -v` | Shows branches with their last commit info. | `git branch -v` |
| `git branch -m <new-name>` | Renames the current branch. | `git branch -m new-branch-name` |
| `git rebase -i <base-branch>` | Squashes multiple commits into one (interactive rebase). | `git rebase -i main` |

---

## Conclusion

Use this cheat sheet as a quick reference for managing Git repositories effectively. Each command plays a unique role in maintaining version control, so understanding when and how to use each one is key to a smooth workflow.
