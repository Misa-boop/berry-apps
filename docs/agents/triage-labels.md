# Triage Labels

The `triage` skill uses these five canonical labels to move issues through a state machine.

| Label | Role | Description |
|-------|------|-------------|
| `needs-triage` | Needs evaluation | Maintainer has not yet evaluated this issue |
| `needs-info` | Waiting on reporter | More information needed before proceeding |
| `ready-for-agent` | AFK-ready | Fully specified; an AI agent can pick it up with no additional human context |
| `ready-for-human` | Needs human | Requires human implementation or decision |
| `wontfix` | Will not action | Issue will not be addressed |

## Usage in GitHub Issues

Apply these labels directly to issues using the GitHub web UI or CLI:

```bash
# Add a triage label
gh issue edit <number> --add-label "ready-for-agent"

# Remove a label
gh issue edit <number> --remove-label "needs-triage"
```

## State Machine Flow

Issues move through this lifecycle:

```
needs-triage
    ↓
    ├──→ needs-info (awaiting reporter)
    │       ↓
    │       └──→ needs-triage (info received)
    │
    ├──→ ready-for-agent (AFK-ready)
    │       ↓
    │       └──→ [closed]
    │
    ├──→ ready-for-human (needs human)
    │       ↓
    │       └──→ [closed]
    │
    └──→ wontfix (will not action)
            ↓
            └──→ [closed]
```
