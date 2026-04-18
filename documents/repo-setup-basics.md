# Basic Repo Setup

## Purpose

This note records the common beginner steps for setting up a GitHub repository from scratch.

## Common First Steps

### 1. Define the project goal

Before creating a repo, it is helpful to know what the project is for.

For this project, the goals are:

- build a beginner-friendly portfolio project
- practice Git and GitHub workflow
- learn Markdown and project documentation
- create a repo that can grow into a bilingual study helper

### 2. Create a local project folder

A project usually starts with a folder on the local computer.

Example:

```bash
mkdir bilingual-study-helper
cd bilingual-study-helper
```

What this does:

- mkdir creates a new folder
- cd moves into that folder

### 3. Initialize Git
To turn a normal folder into a Git repository, use:

```
git init
```

What this does:

- creates a Git repository in the current folder
- allows Git to track changes
- starts version control for the project

### 4. Create a GitHub repository
After preparing the local folder, create a repository on GitHub.

Why this matters:

- stores the project online
- makes it possible to push local work to GitHub
- gives the project a public portfolio link

### 5. Connect the local repo to GitHub
After creating the GitHub repo, connect the local repo to the remote repository.

Example:

```
git remote add origin https://github.com/your-username/your-repo-name.git
```

To check the connection:
```
git remote -v
```

Example output:
```
origin  https://github.com/your-username/your-repo-name.git (fetch)
origin  https://github.com/your-username/your-repo-name.git (push)
```
What this means:

- origin is the default name of the remote repository
- fetch is used to download updates
- push is used to upload local commits

### 6. Check repository status
These commands help confirm the current repo situation:
```
git status
git branch
git remote -v
```
What they do:

- git status shows changed files and whether the working directory is clean
- git branch shows the current branch
- git remote -v shows the connected remote repository

### 7. Prepare basic project files
A useful repo usually needs some basic files and folders.

Common examples:
```
README.md
.gitignore
docs/
learning-log/
```
Why they matter:

- README.md explains the project
- .gitignore prevents unnecessary files from being tracked
- docs/ stores supporting documents
- learning-log/ records what I learn step by step

### 8. Make the first commit
After preparing the basic structure, save the first version with Git.

Example:
```
git add .
git commit -m "Initial project setup"
```
What this does:

- git add . stages all current changes
- git commit -m saves a snapshot with a message

### 9. Push to GitHub
After committing locally, upload the work to GitHub.

Example:
```
git push -u origin master
```
What this does:

- pushes the local branch to GitHub
- links the local branch with the remote branch for future pushes
