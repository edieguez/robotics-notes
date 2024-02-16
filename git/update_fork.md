# Update forked repository

```shell
# List the current configured remote repository for your fork
git remote -v

# Sample output
# origin git@github.com:your_username/your_fork.git (fetch)
# origin git@github.com:your_username/your_fork.git (push)

# Add remote upstream pointing to the original repo
git remote add upstream git@github.com:original_owner/original_repo.git

# Remotes after adding upstream
# origin    git@github.com:your_username/your_fork.git (fetch)
# origin    git@github.com:your_username/your_fork.git (push)
# upstream  git@github.com:original_owner/original_repo.git (fetch)
# upstream  git@github.com:original_owner/original_repo.git (push)

# Fetch the branches and their respective commits from the upstream repository
git fetch upstream

# Rebase the changes from the upstream repository
git rebase upstream/master
```
