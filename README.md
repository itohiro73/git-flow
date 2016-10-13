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

### Show changed files only between 2 commits

```
git diff --name-only commit1 commit2
```

### 3 way rebase

```
git rebase --onto commit from_commit to_commit
```

### Add upstream URL

```
git remote add upstream UPATREAM_URL
```

### Delete local branch and remote branch
Delete local branch.
```
git branch -d branch_to_delete
```

Delete remote branch (local branch should have been removed as above).
```
git push origin :branch_to_delete
```

### Add a tag

```
git tag TAG_NAME
```

### Add an annotated tag

```
git tag -am "Message" TAG_NAME
```

### Push a tag to remote (e.g.upstream)

```
git push upstream TAG_NAME
```

### Delete a tag

```
git tag -d TAG_NAME
```

### Cherry pick a commit

```
git checkout branch_name
git cherry-pick commit_to_pick
```

### Stash changes

```
git stash
```

### List stashed changes

```
git stash list
```

### Apply stashed changes without deleting

```
git stash apply
```

### Apply stashed changes and delete it

```
git stash pop
```

### Delete stashed changes

```
git stash drop
```

### Pick particukar stash

```
git stash pop stash@{1}
```
