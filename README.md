# project-core

Per-project agent stub. Copy these files into every app.

This is not the application template. Application foundations live in
`judigot/template-monorepo`. Global rules, workflow, stack, and skills live
in `judigot/ai` (`~/ai`).

```text
judigot/ai                 global overlay (do not copy into apps)
judigot/project-core       these files, in every app
judigot/template-monorepo  shared application foundation
```

## Files

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | Loads `~/ai/settings/*.md`. Add a repo-specific section below the includes. |
| `CLAUDE.md` | Points at `AGENTS.md`. |
| `.cursor/rules/global-agents/RULE.md` | Always-on Cursor rule that loads the overlay. |
| `.cursor/rules/project-agents/RULE.md` | Points at `agents/README.md`. |
| `agents/` | Project-specific agents only. |

Do not vendor `~/ai` into an app. If the overlay changes, update this stub,
then re-seed projects.
