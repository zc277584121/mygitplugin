---
name: git-commit-push
description: Commit changes and push to origin without creating a PR
allowed-tools:
  - Bash
---

# Git Commit & Push

提交改动并推送到 origin 远端，不创建 PR。

## 触发条件

当用户要求提交改动并 push（但不需要提 PR）时使用此 skill。

## 执行步骤

1. **创建新分支**：`git checkout -b <branch-name>`，分支名由用户指定或根据改动内容自动生成。如果用户希望直接在当前分支提交，则跳过此步。

2. **暂存文件**：`git add` 相关改动文件。不要使用 `git add -A` 或 `git add .`，而是逐个添加相关文件。

3. **提交改动**：
   ```bash
   git commit --signoff --author="Cheney Zhang <277584121@qq.com>" -m "<commit message>"
   ```
   - commit message 用英文编写，简洁描述改动内容。
   - **绝对不要**在 commit message 中提及 AI、Claude、LLM 或任何自动生成相关的字样。

4. **推送分支**：`git push origin <branch-name>`。

## 注意事项

- 提交前检查是否有未暂存的改动需要处理。
- 所有 commit 都需要 `--signoff`，作者为 "Cheney Zhang <277584121@qq.com>"。
- commit message 中不能出现任何 AI 相关字样。
