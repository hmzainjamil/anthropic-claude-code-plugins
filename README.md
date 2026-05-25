# anthropic-claude-code-plugins

> **Anthropic Claude Code plugins — official plugin collection for extending Claude Code**

![Status](https://img.shields.io/badge/status-active-brightgreen?style=flat)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat)
![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-FF6B35?style=flat)
![Stars](https://img.shields.io/github/stars/hmzainjamil/anthropic-claude-code-plugins?style=flat)
![Last Commit](https://img.shields.io/github/last-commit/hmzainjamil/anthropic-claude-code-plugins?style=flat)

---

## CONCEPTS

| Concept | Description |
|---|---|
| **Plugin** | Extends Claude Code with new capabilities |
| **MCP** | Model Context Protocol integration layer |
| **Tool** | Function callable by Claude during tasks |
| **Resource** | Data source accessible to Claude |
| **Prompt** | Pre-built prompt templates |
| **Auth** | Secure credential management |
| **Registry** | Discover plugins via central index |
| **Versioning** | Semantic versioning for stability |

---

## 🔥 Hot Commands

```bash
# Activate skill
claude --skill anthropic-claude-code-plugins 'your task'

# Quick workflow
claude 'anthropic automation task'

# Get capabilities
claude 'what can anthropic-claude-code-plugins do?'
```

## ■ tip
> Mention **anthropic** or **plugins** in your prompt to auto-activate this skill.

---

## ☠️ STARTUPS / BUSINESSES

- **Agencies**: automate anthropic workflows for clients at scale
- **Founders**: ship plugins features 10x faster
- **Freelancers**: deliver official work with AI precision

---

## Features

- Anthropic automation
- Plugins automation
- Official automation
- Claude automation
- Code automation
- Extensions automation

---

## Installation

```bash
git clone https://github.com/hmzainjamil/anthropic-claude-code-plugins.git
cd anthropic-claude-code-plugins
```

---

## Usage

```bash
# Activate skill in Claude Code
claude --skill anthropic-claude-code-plugins "your task here"

# Quick workflow
claude "anthropic automation task"

# Get help
claude "what can anthropic-claude-code-plugins do?"
```

---

## Configuration

| Variable | Description | Default |
|---|---|---|
| `API_KEY` | Primary API key | Required |
| `MODEL` | AI model to use | claude-3-5-sonnet |
| `DEBUG` | Enable verbose debug | false |
| `MAX_TOKENS` | Max token budget | 8192 |
| `TIMEOUT` | Request timeout (sec) | 30 |
| `LOG_LEVEL` | Logging verbosity | info |

---

## Architecture

```
anthropic-claude-code-plugins/
├── README.md           # Documentation
├── SKILL.md            # Claude Code skill definition
├── scripts/            # Automation scripts
├── templates/          # Output templates
├── examples/           # Usage examples
└── docs/               # Extended documentation
```

---

## Examples

### Basic

```bash
# Simple task
claude --skill anthropic-claude-code-plugins "anthropic task"

# Verbose
claude --skill anthropic-claude-code-plugins --verbose "detailed plugins task"
```

### Advanced Pipeline

```bash
# Chain skills
claude --skill anthropic-claude-code-plugins "step 1" | claude --skill summarize

# Batch run
for item in $(cat list.txt); do
  claude --skill anthropic-claude-code-plugins "process $item"
done
```

---

## Troubleshooting

| Issue | Cause | Fix |
|---|---|---|
| Auth fails | Invalid API key | Re-export key in shell profile |
| Timeout | Network or large payload | Increase TIMEOUT value |
| Empty output | Prompt too vague | Add more context |
| Rate limit | Too many requests | Add delay between calls |
| Model error | Unsupported version | Update MODEL variable |
| Import error | Missing dependency | Run pip install -r requirements.txt |

---

## Comparison

| Feature | This Skill | Alt A | Alt B |
|---|---|---|---|
| Claude Code native | ✅ | ❌ | ✅ |
| Auto-activation | ✅ | ✅ | ❌ |
| Free to use | ✅ | ❌ | ✅ |
| Production ready | ✅ | ✅ | ❌ |
| Active maintenance | ✅ | ❌ | ❌ |

---

## Changelog

| Version | Changes |
|---|---|
| v2.0 | Claude 4 support, auto-activation |
| v1.5 | Added keyword triggers |
| v1.0 | Initial release |

---

## Contributing

1. Fork → feature branch → commit → PR
2. Follow conventional commits: `feat:`, `fix:`, `docs:`
3. Add tests for new features

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=hmzainjamil/anthropic-claude-code-plugins&type=Date)](https://star-history.com/#hmzainjamil/anthropic-claude-code-plugins&Date)

---

## 📜 License

MIT — free to use, modify, distribute.

---

Made with ❤️ by [@hmzainjamil](https://github.com/hmzainjamil)
