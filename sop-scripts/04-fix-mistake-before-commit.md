# 04 - Fix Mistake Before Commit

Use this when files were changed or staged by mistake, but no commit has been made yet.

## See Current State

```powershell
git status --short
```

## Unstage A File

This keeps the file changes but removes the file from the staging area.

```powershell
git restore --staged <file>
```

## Discard A File Change

Only use this when you are sure the local change should be removed.

```powershell
git restore <file>
```

## Important

- Do not use `git reset --hard` unless the user clearly confirms.
- If unsure, ask before discarding work.

