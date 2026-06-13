# AGENT.md

This file records how Codex should help manage this local Git workspace.

## Current Environment

- Workspace root: `D:\07_GIT\git_project`
- Git install path: `D:\07_GIT\Git_software\Git`
- Git executable: `D:\07_GIT\Git_software\Git\cmd\git.exe`
- Git global config: `D:\07_GIT\Git_config\.gitconfig`
- SSH key directory: `D:\07_GIT\SSH_key`
- SSH private key: `D:\07_GIT\SSH_key\id_ed25519`
- SSH public key: `D:\07_GIT\SSH_key\id_ed25519.pub`
- SSH config: `D:\07_GIT\SSH_key\config`
- GitHub username: `3380676313-boop`
- Git email: `3380676313@qq.com`
- Remote repository: `git@github.com:3380676313-boop/git_project.git`
- Default branch: `main`

## Current Capabilities

Codex can help with the following Git operations in this workspace:

- Check local repository status.
- Review changed files before saving.
- Stage selected files safely.
- Create clear commits.
- Push commits to GitHub.
- Pull latest changes from GitHub.
- Explain Git concepts in beginner-friendly language.
- Avoid staging unrelated user work unless explicitly requested.
- Keep Git/SSH configuration files on `D:` instead of `C:`.

## Completed Representative Cases

- Installed Git for Windows to `D:\07_GIT\Git_software\Git`.
- Configured Git user identity:
  - `user.name = 3380676313-boop`
  - `user.email = 3380676313@qq.com`
- Generated SSH key under `D:\07_GIT\SSH_key`.
- Configured SSH to use the custom D drive key path.
- Verified GitHub SSH authentication.
- Initialized `D:\07_GIT\git_project` as a Git repository.
- Linked remote repository `git@github.com:3380676313-boop/git_project.git`.
- Created and pushed the first commit to GitHub branch `main`.

## Git Save Rule

After Codex completes a clear task, Codex should offer or perform a Git save flow:

1. Check status with `git status --short --branch`.
2. Review changed files and avoid unrelated changes.
3. Stage only files related to the completed task.
4. Commit with a clear message.
5. Push to GitHub when the user wants remote backup.
6. Report the commit hash and push result.

## Safety Rules

- Do not stage large cache, virtual environment, or generated folders.
- Do not stage unrelated user work without confirmation.
- Do not delete or overwrite SSH keys.
- Do not put Git software, SSH private keys, or Git config files into this repository.
- Do not use destructive Git commands such as `reset --hard` unless the user explicitly confirms.

