# Git Cheatsheet

This file covers most (not all) of the commands you need to get comfortable with Git, from daily pull/push all the way down to basic terminal commands. It's for anyone just getting started.

Think of Git as a time machine, or a super advanced "save" button. When you save your work in Git, it's called a **commit**. If you accidentally break your project, you can roll back to how it was before. Git is the industry standard, so if you're preparing for FAANG internships or jobs, I hope this helps you out a little. Happy learning!

## Download Git

- [Windows](https://git-scm.com/install/windows)
- [Mac](https://git-scm.com/install/mac)
- [Linux](https://git-scm.com/install/linux)
- [Build from source](https://git-scm.com/install/source)

## One-Time Setup

```
git config --global user.name "Your Name"         # tells Git your name
git config --global user.email "you@example.com"  # tells Git your email
git --version                                     # checks Git is installed
```

> Tip: `&&` chains commands together. The next command only runs if the previous one worked.

## Getting a Project

```
git clone <url>   # download a repo from GitHub to your computer (use the HTTPS link)
git init          # turn the current folder into a new Git repo
```

## Daily Loop (what you'll use 90% of the time)

```
git pull                 # download new changes from GitHub (do this first)
git status               # shows what changed and what's saved
git add .                # stage ALL changed files, ready to save
git add file.py         # stage just one file
git commit -m "message"  # save a snapshot with a short description
git push                 # upload your commits to GitHub
```

## Teamwork and Syncing

```
git fetch                  # check GitHub for changes WITHOUT applying them
git pull --rebase          # pull, but keep your history in a straight line
git branch -d old-idea     # delete a branch you're done with
git push -u origin branch  # push a new branch to GitHub for the first time
```

## Looking Around

```
git log            # shows your commit history (press q to exit)
git log --oneline  # same, but one short line per commit
git diff           # shows exactly what lines you changed
git remote -v      # shows which GitHub repo you're connected to
```

## Undoing Mistakes

```
git restore file.py           # throw away your unsaved changes to a file (permanent!)
git restore --staged file.py  # un-stage a file (undo git add)
git reset --soft HEAD~1       # undo your last commit, but keep your changes
```

## Branches

```
git branch                # list your branches
git branch new-idea       # create a branch
git checkout new-idea     # switch to it
git checkout -b new-idea  # create AND switch in one step
git merge new-idea        # bring that branch's changes into your current one
```

## Terminal Basics

```
pwd                # shows which folder you're in
ls                 # lists files in the current folder
cd folder-name     # go into a folder
cd ..              # go up one folder
mkdir folder-name  # make a new folder
cat file.txt       # print a file's contents
clear              # clean up the screen
```