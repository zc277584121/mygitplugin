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
| `git-get-notification` | Check GitHub notifications and recent Issues/PRs for monitored repos |
| `git-sync-main` | Sync local main branch with the latest code from official upstream or origin remote |

## Installation

### Via npx skills (works with 40+ agents)

**Claude Code** (project-level):
```
npx skills add zc277584121/mygitplugin -a claude-code
```

**Claude Code** (global, available across all projects):
```
npx skills add zc277584121/mygitplugin -a claude-code -g
```

**Cursor**:
```
npx skills add zc277584121/mygitplugin -a cursor
```

**Other agents** — replace `<agent-name>` as needed:
```
npx skills add zc277584121/mygitplugin -a <agent-name>
```

Common agent names: `windsurf`, `github-copilot`, `cline`, `roo`, `gemini-cli`, `goose`, `kilo`, `augment`.

### Via Claude Code Plugin System

```
/plugin marketplace add zc277584121/mygitplugin
/plugin install mygitplugin
```

## Development

To load the plugin locally for development/testing:

```
claude --plugin-dir /path/to/mygitplugin
```

## Configuration

- GitHub account: `zc277584121`
- All commits are signed off by: `Cheney Zhang <chen.zhang@zilliz.com>`
- Requires `gh` CLI to be authenticated

## License

MIT
