Start at `AGENTS.md`. This repository is the app workspace.

The overlay is https://github.com/judigot/ai. Fetch
https://raw.githubusercontent.com/judigot/ai/main/AGENTS.md and the files it
names from that same tree. Always use that live tree. Do not clone or download
https://github.com/judigot/ai to load it, and do not read `~/ai` or any other
local clone (those copies can be stale). `~/ai` is only for the optional local
Claude Code plugin (`cc` / `--plugin-dir`).

Do not copy the overlay into this repository, and do not list overlay files here.

The workflow is portable [AGENTS.md](https://agents.md/): plain Markdown that
any coding agent can follow. Cursor and Claude Code files are adapters. They
point at `AGENTS.md`; they do not replace it.

## Files

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | Workflow. Overlay loader plus a repo-specific section. |
| `CLAUDE.md` | Claude Code adapter. Points at `AGENTS.md`. |
| `.cursor/rules/` | Cursor adapter. Always-on rule loads `AGENTS.md`. |
| `agents/` | Project-specific agents only. |
