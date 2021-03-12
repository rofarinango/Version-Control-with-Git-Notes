# Version-Control-with-Git-Notes
This repository is a summary on how to use version control with git. Git command-line cheatsheet.

## Terminology
* ### Version Control System
A Version Control System is a tool that manages different versions of source code.

* ### Commit
Every time you make a commit you save the state of your project in Git.

* ### Repository / repo
A directory that contains your project work. You can either have a repository locally on your machine or as a remote copy on another computer. A repository is made of commits.

* ### Working directory
The files that are on your computer. When you open your project files up on a code editor, you're working with files in the Working Directory.

* ### Checkout
A checkout is when content in the repository has been copied to the Working Directory.

* ### Staging Area / Staging Index / Index
A file in the Git directory that stores information about what will go into your next commit. You can think of the staging area as a prep table where Git will take the next commit. Files on the Staging Index are poised to be added to the repository.

* ### SHA
The SHA number its basically the ID of each commit. SHA is shorthand for "Secure Hash Algorithm".

* ### Branch
An alternative line of development that diverge from the main line and doenst affect it.

## Create a Repository
- Create a new local repository from scratch

`$git init [project name]`

- Clone from an existing repository

`$git clone [url]`

## Review a Repo's history
- List new o modified files not yet commited

`$git status`
