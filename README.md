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