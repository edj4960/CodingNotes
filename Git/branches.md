# Branches

## Delete a local branch

### Delete if branch has no unmerged commits

```git
git branch -d <local-branch>
```

### Delete branch no matter what

```git
git branch -D <local-branch>
```

## Update list of remote branches

```git
git remote update origin --prune
```

## View branches

### View remote branches only

```git
git branch -r
```

### View local and remote branches

```git
git branch -a
```
