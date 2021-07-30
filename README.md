# git
git practice

# Force push to remote

## Ignore remote version and push local version forcefully

```sh
git push -f or --force
```

Steps
1. Advance remote repo from Local repo
2. git fetch
3. Inspect changes
    git log origin/main
    get commit id
4. git show origin/main
    this will show remote and local branch diff
5. collbarators
    git pull
    git reset --hard origin/main

# Identify Merged Branches
git branch --merged (shows - Merged branches)
git branch --no-merged (show branches which are not yet merged into main branch)
git branch -r --merged (check remote branch for branches)


# Push new local branch to Remote
```sh
git push -u origin key_feature_merge
```

# Delete a git branch

## Local Branch
git branch -d new_feature
git branch -D new_feature //Force Delete

## Remote Branch
git push origin :new_feature
git push origin <local>:<remote>

git push --delete origin new_feature
git push -d origin new_feature


# git Prune Stale Branches 
Delete all stale remote tracking branches
Stale branch: a remote trackign branch that no longer tracks anything because actual branch in remote is deleted

git remote prune origin

git remote prune origin --dry-run

git fetch -p

git config --global fetch.prune true

git prune (prunes all unreachable objects)
or
git gc

# Tags in git
Tag is a name to a commit
## Light weight Tags

git tag issue1234 <CommitID>