#### Repo-->GIT_Base

# Basic commands for working with GIT

## Start & settings
+ git help / git help [command name] --> show information by command
+ git config --global [user.name] --> setting your first and last name
+ git config --global [user.email] --> setting your email
+ git config --global color.ui true --> setting the color scheme
+ mkdir [name] --> create a new folder
+ cd [name] --> go to folder
+ git init --> Initializing a folder for working with GIT
+ (Git Bash) --> command line for working from windows

## Basic work
+ git status --> find out the current status of the repository
+ git log --> allows you to view the entire commit history
+ (HEAD) --> indicates the current state of the project
+ HEAD~2 --> move the pointer 2 commits back
+ __ADD__
+ git add [name] --> preparing files for commit
+ git add file1 file2 file3
+ git add . --> add all files in the current folder
+ git add *.java --> add all files in the current folder with the .java extension
+ git add someDir/ --> add all files in the someDir folder
+ git add someDir/*.java --> add all files in the someDir folder with the .java extension
+ git add ”*.java” --> add all files in the project with the .java extension
+ __COMMIT__
+ git commit -m ” message to the commit ” --> make a commit
+ git commit -a -m ” message to the commit ” --> move changes in the file to the tracked zone and add a commit
+ git commit --amend -m ” message to the commit ” --> overwrite the last commit with changes
+ __DIFF__
+ git diff --> shows the difference between the current state of the repository and the last snapshot of the repository
+ git diff --staged --> difference between the current monitored state and the last snapshot of the repository
+ git diff COMMIT_ID --> difference between the current state and the specified snapshot of the repository
+ __RESET__
+ reset --> cancels the changes and rolls back to the old snapshot
+ git reset [--soft | --mixed | --hard] [commit & HEAD~2 & Hash commit]
+ git reset --hard --> returns the project to the specified commit, and completely deletes all commits after the specified one (git reset --hard HEAD~2)
+ git reset --mixed --> returns the project to the specified commit, and transfers all commits after the specified one to the unstaged zone
+ git reset --soft --> returns the project to the specified commit, and transfers all commits after the specified one to the staged zone
+ git reset HEAD~2 (default -> mixed)
+ git reset / git reset --mixed HEAD
+ __CHECKOUT__
+ git checkout [the name of the branch] --> switching between branches
+ git checkout HEAD~2 / git checkout [hash code] --> go back a few commits and view the snapshot
+ git checkout master --> go back to the last commit of the master branch
+ git checkout hash code --file1 --> return the state of file1 from the specified commit
+ git checkout -- . --> return the state of all files to the last commit
+ __CLEAN__
+ git clean -n --> displays which untraceable files will be deleted
+ git clean -f --> deletes untraceable files
+ __REMOTE__
+ git remote -v --> view a list of existing remote repositories
+ git remote add [name of the repository] [the address of the repository] --> add a new remote repository located at the specified address
+ git remote remove [name of the repository] --> delete a repository with the specified name [name of the repository] 
+ git remote show --> view the status of a remote repository
+ __PUSH&PULL__
+ git push [name of the remote repository] [Branch] --> sending a local repository to a remote one
+ git push --delete  [name of the remote repository] [Branch] - 
+ git pull [name of the remote repository] [Branch] --> download updates from a remote repository 
+ __SSH__
+ ls -al ~/.ssh --> checking for ssh keys on the computer
+ ssh-keygen -t rsa -b 4096 -C “your_email@example.com” --> creating an ssh key
+ eval $(ssh-agent -s) --> starting the ssh agent
+ ssh-add ~/.ssh/id_rsa --> adding an ssh key to the ssh agent
+ clip < ~/.ssh/id_rsa.pub --> command to copy the public key
+ __CLONE__
+ git clone [address of the remote repository] --> copy a remote repository

## Working with branches




git branch [the name of the branch] - command for creating a new branch
git branch - view which branch we are currently on
git branch -d [the name of the branch] - command to delete a branch
git branch -r - view the list of remote branches
git merge [the name of the branch] - merges one branch with another
:wq - exit the editor vi
git fetch - download a remote branch from a remote repository
git pull = git fetch + git merge origin/master
fast-forvard - merge without changes in the main branch
