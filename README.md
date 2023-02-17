# GIT AND GITHUB

## Version Control System
        Version Control System (VCS) is a software that helps software developers to work together and maintain a complete history of their work.

        -Centralized version control system (CVCS).
        -Distributed/Decentralized version control system (DVCS).

## General workflow
![git workflow](https://www.tutorialspoint.com/git/images/life_cycle.png)


## Initializing a repository
-git init

### Staging files
git add file1.js           - Stages a single file\
git add file1.js file2.js  - Stages multiple files\
git add *.js               - Stages with a pattern\
git add .                  - Stages the current directory and all its content

## Viewing the status
git status       - Full status\
git status -s    - Short status

## Committing the staged files
git commit -m “Message” - Commits with a one-line message\
git commit              - Opens the default editor to type a long message

## Removing files
git rm file1.js           - Removes from working directory and staging area\
git rm --cached file1.js  - Removes from staging area only


## Renaming or moving files
git mv file1.js file1.txt

## Viewing the staged/unstaged changes
git diff            - Shows unstaged changes\
git diff --staged   - Shows staged changes\
git diff --cached   - Same as the above

## Viewing the history
git log              - Full history\
git log --oneline    - Summary\
git log --reverse    - Lists the commits from the oldest to the newest

## Viewing a commit
git show HEAD - Shows the last commit\
git show HEAD~2 - Two steps before the last commit\
git show HEAD:file.js - Shows the version of file.js stored in the last commit

## Unstaging files (undoing git add)
git restore --staged file.js - Copies the last version of file.js from repo to index

## Viewing the history
git log --oneline\
git log -3  -  Shows the last 3 entries \
git log hash1..hash2  -  Range of commits\
git log file.txt - Shows the commits that touched file.txt\
git log --stat file.txt - Shows statistics (the number of changes) for file.txt\
git log --patch file.txt - Shows the patches (changes) applied to file.txt

## Comparing commits
git diff HEAD~2 HEAD  -Shows the changes between two commits\
git diff HEAD~2 HEAD file.txt - Changes to file.txt only

## Finding contributors
git shortlog

# Branching & Merging

## Managing branches
git branch bugfix - Creates a new branch called bugfix\
git checkout bugfix - Switches to the bugfix branch\
git switch bugfix - Same as the above\
git switch -C bugfix - Creates and switches\
git branch -d bugfix - Deletes the bugfix branch

## Comparing branches
git log master..bugfix- Lists the commits in the bugfix branch not in master\
git diff master..bugfix - Shows the summary of changes

## Stashing
git stash push -m “New tax rules”- Creates a new stash\
git stash list - Lists all the stashes\
git stash show stash@{1} - Shows the given stash\
git stash show 1 - shortcut for stash@{1}\
git stash apply 1- Applies the given stash to the working \dir
git stash drop 1 - Deletes the given stash\
git stash clear - Deletes all the stashes
