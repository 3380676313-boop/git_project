# 01 - Initialize And Link Remote

Use this when a local folder is not yet a Git repository and needs to connect to GitHub.

## Example

```powershell
cd D:\07_GIT\git_project
git init
git branch -M main
git remote add origin git@github.com:3380676313-boop/git_project.git
git remote -v
git status --short --branch
```

## Verify

```powershell
git ls-remote origin
```

If the command succeeds, SSH and the remote repository are accessible.

## Notes

- Only initialize the project folder, not the whole `D:\07_GIT` directory.
- Do not include `Git_software`, `Git_config`, or `SSH_key` in the repository.

