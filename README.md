# GIT UNDERSTANDING

--- 
## Contributors
- Aditya Verma <adityaverma0397@gmail.com>

---
## Commands

* git init - This command turns a directory into an empty Git Repository.

* git add - This command add files to the staging area for Git.
- So when you do git commit, git looks for file which are in staging area. It won't add modified/new files which are not in staging area.

- Usually we do git add .
	* This will add all the files present in local repository into the staging area.

* git commit - This command records the changes made to the files in a local repository. For easy reference, each commit has a unique Commit ID. 
- Syntax  _git commit -m "Commit Message"_

* git status - This command returns the current state of the repository.
- If a file is in the staging area, but not committed, it shows with git status.
- If there are no changes it will return nothing to commit, working directory clean.

* git config - Name and Email address assigned to commits from a local computer.
- With git, there are many configurations and settings possible. git config is how to assign these settings. Two important settings are user.name and user.email. 
- Syntax: _git config --global user.email "adityaverma0397@gmail.com"_  _git config --global user.name "Aditya Verma"_

* git clone - This command creates a local working copy of an existing remote repository.

* git push - Pushing the changes from local to remotely server/repository. 
- Syntax: _git push -u origin branch name_

* git pull - This command pulls the changes from the remote repository to the local computer.

* git stash - To save changes made when they are not in a state to commit them to a repository. (Means Convert dirty directory to clean directory).

1. git stash list
2. git stash show
- The above 2 commands used to know where are the commits done.These commits are placed in stack.

- If work (or bug) fixed in code, then bring the stack content back to untracked file by applying the following command:
**git stash apply**

* git log - It will show you list of commits that you have done in local repository. {This helps give context and history for a repository.

**git log --author="xxxx"**
- This will produce log based on authors

**git log --before="date xxxxx"**
- This will produce log based on date.

* git revert - It helps you to roll back to the previous version of the file.

 **git revert <commit id>**
**git revert HEAD**
- The above command will reflect back to HEAD commit.

* git rebase - Basically, rebase is again one way of combining work between different branch. What rebase does is :- It takes a set of commits, copy them and store outside the repository. Advantage of rebase is that linear sequencing of commits. So commit logs or history logs will be clean if rebase is done. 

**git rebase master**
- The above command basically move our work from current branch to master branch. It looks like it develop sequentially but it develop parallely.

## For Example: -
	* Create a branch - git branch -b xyz
	* Do some changes
	* Trigger above command
	* You see your changes on master

---

## Git Stash
**Git Stash is a command which is used to save the files temporary in stack**
1. We can normally use git stash command just we have to make sure all things are on right place.
2. We can do the following aspects:
- git add
- git status
- git stash
- git stash list 
- git stash show
- git stash apply
* Here the stash changes will go bach to staging area.
- git stash pop
* Did exactly same as git stash apply
- git stash push
* Here it will push the files into the stack exactly same like git stash

---

## Use of Git Rebase command for making only 1 commits from several commits
- git rebase -i HEAD~4
* **4 Represents how many commits to be considered**
* pick which to choose and select s for squash
---
