# Git Version Management SOP

This document is the main index for Git workflows used in this workspace.

## Core Idea

Git is used to save local work as clear versions. GitHub is used to back up and share those versions remotely.

The normal loop is:

```powershell
git status
git add <files>
git commit -m "message"
git push
```

## Before Every Git Operation

Run:

```powershell
git status --short --branch
```

Check:

- Which branch is active.
- Which files changed.
- Whether there are unrelated files.
- Whether ignored folders such as `.venv`, `.pytest_cache`, and `__pycache__` are excluded.

## Task Types

| Task type | Use this SOP script |
| --- | --- |
| Initialize a local folder and link GitHub | `sop-scripts/01-init-and-link-remote.md` |
| Save completed daily work | `sop-scripts/02-daily-save-and-push.md` |
| Start a new task with a branch | `sop-scripts/03-new-task-branch.md` |
| Fix mistakes before commit | `sop-scripts/04-fix-mistake-before-commit.md` |
| Sync remote GitHub changes | `sop-scripts/05-sync-remote-changes.md` |
| Check history and current state | `sop-scripts/06-check-status-and-history.md` |

## Standard Save Flow

Use this when a task is finished and should be saved to GitHub:

```powershell
git status --short --branch
git diff --stat
git add <related-files>
git status --short
git commit -m "Describe completed task"
git push
```

## Branch Rule

- Use `main` for stable saved work.
- Use a new branch for experiments or risky changes.
- Push the branch when the work should be backed up remotely.

Example:

```powershell
git checkout -b task/update-docs
git add AGENT.md SOP.md sop-scripts/
git commit -m "Add Git workflow documentation"
git push -u origin task/update-docs
```

## What "Push To A Specific Branch" Means

Pushing code to a branch means uploading local commits to a named version line on GitHub.

Example:

```powershell
git push -u origin main
```

Meaning:

- `origin` is the GitHub remote repository.
- `main` is the target branch on GitHub.
- `-u` links local `main` with remote `origin/main`.

After this link is created, later pushes can usually use:

```powershell
git push
```

