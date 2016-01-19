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
