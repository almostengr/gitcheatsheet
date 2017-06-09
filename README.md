# gitcheatsheet
Cheatsheet of commands to use when working with git. This is a quick reference for the commands that are most commonly used when working with Git.

## git init
Creates a new repository in the current directory. 

## git branch
Lists all of the branches that are in the current branch. 

## git add . 
Adds all the files that have not been staged for commit in the current directory. 

## git status 
Shows the current branch, files that have added but not committed, files that have been removed but not committed, files that have not been staged for committing. 

## git rm FILENAME
Removes files from the repository. If removing directories, "-r" option needs to be used. Replace FILENAME with the name of the actual file. 

## git diff --cached COMMITHASH
Shows the changes that have been made between a previous commit and the files pending commitment. If no files have been staged for commit, then this command will not return any output.  COMMITHASH should be replaced with the unique identifer of a previous commit.

## git log 
Shows the previous commit history. This include the commit message, date, time, author, and commit ID (or hash). 

## git clean
Removes files that are not being tracked.

## git push origin BRANCH
Pushes files from the origin branch to the git server that hosts the repository.  "BRANCH" should be replaced with the name of the branch, although it does not have to be specified. if "BRANCH" is not entered, then the current branch will be pushed.

## git pull origin BRANCH
Pulls the latest version of the branch from your git server. "BRANCH" should be reaplced with the name of the branch, although it does not have to be specified.
