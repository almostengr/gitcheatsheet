# Git Cheat Sheet
Cheatsheet of commands to use when working with git. This is a quick reference for the commands that are most commonly used when working with Git.

A description of what each command does if executed, is provided under each command.

## Commands

### Create a new repository in the current directory

```bash
git init
```

### List all of the branches in the current repo 

```bash
git branch
```

### Stage all of the files in the current directory for commit

```bash
git add .
```

### Stage all of the previously committed files for commit 

```bash
git add -u
```

### Commit the changes made to files

```bash
git commit -m "MESSAGE"
```
"MESSAGE" should be replaced with a details of the changes made since the last commit.

### Clones the repository from the source to your computer

```bash
git clone REPOURL
```

"REPOURL" should be replaced with the URL from the remote repository.

### Show the current branch, files that are staged, and files that are unstaged

```bash
git status
```

### Remove files from the repository 

```bash
git rm FILENAME
```

If removing directories, "-r" option needs to be used. Replace 
```FILENAME``` with the name of the actual file. 

```bash
git diff --cached COMMITHASH
```
Shows the changes that have been made between a previous commit and the files pending commitment. 
If no files have been staged for commit, then this command will not return any output.  
```COMMITHASH``` should be replaced with the unique identifer of a previous commit.

```bash
git diff --cached $(git log | head -1 | awk '{print $2}')
```
Performs the same command above, but automatically gets the latest commit from the ```git log``` 
command. This command will only work on Unix or Linux based systems.

```bash
git diff $(git log | head -1 | awk '{print $2}') $(git log | head -7 | tail -1 | awk '{print $2}')
```
Shows the changes between the latest commit and the previous commit by pulling the commit hash from 
```git log``` command.  This command will only work on Unix or Linux based systems.

```bash
git log
```
Shows the commit history. This include the commit message, date, time, author, and commit ID (or hash). 

```bash
git clean
```
Removes files that are not being tracked.

```bash
git push origin BRANCH
```
Pushes files from the origin branch to the git server that hosts the repository.  ```BRANCH``` should 
be replaced with the name of the branch, although it does not have to be specified. if ```BRANCH``` is 
not entered, then the current branch will be pushed.

```bash
git pull origin BRANCH
```
Pulls the latest version of the branch from your git server. ```BRANCH``` should be replaced with the 
name of the branch, although it does not have to be specified.

```bash
git ls-files --deleted -z | xargs -0 git rm
```
Deletes the local files that have already been removed from the git repo.

```bash
git branch | grep -v master | xargs git branch -D 
```
Deletes all of the local branches except master. Useful for when multiple remote branches have been removed and you need to remove the local corresponding branches.

## Definitions

### commit
A commit is a revision, or set of updates, made to one or more files.

### fork
Makes a copy of repo that is owned by somebody else and allows you to make changes to the code without 
making changes to the original repo.

### issue
Issues are used to track bugs or enhancements for a project.

### merge
Combines changes from two branches into a single branch.

### branch
A version of code in the repository. Changes to the code are normally done in another branch and then 
merged into the master branch of the repository.

### push
To send the code from your local machine to the central repository (server).

### pull 
To get the latest code from the central repository (server) to your local machine.

### clone 
To make a copy of the repository from the central repository (server) to the local machine.

[thealmostengineer.com](http://thealmostengineer.com)

