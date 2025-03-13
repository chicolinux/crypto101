# Introduction to Git

This is more like a cheatsheet to Git, a quick way to have a reference to git commands that are used on a daily basis. For a more 
comprehensive coverage of Git check the [tutorial](https://git-scm.com/docs/gittutorial).

## Get help
git --help
git <command> --help

## Get git version
git --version

## Create a new repo with a specific name
git init cpv101

## Check the status of the repo (from within the repo dicrectory); what files are being tracked or not?
git status

## Convert an existing project or directory into a git repo
git init

> ** DO NOT CREATE NESTED REPOS! **

## Git workflow
- Create your files and directories, business as usual.
- Start tracking the files and directories you are interested in tracking.
- Commit all changes on your tracked files, this is like taking a snapshop at that point in time.

## Tracking files and directories
- git add <filename>
- git add . 

## Making a commit
git commit -m "My initial commit"

## Commit structure
- commit
- tree
- BLOB (Binary Large Object)

## Check the commit history, from most recent to last.
git log 
git log -3
git log <filename>
git log -3 <filename>
git log --since="Apr 02 2024" --until="Apr 11 2024"

## View a specific commit using it's hash
git show 78df435xd

## Comparing versions of files. Difference between the last committed version and the current untracked version.
git diff <filename>

## Difference between the last committed version and the staged one
git diff --staged <filename>
git diff --staged

## Comparing two commits. Put most recent hash second. HEAD=state in latest commit.
git diff HEAD~1 HEAD

## Reverting commits, fixing errors. Restoring a repo to the state prior to the previous commit.
### revert: reinstates previous versions and makes a commit. It works on commits, not individual files.
git revert HEAD
git revert --no-edit HEAD //no text editor
git revert -n HEAD // no commit


## Revert a single file
git checkout  HEAD~1 -- <filename>

## Unstaging a file
git restore --staged <filename>

## Unstaging all files
git restore --staged

## Default branch in Git: main
## Identifying branches
git branch

## Switching between branches
git switch <branch_name>

## Creating a new branch
git branch <branch_name>

## Switching to a different branch
git switch <branch_name>

## Create and switch to new branch
git switch -c <branch_name>

## Comparing between branches
git diff <branch_name> <branch_name>
git diff <branch_name> <filename>

## Renaming a branch
git branch -m <current_name> <new_name>

## Deleting a branch
git branch -d <branch_name>

## Force deletion of a branch
git branch -D <branch_name>

> When merging two branches, the last commits from each branch are called parent commits. * source * the branch we want to merge from. * destination * the branch we want to merge into. When merging branches, we must first switch to the destination branch.

## Merging branches
git merge <source_branch_name>
git merge <source_branch_name> <destination_branch_name>

## Cloning a repo (making a local copy)
git clone <path_to_repo> <new_repo_name>

## Cloning from a remote repo such as Github (git remembers where the original was). The remote repo is called: origin
git clone URL
git clone PATH
git remote -v

## Create a remote repo
git remote add <name_repo> <URL>

## From remote to local repo. Fetching from a remote.
git fetch origin

> Fetch all remote branches. Might create new local branches if they only existed in the remote. Doesn't merge the remote's contents into local repo.

## Fetching a remote branch
git fetch origin main

## After fetching we need to sync between remote and local. Uses default remote and current local branches.
git merge origin

## Fetch & Merge. Uses default remote and current local branches.
git pull origin
git pull origin <branch_name>

## Push to remote 
git push <remote> <local_branch_name>
git push origin main

## Creating a new remote branch: hotfix branch only exists locally
git push origin hotfix

## The end!
