# Notes for git related tips
### Sync from remote master branch to local master branch 
Use case: Make changes directly to remote master branch. Want to sync it to local branch.
```
git fetch origin
git reset --hard origin/master
```
### Squash the commits

```
git rebase -i commit#
```
Then choose squash!

### Add remote URLs

```
git remote add some_name URL 
```

### Catch-up with upatream

```
git fetch --all
git checkout master
git rebase upstream/master master
git push -f origina master
```

### List all authors in the repo

```
git log --all --format='%aN' | sort -u
```

### Checkout tag

```
git tag -l
git checkout refs/tags/7.0.0
```

### Unstage an added file

```
git reset HEAD fileName
```

### Untrack a file that was added one time but now ignored in .gitignore
Reference: http://stackoverflow.com/questions/1274057/making-git-forget-about-a-file-that-was-tracked-but-is-now-in-gitignore

```
git rm --cached <file>
```

### Fixup

```
git commit --fixup=COMMIT_HASH
```

```
git rebase -i --autosquash COMMIT_HASH_TO_REBASE
```
