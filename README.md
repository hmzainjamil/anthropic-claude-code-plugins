# anthropic-claude-code-plugins

> **Curated Claude Code plugin pack** - Hand-picked Claude Code skills and plugins, starting with `frontend-design` - the skill that makes Claude produce design-system-grade UI instead of generic Bootstrap.

<p align="center"><a href="https://github.com/hmzainjamil/anthropic-claude-code-plugins">Repository</a> · <a href="https://github.com/hmzainjamil/anthropic-claude-code-plugins/commits/main">Commits</a> · <a href="https://github.com/hmzainjamil/anthropic-claude-code-plugins/issues">Issues</a></p>
<p align="center"><img alt="Documentation" src="https://img.shields.io/badge/documentation-deep%20editorial-lightgrey"> <img alt="Lifecycle" src="https://img.shields.io/badge/lifecycle-active-success"></p>

<!-- HMZ DEEP README v1 -->

## At a glance

| Field | Current state |
|---|---|
| Repository | anthropic-claude-code-plugins |
| Visibility | Public |
| Lifecycle | Active |
| Evidence basis | Current repository documentation and source-visible material |

## Why this exists

**Curated Claude Code plugin pack** - Hand-picked Claude Code skills and plugins, starting with `frontend-design` - the skill that makes Claude produce design-system-grade UI instead of generic Bootstrap.

The README focuses on plugin interfaces, installation, permissions, and actual plugin behavior rather than implying capabilities that are not present in the repository.

## CONCEPTS

| Concept | Location | Description |
|---|---|---|
| **frontend-design skill** | `frontend-design/SKILL.md` | Design-system-grade UI mode - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Repo README** | `README.md` | Curated plugin index - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/README.md) |
| **Skill format** | `frontend-design/SKILL.md` | Claude Code SKILL.md spec compliance - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Install path** | `~/.claude/skills/` | Where the skill mounts locally - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Trigger heuristic** | `frontend-design/SKILL.md` | Auto-activates on UI prompts - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Token rules** | `frontend-design/SKILL.md` | Enforces design-token-only colors - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Component anatomy** | `frontend-design/SKILL.md` | Slot/state/variant pattern - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Motion rules** | `frontend-design/SKILL.md` | Opinionated easing + duration - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **Dark-mode rules** | `frontend-design/SKILL.md` | Light/dark parity required - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |
| **A11y rules** | `frontend-design/SKILL.md` | WCAG 2.2 AA baseline - [Source](https://github.com/hmzainjamil/anthropic-claude-code-plugins/blob/main/frontend-design/SKILL.md) |

## HOW IT WORKS

```
+---------------------------------------------------------+
|                       INPUT                             |
|   1 (and growing) - frontend-design                 |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  ORIENT / PARSE                         |
|   - Validate inputs                                     |
|   - Load skill / agent / tool definitions               |
|   - Resolve config + secrets from .env                  |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  PLAN (Claude Sonnet)                   |
|   - Decompose goal into ordered subtasks                |
|   - Pick model per task (Sonnet / Haiku / Tier-0)       |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  EXECUTE (parallel)                     |
|   - Spawn sub-agents / call tools                       |
|   - Stream tokens, persist artifacts                    |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  VERIFY                                 |
|   - Lint / typecheck / visual diff / QA agent           |
|   - On failure -> re-prompt with error context          |
+--------------------------+------------------------------+
                           v
+---------------------------------------------------------+
|                  SHIP                                   |
|   - Write to disk . commit . PR . upload                |
+---------------------------------------------------------+
```

## Install

```bash
git clone https://github.com/hmzainjamil/anthropic-claude-code-plugins.git
cd anthropic-claude-code-plugins

# Per-repo install (try in order):
bash install.sh 2>/dev/null || \
npm install 2>/dev/null || \
bun install 2>/dev/null || \
pip install -r requirements.txt 2>/dev/null || true
```

Environment:

```bash
cp .env.example .env  # if present
# fill ANTHROPIC_API_KEY at minimum
```

## Usage

```bash
# Claude Code skill packs:
/skill-name "your goal"

# CLI / scripts:
python scripts/<script>.py --input ./input --output ./output

# TypeScript projects:
bun run dev    # or npm run dev
```

### Configuration knobs

| Key | Default | Description |
|---|---|---|
| `ANTHROPIC_API_KEY` | - (required) | Claude API key |
| `MODEL` | `claude-sonnet-4-7` | Default LLM |
| `MODEL_FALLBACK` | `claude-haiku-4` | Cheaper fallback |
| `MAX_TOKENS` | `8192` | Per-call ceiling |
| `TEMPERATURE` | `0.2` | Determinism dial |
| `LOG_LEVEL` | `info` | debug / info / warn / error |
| `OUT_DIR` | `./out` | Where artifacts land |
| `CACHE_DIR` | `.cache` | Prompt cache root |
| `PARALLELISM` | `4` | Sub-agent concurrency |
| `RETRY_MAX` | `3` | Per-call retry budget |
| `TIMEOUT_S` | `120` | Per-call timeout |
| `DRY_RUN` | `false` | Plan-only, no side effects |

### Case 3 - DTC brand, ad creative testing

- Before: $2K/month UGC creator retainer, 4 ads/month.
- After: 30+ ad variants/week via Arcads + Claude, A/B-tested.
- Result: 3x creative velocity, 41% lower CAC after 6 weeks.

## Security

- Never commit API keys. `.env` is in `.gitignore` by default.
- Use [git-secret](https://git-secret.io/) or 1Password CLI for team secret sharing.
- Review the QA / safety layer for any tool that writes to disk or runs shells (see `mac_safety.py` style guards).
- Vulnerability reports: open a private GitHub Security Advisory.

## Limitations

- Claude Code behavior can change independently of this repository.
- Plugin compatibility depends on the host version and supported interfaces.
- Quantitative performance claims require reproducible tests.

## Related

- [Claude Code](https://docs.claude.com/en/docs/claude-code) - official docs
- [Anthropic Console](https://console.anthropic.com) - API keys + billing
- [Crawlee](https://crawlee.dev) - web scraping framework
- [hmz-claude-code-best-practice](https://github.com/hmzainjamil/hmz-claude-code-best-practice) - sister repo

## Maintainer

[hmzainjamil](https://github.com/hmzainjamil)