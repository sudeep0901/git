# git
git practice

# Force push to remote

## Ignore remote version and push local version forcefully

sh```
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