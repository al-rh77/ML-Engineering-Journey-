# Git Cheatsheet 

## This md contains majority (not all) of the commands one would need to have a basic understanding of how to navigate through git from pull requests all the way down to basic terminal commands for those who are starting out getting used to Git think of it as a time machine or a super advanced "save" button when you save your work in git its called a commit and lets say you accidently write a code in your project (in github or other software) and it breaks completely you can rollback to how it was before it is an industry standard and if your here to prepare for FAANG internships or jobs I hope this md can help you out a little here is the download link for all types from windows to building it from source! happy learning! 

<https://git-scm.com/install/windows> ## for windows 
<https://git-scm.com/install/mac> ## for mac 
<https://git-scm.com/install/linux> ## for linux 
<https://git-scm.com/install/source> ## build from source 

## One Time Set up 
git config --global user.name "Your Name"        # tells Git your name
git config --global user.email "you@example.com" # tells Git your email
git --version                                    # checks Git is installed

## Getting a project 
git clone <url>        # download a repo from GitHub to your computer make sure its HTTPS
git init               # turn the current folder into a new Git repo

## Daily loop (what we will use 90% of the time)

git pull               # download new changes from GitHub (do this first)
git status             # shows what changed and what's saved
git add .              # stage ALL changed files, ready to save
git add file.py        # stage just one file
git commit -m "message"  # save a snapshot with a short description
git push               # upload your commits to GitHub

# Teamwork and syncing 

git fetch                  # check GitHub for changes WITHOUT applying them
git pull --rebase          # pull, but keep your history in a straight line
git branch -d old-idea     # delete a branch you're done with
git push -u origin branch  # push a new branch to GitHub for the first time

# Looking Around 

git log                # shows your commit history (press q to exit)
git log --oneline      # same, but one short line per commit
git diff               # shows exactly what lines you changed
git remote -v          # shows which GitHub repo you're connected to

# Undoing Mistakes 

git restore file.py            # throw away your unsaved changes to a file
git restore --staged file.py   # un-stage a file (undo git add)
git reset --soft HEAD~1        # undo your last commit, but keep your changes

# Branches

git branch                 # list your branches
git branch new-idea        # create a branch
git checkout new-idea      # switch to it
git checkout -b new-idea   # create AND switch in one step
git merge new-idea         # bring that branch's changes into your current one

# Terminal Basics 

pwd                # shows which folder you're in
ls                 # lists files in the current folder
cd folder-name     # go into a folder
cd ..              # go up one folder
mkdir folder-name  # make a new folder
cat file.txt       # print a file's contents
clear              # clean up the screen

