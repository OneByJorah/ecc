# ecc — Agent Operating System

**Version:** v2.0.0  
**Status:** Active Development  
**Repository:** https://github.com/OneByJorah/ecc

---

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Technology Stack](#technology-stack)
- [Features](#features)
- [Getting Started](#getting-started)
- [Service Management](#service-management)
- [Project Structure](#project-structure)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## Overview

ecc is a harness-native agent operating system for Codex, OpenCode, Cursor, Gemini, Claude Code, and terminal workflows. It provides skills, hooks, rules, MCP conventions, and operator control-plane patterns in a single installable package.

> Formerly described as error-correcting code utilities; the project has grown into a full agent/rules framework.

---

## Architecture

Client → agent runtime (Claude Code / Codex / OpenCode / Cursor / Gemini / terminal) → ecc assets (agents, skills, rules, hooks) → workspace integration (commands, plugins, MCP configs).

State and context are managed via:
- `AGENTS.md` and `WORKING-CONTEXT.md`
- `agent.yaml` for global agent configuration
- `ecc_dashboard.py` for visualization

---

## Technology Stack

| Layer | Stack |
|---|---|
| Runtime | Node.js / Python |
| Packaging | npm / pyproject.toml |
| Config | YAML / JSON / Markdown |
| Integrations | MCP, hooks, CLI shims |
| Dashboard | Python (ecc_dashboard.py) |
| VCS | Git + GitHub (`github.com/OneByJorah/ecc`) |

---

## Features

- **Agent definitions**: 20+ specialized agents in `agents/` (security, code review, build error resolution, e2e, accessibility, etc.).
- **Skills / rules**: reusable conventions under `skills/` and `rules/`.
- **Hooks**: event-driven automation at startup and turn boundaries.
- **MCP integration**: configs under `mcp-configs/` for model-context protocol servers.
- **Multi-harness**: supports Codex, OpenCode, Cursor, Claude Code, Gemini, and terminal runs.
- **Dashboard**: `ecc_dashboard.py` visualizes agent/rules state.

---

## Getting Started

```bash
# 1. Clone
git clone https://github.com/OneByJorah/ecc.git
cd ecc

# 2. Install dependencies
npm install
# and/or
pip install -e .

# 3. Install / bootstrap
./install.sh
# Windows:
# .\\install.ps1
```

Follow `CONTRIBUTING.md` and `DEVELOPMENT.md` for harness-specific setup.

---

## Service Management

```bash
# Dashboard
python ecc_dashboard.py

# Agent invocation (CLI)
# Use your harness CLI and point to this repo as the rules/skills root
```

---

## Project Structure

```
ecc/
├── agents/                    # Agent markdown definitions
├── skills/                    # Skill packages
├── rules/                     # Rule packs
├── commands/                  # CLI commands
├── hooks/                     # Lifecycle hooks
├── mcp-configs/               # MCP server conformations
├── integrations/              # Third-party integrations
├── src/                       # Core source
├── tests/                     # Test suite
├── docs/
├── ecc_dashboard.py
├── agent.yaml
├── AGENTS.md
├── package.json
├── pyproject.toml
└── README.md
```

---

## Screenshots

### ecc
![ecc](assets/hero.png)

### ECC Logo
![ECC Logo](assets/images/ecc-logo.png)

---

## Contributing

1. Create a feature branch off `main`.
2. Follow `CONTRIBUTING.md` and `CODE_OF_CONDUCT.md`.
3. Run lint/tests before submitting a PR.

---

## License

MIT (unless otherwise noted in LICENSE)

---

## Author

Built by **Jhonattan L. Jimenez**.
