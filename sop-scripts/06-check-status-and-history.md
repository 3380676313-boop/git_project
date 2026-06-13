# 06 - Check Status And History

Use this to understand the current Git state.

## Current Status

```powershell
git status --short --branch
```

## Latest Commits

```powershell
git log --oneline -5
```

## Remote Repositories

```powershell
git remote -v
```

## Branches

```powershell
git branch -vv
```

## Changed Files Summary

```powershell
git diff --stat
```

## Staged Files Summary

```powershell
git diff --cached --stat
```

