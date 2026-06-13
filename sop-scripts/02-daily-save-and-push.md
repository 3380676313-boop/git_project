# 02 - Daily Save And Push

Use this after completing a normal task.

## Commands

```powershell
cd D:\07_GIT\git_project
git status --short --branch
git diff --stat
git add <related-files>
git status --short
git commit -m "Describe completed task"
git push
```

## Example

```powershell
git add AGENT.md SOP.md sop-scripts/
git commit -m "Add Git workflow SOP documentation"
git push
```

## Checklist

- Confirm only task-related files are staged.
- Confirm no private key or local config file is staged.
- Confirm push succeeds.

