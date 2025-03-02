# Guide to Contributing to a GitHub Repository

This guide explains how to contribute to a public GitHub repository, both with and without Visual Studio Code.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Contributing without VS Code](#contributing-without-vs-code)
  - [1. Fork the repository](#1-fork-the-repository)
  - [2. Clone your fork](#2-clone-your-fork)
  - [3. Create a branch](#3-create-a-branch)
  - [4. Make your changes](#4-make-your-changes)
  - [5. Add and commit your changes](#5-add-and-commit-your-changes)
  - [6. Push your changes](#6-push-your-changes)
  - [7. Create a Pull Request](#7-create-a-pull-request)
- [Contributing with VS Code](#contributing-with-vs-code)
  - [1. Fork the repository](#1-fork-the-repository-with-vs-code)
  - [2. Clone in VS Code](#2-clone-in-vs-code)
  - [3. Create a branch in VS Code](#3-create-a-branch-in-vs-code)
  - [4. Make your changes in VS Code](#4-make-your-changes-in-vs-code)
  - [5. Managing changes with VS Code's Git interface](#5-managing-changes-with-vs-codes-git-interface)
  - [6. Push your changes with VS Code](#6-push-your-changes-with-vs-code)
  - [7. Create a Pull Request from VS Code](#7-create-a-pull-request-from-vs-code)
- [Contribution Best Practices](#contribution-best-practices)
- [Resolving Conflicts](#resolving-conflicts)

## Prerequisites

Before you begin, make sure you have:

- A GitHub account
- Git installed on your machine ([download Git](https://git-scm.com/downloads))
- If using VS Code, ensure it's installed ([download VS Code](https://code.visualstudio.com/download))

## Contributing without VS Code

### 1. Fork the repository

1. Navigate to the GitHub repository you want to contribute to
2. Click the "Fork" button in the top right of the page
3. Select your account as the destination for the fork

### 2. Clone your fork

```bash
# Replace USERNAME with your GitHub username
# Replace REPOSITORY with the repository name
git clone https://github.com/USERNAME/REPOSITORY.git
cd REPOSITORY
```

### 3. Create a branch

```bash
# Make sure you're up to date with the original repository
git remote add upstream https://github.com/ORIGINAL_OWNER/REPOSITORY.git
git fetch upstream
git checkout main
git pull upstream main

# Create a new branch for your contribution
git checkout -b your-branch-name
```

### 4. Make your changes

Edit the files with your preferred text editor.

### 5. Add and commit your changes

```bash
# Check which files have been modified
git status

# Add modified files
git add path/to/modified-file
# Or to add all modified files
git add .

# Commit your changes with a descriptive message
git commit -m "Clear description of the changes made"
```

### 6. Push your changes

```bash
git push origin your-branch-name
```

### 7. Create a Pull Request

1. Return to your GitHub fork in your browser
2. You should see a message suggesting to create a Pull Request for your recently pushed branch
3. Click "Compare & pull request"
4. Add a title and detailed description of your changes
5. Click "Create pull request"

## Contributing with VS Code

### 1. Fork the repository with VS Code

This step is done in the browser, just like in the method without VS Code.

### 2. Clone in VS Code

1. Open VS Code
2. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open the command palette
3. Type "Git: Clone" and select this option
4. Enter your fork's URL (`https://github.com/USERNAME/REPOSITORY.git`)
5. Select a local folder to clone the repository to
6. Click "Open" when prompted

### 3. Create a branch in VS Code

1. Click on the current branch name in the status bar at the bottom left
2. In the palette that opens, select "+ Create new branch"
3. Enter your new branch name and press Enter

Before this, you can configure the original repository:

1. Open a terminal in VS Code (`Ctrl+` or Terminal > New Terminal)
2. Run:
   ```bash
   git remote add upstream https://github.com/ORIGINAL_OWNER/REPOSITORY.git
   git fetch upstream
   git pull upstream main
   ```

### 4. Make your changes in VS Code

1. Navigate in the file explorer on the left
2. Open and modify files as needed

### 5. Managing changes with VS Code's Git interface

1. Click on the "Source Control" icon in the sidebar (or press `Ctrl+Shift+G`)
2. You'll see the list of modified files
3. Hover over a file and click the "+" to add it to the staging area
4. To add all files, click the "+" next to "Changes"
5. Enter a commit message in the field at the top
6. Press `Ctrl+Enter` or click the checkmark to commit

### 6. Push your changes with VS Code

1. Click on the "..." (More actions) in the Source Control view
2. Select "Push"
3. If it's a new branch, VS Code will ask if you want to publish the branch - click "OK"

### 7. Create a Pull Request from VS Code

You can do this directly from VS Code with the GitHub Pull Requests extension:

1. Install the "GitHub Pull Requests and Issues" extension
2. Once installed, click on the GitHub icon in the sidebar
3. Under "Pull Requests", click "Create Pull Request"
4. Fill in your PR details
5. Click "Create"

Alternatively, you can create the PR via the web interface as in the method without VS Code.

## Contribution Best Practices

1. **Clearly name your branch**: use a prefix like `feature/`, `bugfix/`, `docs/` followed by a concise description.
2. **Make atomic commits**: each commit should represent a single logical change.
3. **Write clear commit messages**: use the present imperative tense and explain the "why" of changes.
4. **Test your changes**: ensure your changes work as expected.
5. **Follow the project's style guidelines**: respect the project's code conventions.
6. **Keep your PR focused**: a PR should address just one issue or feature.
7. **Stay up to date**: regularly sync your fork with the original repository.
8. **Respond to feedback**: be responsive during code review.

## Resolving Conflicts

If conflicts arise during your contribution, here's how to resolve them:

### Without VS Code

```bash
# Update your branch with the latest version of main
git fetch upstream
git checkout your-branch-name
git merge upstream/main

# If there are conflicts, Git will tell you
# Open the affected files and resolve the conflicts manually
# Conflicts are indicated by <<<<<<< HEAD ... ======= ... >>>>>>> upstream/main

# Once conflicts are resolved
git add .
git commit -m "Resolve merge conflicts"
git push origin your-branch-name
```

### With VS Code

1. Follow the same steps to update your branch
2. VS Code will display conflicts with a visual interface
3. Click "Accept Current Change", "Accept Incoming Change", "Accept Both Changes", or edit manually
4. Once all conflicts are resolved, commit as usual

---

We appreciate your interest in contributing to this project. If you have questions or need help, feel free to open an issue or contact the project maintainers.