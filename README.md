# mygitplugin

A Claude Code plugin for automating common Git/GitHub workflows.

## Skills

| Skill | Description |
|-------|-------------|
| `git-fork-clone` | Fork a GitHub repo and clone it locally with proper remote setup |
| `git-commit-pr` | Commit changes and create a PR to the upstream (official) repo |
| `git-create-repo` | Create a new GitHub repo and clone it locally |
| `git-commit-push` | Commit changes and push to origin (no PR) |
| `git-summarize-weekly` | Summarize weekly GitHub contributions for weekly reports |

## Installation

### Via Marketplace

1. Add the marketplace source:
   ```
   gh repo clone zc277584121/mygitplugin ~/.claude/plugins/marketplaces/mygitplugin-marketplace
   ```

2. Install the plugin in Claude Code:
   ```
   /plugins install mygitplugin
   ```

### Manual Installation

Clone this repo and add it as a local plugin in Claude Code.

## Configuration

- GitHub account: `zc277584121`
- All commits are signed off by: `Cheney Zhang <277584121@qq.com>`
- Requires `gh` CLI to be authenticated

## License

MIT
