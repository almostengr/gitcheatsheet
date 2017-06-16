# gitcheatsheet
Cheatsheet of commands to use when working with git. This is a quick reference for the commands that are most commonly used when working with Git.

## Commands

### git init
Creates a new repository in the current directory. 

### git branch
Lists all of the branches that are in the current branch. 

### git add . 
Adds all the files that have not been staged for commit in the current directory. 

### git commit -m "MESSAGE" 
Commits the changes made to files, removal of files from the repo, and addition of files to the repo. MESSAGE should be replaced with a details of the changes made since the last commit.

### git clone REPOURL
Makes a copy of the repository from Github to your local computer. This allows for changes to be made from your local computer. REPOURL should be replaced with the URL from the remote repository.

### git status 
Shows the current branch, files that have added but not committed, files that have been removed but not committed, files that have not been staged for committing. 

### git rm FILENAME
Removes files from the repository. If removing directories, "-r" option needs to be used. Replace FILENAME with the name of the actual file. 

### git diff --cached COMMITHASH
Shows the changes that have been made between a previous commit and the files pending commitment. If no files have been staged for commit, then this command will not return any output.  COMMITHASH should be replaced with the unique identifer of a previous commit.

### git log 
Shows the commit history. This include the commit message, date, time, author, and commit ID (or hash). 

### git clean
Removes files that are not being tracked.

### git push origin BRANCH
Pushes files from the origin branch to the git server that hosts the repository.  "BRANCH" should be replaced with the name of the branch, although it does not have to be specified. if "BRANCH" is not entered, then the current branch will be pushed.

### git pull origin BRANCH
Pulls the latest version of the branch from your git server. "BRANCH" should be reaplced with the name of the branch, although it does not have to be specified.


## Definitions
### commit
A commit is a revision, or set of updates, made to one or more files.

### fork
Makes a copy of repo that is owned by somebody else and allows you to make changes to the code without making changes to the original repo.

### issue
Issues are used to track bugs or enhancements for a project.

### merge
Combines changes from two branches into a single branch.

### branch
A version of code in the repository. Changes to the code are normally done in another branch and then merged into the master branch of the repository.

