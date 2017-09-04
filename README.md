# QUICK GUIDE TO GIT BASICS

# GIT WORKFLOW
## Working Directory
- Everything that's not saved - like the code we are creating, our files, directories and changes - lives here.

## Staging Area
- This is a file that stores the information about what will go in your next commit - Files and directories that we explicitly add to the staging area. Also known as index.

## Git Repository
- Here is were the files are commmited and where the project up to date lives.


# BASIC COMMANDS

## Account configuration
- git config --global user.email your@email.here
- git config --global user.name yourName
(To configure only the current repository, avoid using --global)

## Add all files in directory (include hidden ones)
- git add -A

## Add multiple files of a certain type
- git add *.extension

## Remove files from staging area
- git reset HEAD <file>

## Ignore files and directories
- Create a file named .gitignore
- Write inside the name of the files and directories Git should ignore

## Check out our commit history
- git log
- To exit git log when the log is too long, press Q

## Check out old commits
- git log
- Find the hash key to the required commit (no need to copy the full hash, a few characters from the beginning would be enough)
- git checkout <hash>
- In order to work with this commit without overwrite your actual branch, move files to a new branch using - git checkout -b <new_branch_name>
- NOTE: When you checkout an earlier commit, you are now in a "detached HEAD" state, this means that you are no longer on the commit that is being pointed to by the HEAD. The HEAD, in git, is a pointer to the most recent commit of whichever branch you are currently on.


## Git Branches
### Listing all branches
- git branch

### Add a branch and move there
- git checkout -b <new_branch_name>

### Move from one branch to another
- git checkout <branch_name>

### Merge a branch
- From the branch where we want to "update"
- git merge <branch_name>
- To exit the message window while merging (in case it appears), use - esc + ctrl + zz or - esc + :wq (both commands perform save and exit)

### Remove a branch
- git branch -d <branch_name>


## Link a repository to GitHub
- git remote add origin <url>
- git remote -v (checks out the remote repository)
- git push origin <branch_name> (push to GitHub)