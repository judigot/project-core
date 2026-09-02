# Project Instructions

This file is the per-project stub from `judigot/project-core`. Copy it into
every app. Do not copy `judigot/ai` into the app.

Load the overlay when `~/ai` is available:

@~/ai/settings/rules.md
@~/ai/settings/workflow.md
@~/ai/settings/stack.md
@~/ai/settings/references.md
@~/ai/settings/ecosystem.md

Application foundation is `judigot/template-monorepo`, not this stub.

## IDE Setup

### Claude Code

```sh
claude   # uses --plugin-dir ~/ai
```

Project-specific agents:

```sh
claude --plugin-dir ~/ai --plugin-dir .
```

### Cursor IDE

- Global overlay: `~/ai/settings/*.md` (not duplicated in this repo)
- Project agents: `@agents/<agent>.md`

## Available Agents

See `agents/*.md`. Add product agents here; do not fork overlay agents from
`~/ai`.

## Directory Structure

```
project/
├── .cursor/rules/
│   ├── global-agents/RULE.md     # always load ~/ai
│   └── project-agents/RULE.md    # load agents/README.md
├── agents/                       # project-specific agents only
│   ├── README.md
│   └── agent-template.md
├── AGENTS.md
└── CLAUDE.md                     # @AGENTS.md
```

## This repository

Replace this section with product-specific guidance. Keep the overlay
includes above unchanged.
