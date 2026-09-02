# project-core

Per-project agent stub. Copy these files into every app.

The overlay lives in `judigot/ai`. Apps load it from **one entrypoint**:
fetch `https://raw.githubusercontent.com/judigot/ai/main/AGENTS.md` and the
files it names from that same tree. Always use that live tree. Do not clone
or download `judigot/ai` to load it, and do not read `~/ai` or any other
local clone (those copies can be stale). `~/ai` is only for the optional
local Claude Code plugin (`cc` / `--plugin-dir`).

Do not copy the overlay into an app, and do not list overlay files in the app.

The stub is portable [AGENTS.md](https://agents.md/): plain Markdown, no
IDE-specific includes.

```text
judigot/ai            overlay. Start at AGENTS.md. Not the app workspace.
judigot/project-core  these files, in every app
```

## Files

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | Portable overlay loader plus a repo-specific section. |
| `CLAUDE.md` | Points at `AGENTS.md` for tools that still look for that filename. |
| `agents/` | Project-specific agents only. |

If the overlay changes, update this stub, then re-seed projects.
