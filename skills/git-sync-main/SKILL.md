---
name: git-sync-main
description: Sync local main branch with the latest code from the official upstream remote
allowed-tools:
  - Bash
---

# Git Sync Main

同步 official remote 的最新主分支代码到本地主分支，并推送到自己的 origin remote。

## 触发条件

当用户要求同步上游代码、更新主分支、或拉取 official 最新代码时使用此 skill。

## 执行步骤

1. **检测主分支名称**：通过 `git remote show official` 或查看本地分支，确定主分支名称（`main` 或 `master`）。

2. **拉取 official 最新代码**：`git fetch official`。

3. **切换到本地主分支**：`git checkout <main-branch>`。

4. **同步代码**：`git reset --hard official/<main-branch>`，将本地主分支重置到 official 最新状态。

5. **推送到 origin**：`git push origin <main-branch> --force-with-lease`，同步自己 fork 的远端主分支。

6. **验证结果**：`git log --oneline -5`，展示最新的几条 commit 确认同步成功。

## 注意事项

- 先确认 `official` remote 存在，如果不存在则提示用户先配置（可使用 `git-fork-clone` skill）。
- 始终使用 `official` 作为上游 remote 名称（而非 `upstream`），以保持一致性。
- 使用 `--force-with-lease` 而非 `--force`，更安全地强制推送。
- 如果当前有未提交的改动，先提示用户处理（stash 或 commit），避免丢失工作。
