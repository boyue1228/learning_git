# Learning_git

4 steps in git
- hard disk 
  - use `git diff & git status` to check status and changes
  - use `git restore filename` to remove hard disk file modification 
- stage : after `add` status
  - to remove `add` without remove changes from hard disk , use `git restore --staged filename`  or `git reset filename` 
  - to remove `add` and changes from hard disk, use `git checkout HEAD filename` 
- local git: after `commit`status
  - to remove `commit`, use `git reset --soft HEAD~1` 
  - to remove `add & commit`, use `git reset HEAD~1` 
  - to remove `add & commit and from hard disk` , use `git reset --hard HEAD~1` 
  - recommend to use `git revert HEAD` instead of above commands when working within a team in the same branch 
- remote: after `push` status 
