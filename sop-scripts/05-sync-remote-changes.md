# 05 - Sync Remote Changes

Use this when GitHub may have newer code than the local computer.

## Safe Sync Flow

```powershell
cd D:\07_GIT\git_project
git status --short --branch
git fetch origin
git status --short --branch
git pull --ff-only
```

## Meaning

- `git fetch origin` checks GitHub for new commits.
- `git pull --ff-only` updates local code only if Git can do it safely without a merge commit.

## If Pull Fails

Stop and inspect:

```powershell
git status
git log --oneline --graph --decorate --all -10
```

Do not force pull unless the user confirms.

