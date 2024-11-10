# Git `merge`

```shell
# Attempt to merge branch `feature` into current branch
git merge feature

# Attempt to merge branch `feature` into current branch, but do not commit
git merge --no-commit feature

# Check which commits are involved in the conflict
git log --merge --oneline

# Check files with conflicts
git status

# Abort current merge attempt
git merge --abort
```
