---
layout: post
title:  "My Git Notes"
date:   2019-07-25 18:23:10 +0530
categories: jekyll update
---

# Easy Start

## Step 1: Make a new repo
1. Go to GitHub and create a repo (either public or private). 
2. Copy the SSH link, e.g. `git@github.com:MindAI/git-demo.git`
3. In the local git folder, create a new sub-folder with the same name as the name of the repo, e.g. `git-demo`
4. Change directory to this new sub-folder, e.g. `cd git-demo`
5. `git init`
6. `git remote add origin SSH_link`, e.g. `git remote add origin git@github.com:MindAI/git-demo.git`
  
## Step 2: create files in the repo folder
1. Create those files.
2. `git add .`

## Step 3: commit
`git commit -m commit_message`, e.g. `git commit -m "Initial commit."`

## Step 4: push
`git push origin master`


# Ignoring files in a repo
1. Make a file named `.gitignore`
2. Put the names of the files to be ignored in `.gitignore`, one filename per line.
3. `git add .`
   
    `git commit -m "Adding .gitignore`

    `git push`

# Other commands
`git status`: check changes made to files




