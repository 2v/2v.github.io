---
templateKey: blog-post
id: 1a01d82bc3961a10a49574f75c300fe0
title: Simple Git Reference
slug: /2020/04/03/git
date: 2020-04-03T03:48:03.125Z
description: An easy to read and nicely formatted reference for common Git tasks.
headerImage: https://i.imgur.com/mich3dS.jpg
tags:
  - Reference
  - Programming
  - Git
---

Hello! This page is a collection of useful commands and procedures for using git. I often forget various useful commands, and I know many others who would benefit from a useful list of simplistic commands to get things done in Git, so this article will serve that purpose. This list is not in any particular order, and will likely be added to often.

## General useful status commands  

Commands | Description
--- | ---
`git status` | Gives useful information about the current state of the repo. Good to use after adding files to the staging area, before and after committing changes, and when changing branches.
`git add [filename]` | adds a specific file to the staging area. If the filename is "." all files will be added to the staging area
<br>

## General useful status commands  

Commands | Description
--- | ---
`git clone [github-project-web-address]` | Clone a remote GitHub project to the current directory  
<br>

## Setting username/email for every git project

Commands | Description
--- | ---
`git config --global user.name "firstname lastname"` | Set the name of all Git projects
`git config --global user.email "name@example.com"` | Set the email of all Git projects  
<br>

## Setting username/email for a specific git project


Commands | Description
--- | ---
`git config user.name "firstname lastname"` | Set the name of a Git projects
`git config user.email "name@example.com"` | Set the email of a Git projects  
<br>

## Quickly committing and pushing changes to a project on the master branch


Commands | Description
--- | ---
`git add .` | Stages all currently unstaged files in the current Git repo
`git commit -m 'commit message goes here'` | Commits all staged files with a given message
`git push -u origin master` | Pushes the repository (branch will be remembered using -u flag)  
<br>

## Push a project on any branch

Commands | Description
--- | ---
`git push origin [branch-name]` | Pushes the repository to chosen branch  
<br>

## List branches

Commands | Description
--- | ---
`git branch -a` | Lists all of the branches of a Git repo  
<br>

## All Useful Branch and Merge Commands (https://github.com/joshnh/Git-Commands)

Commands | Description
--- | ---
`git branch` | List branches (the asterisk denotes the current branch)
`git branch -a` | List all branches (local and remote)
`git branch [branch name]` | Create a new branch
`git branch -d [branch name]` | Delete a branch
`git push origin --delete [branch name]` | Delete a remote branch
`git checkout -b [branch name]` | Create a new branch and switch to it
`git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it
`git branch -m [old branch name] [new branch name]` | Rename a local branch
`git checkout [branch name]` | Switch to a branch
`git checkout -` | Switch to the branch last checked out
`git checkout -- [file-name.txt]` | Discard changes to a file
`git merge [branch name]` | Merge a branch into the active branch
`git merge [source branch] [target branch]` | Merge a branch into a target branch
`git stash` | Stash changes in a dirty working directory
`git stash clear` | Remove all stashed entries  
<br>

## Fixing a .gitignore file
This method is useful if a .gitignore file is added after various commits that have already been done to a project. Additionally, if the .gitignore file is no longer preventing files from being staged, this method can help solve any of those problems.  

Commands | Description
--- | ---
`git add .` | Add all untracked files to repo
`git commit -m 'outstanding commit'` | Commit files if necessary. This must be done before removed files that should be uncached by the .gitignore file
`git rm -rf --cached .` | Removes all files from the staging area
`git add .` | Adds all files back to the staging area, this time abiding by the .gitignore file.  