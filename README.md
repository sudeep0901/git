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
    git commit id
4. git show origin/main
    this will show remote and local branch diff
5. collbarators
    git pull
    git reset --hard origin/main

# Identify Merged Branches
git branch --merged
git branch --no-merged
git branch -r --merged


# Push new local branch to Remote
```sh
git push -u origin key_feature_merge
```

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

```sh
git branch -d new_feature
git branch -D new_feature //Force Delete
```
## Remote Branch
```sh

git push origin :new_feature
git push origin <local>:<remote>

git push --delete origin new_feature
git push -d origin new_feature

```
# git Prune Stale Branches 
```sh

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

## Annotated Tag
git tag -a v1.0.0 -m "Version 1.0" 06b7639c198b7ad014d1c05d31e366919a9ffea8


### List Tag
git tag
git tag --list
git tag -l

### Search a tag in git
git tag -l "v2*"

## List Tag with annotations

git tag -l -n
git show <tagname>
git diff <tag1> <tag2>

## Delete Tag 
git tag --delete push  
git tag -d push

## Push git Tags to Remote
git push origin <tagName>
### Push all tags to Remote
git push origin --tags

## Delete Remote Tag
git push origin :tagstarted
git push origin --delete tagstarted
git push origin -d tagstarted

## Checkout Tags
Create a  branch and checkout tag
```sh
git checkout -b new_branch tagstarted

Below not preferred -> No Branch only local changes and will be lost when switched to other branch and is detached head
git checkout tagstarted

create a branch and reattach head
git checkout -b temp_branch
```

# Git Interactive
git add -i or interactive

git diff --cached

git add --patch

