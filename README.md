# git-commands
Frequently used git commands

# initialize git
```shell
git init
```

# see what you have changed since the last commit
```shell
git diff
```

# stage files for committing
```shell
git add .
```

# commit changes
```shell
git commit -m "Made some changes"
```

# create a branch and switch to it
```shell
git checkout -b issue87
```

# list branches
```shell
git branch
```

# switch to a different branch
```shell
git checkout issue13
```

# change remote 
```shell
git remote remove origin
git remote add origin https:#github.com/dancancro/ng2-redux-form
```

# save changes without committing them so you can go to a different branch and come back later
```shell
git stash
```

# restore stashed changes
```shell
git stash apply
```

# push the current branch to the same name on the remote
```shell
git push origin HEAD
```

# compare two branches
```shell
git diff branch1..branch2
```

# delete a local branch
```shell
git branch -d branchname
```

# delete a remote branch
```shell
git push origin --delete branchname
```

# merge a branch into another branch
```shell
git checkout dest_branch
git merge source_branch
```

# discard all unstaged changes in the current branch
```shell
git checkout -- .
```

# Remove untracked files from the working tree
```shell
git clean -xfd
```

# [Create a new branch with changes](http://stackoverflow.com/questions/3899627/create-git-branch-with-current-changes)
```shell
git branch mynewbranch
git git reset --soft HEAD~3 # only if you want to undo last 3 commits
git checkout mynewbranch
```

# [Combine commits from a branch and merge it into another branch](http://stackoverflow.com/questions/5308816/how-to-use-git-merge-squash)
```shell
git checkout master
git merge --squash bugfix
git commit
```

# Undo last commit without undoing the changes. 
Do this so you can see the differences between your files and a previous commit. Repeat the command until you reach the point
against which you want to compare your current files 

```shell
git reset --soft HEAD~
```

# Rename a branch
1. Rename your local branch.
If you are on the branch you want to rename:

```shell
git branch -m new-name
```

If you are on a different branch:

```shell
git branch -m old-name new-name
```

2. Delete the old-name remote branch and push the new-name local branch.

```shell
git push origin :old-name new-name
```

3. Reset the upstream branch for the new-name local branch.
Switch to the branch and then:

```shell
git push origin -u new-name
```

# Useful articles

[Writing a good commit message](https://chris.beams.io/posts/git-commit/)
[Set of useful commands like this but much better](https://www.atlassian.com/git/tutorials/rewriting-history)
