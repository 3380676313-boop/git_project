# 03 - New Task Branch

Use this when starting a larger or risky task.

## Commands

```powershell
cd D:\07_GIT\git_project
git status --short --branch
git checkout -b task/task-name
```

After finishing work:

```powershell
git add <related-files>
git commit -m "Describe task"
git push -u origin task/task-name
```

## Example

```powershell
git checkout -b task/git-docs
git add AGENT.md SOP.md sop-scripts/
git commit -m "Add Git workflow documentation"
git push -u origin task/git-docs
```

## Notes

- Branch names should be short and meaningful.
- Use lowercase words separated by hyphens.

