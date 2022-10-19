# Learning_git
version 1.0
## How to remove changes in GIT
4 steps in git
- hard disk : working area (red)
  - use `git diff & git status & git log` to check status and changes
  - use `git restore filename` to remove hard disk file modification or `git checkout filename` equivalent 
- stage : after `add` status, staging area (green)
  - to remove `add` without remove changes from hard disk , use `git restore --staged filename`  or `git reset filename` 
  - to remove `add` and changes from hard disk, use `git checkout HEAD filename` 
- local git: after `commit` status
  - to remove `commit`, use `git reset --soft HEAD~1` HEAD~1 could be replace by release number
  - to remove `add & commit`, use `git reset HEAD~1`  
  - to remove `add & commit and from hard disk` , use `git reset --hard HEAD~1` 
  - recommend to use `git revert HEAD` instead of above commands when working within a team in the same branch 
- remote: after `push` status, repository 
## How to create new branch
- check branch status `git branch`
- create new branch named dev `git branch dev` && `git checkout dev` 
- or create new and change to dev `git checkout -b dev`
### Once dev branch completed, we need to merge dev to main
- need first checkout to master branch 