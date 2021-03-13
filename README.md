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
Create a new local repository from scratch

`$git init [project name]`

Clone from an existing repository

`$git clone [url]`

Change default branch name.
`$git config --global init.defaultBranch [branchname]`

## Review a Repo's history
List new o modified files not yet commited

`$git status`

Show the changes to files not yet stage.

`$git diff`

Show full change history

`$git log`

List commits per line, shows the first 7 characters of the commit's SHA and shows the commit message.

`$git log --oneline`

Display the files that has been modified, displays the number of lines that have been added/removed and displays a summary line with the total number of modified files and lines that have been added/removed.

`$git log --stat`

Displays the files that have been modified, displays the location of the lines that have been added/removed and displays the actual changes that have been made.

`$git log -p`

You can supply the SHA of a commit as the final argument for these commands, by supplying a SHA, the command will start at that commit. No need to scroll through everything.

`$git log -p [commit's SHA]`

Show only one commit, by default display the commit, the author, the date, the commit message, the patch information.

`$git show` or `$git show [commit's SHA]`

## Making a change

Add all modified files to the stage area.

`$git add .`

Add a file to the stage are.

`$git add [filename]`

Commit all staged files to versioned history.

`$git commit -m "commit message"`

Remove file from the stage area while keeping the file changes.

`$git reset [filename]`

Revert everything to the last commit.

`$git reset --hard`

## Tagging, Branching and Merging.

Add a marker to the most recent commit. The tag does not move aroud as new commits are added. Add a tag to a specific commit if a SHA is passed.

`$git tag -a [tagname]` or `$git tag [tagname] [commit's SHA]`

List all branches

`$git branch`

Create a new branch

`$git branch [branchname]`

Delete the [branchname] branch.

`$git -d [branchname]`

Switch between branch.

`$git checkout [branchname]`

Combine branches, current branch and [other-branchname].

`$git merge [other-branchname]`

## Syncronize

Push a project upstream.

`$git push [remote] [branchname]`

Get the last changes from origin (no merge).

`$git fetch`

