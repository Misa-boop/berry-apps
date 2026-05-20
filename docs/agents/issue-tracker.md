# Issue Tracker: GitHub

Issues are tracked in the repo's GitHub Issues at https://github.com/Misa-boop/berry-apps/issues.

## Workflow

1. **Create**: Use `gh issue create` or the GitHub web UI
2. **Triage**: Apply one of the triage labels
3. **Update**: Edit the issue or add comments as work progresses
4. **Close**: Mark as resolved when complete

## Labels

The triage skill uses these labels (see `docs/agents/triage-labels.md`):
- `needs-triage` — maintainer needs to evaluate
- `needs-info` — waiting on reporter
- `ready-for-agent` — fully specified, AFK-ready
- `ready-for-human` — needs human implementation
- `wontfix` — will not be actioned

## CLI Usage

This project uses the GitHub CLI (`gh`) for issue management:

```bash
# Create a new issue
gh issue create --title "Issue title" --body "Description..."

# List issues
gh issue list

# View an issue
gh issue view <number>

# Add a label
gh issue edit <number> --add-label "needs-triage"
```

## Why GitHub

This project has a GitHub remote (`https://github.com/Misa-boop/berry-apps.git`). Using GitHub Issues provides:
- Built-in collaboration features
- Integration with pull requests
- Native label and milestone management
- Web UI accessibility
- Standard GitHub workflow compatibility