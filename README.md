# Useful Git commands collected from whole internet

### Remove untracked files/folders

Undo changes to tracked files with:
```
git reset HEAD --hard
```

Remove untracked files with:
```
git clean -f
```

Remove untracked files and directories with:
```
git clean -fd
```
but you can't undo change to untracked files.


Remove ignored and untracked files and directories:
```
git clean -fdx
```
------

### Delete Remote/Local Branch
##### To delete the Remote branch use:
```
git push -d <remote_name> <branch_name>
```
*Note that in most cases the remote name is origin.*

##### To delete the Local branch use one of the following:
```
git branch -d <branch_name>
```
```
git branch -D <branch_name>
```
------

### Rename Branch
If you want to rename a branch while pointed to any branch, do:
```
git branch -m <oldname> <newname>
```

If you want to rename the current branch, you can do:
```
git branch -m <newname>
```
*A way to remember this, is -m is for "move" (or mv), which is how you rename files.* 

------

### Merge Branches
```
git checkout <branch_name>
git pull origin <branch_name>
git merge <with_branch_name>
git push origin <branch_name>
```
------

### To change the last commit
You can simply commit again, using the --amend flag:
```
git commit --amend -m ""
```
------

### Reset origin/<branch_name> to a commit
```
git reset --hard <commit-hash>
git push -f origin <branch_name>
```
