# Anthropic Claude Code Plugins

This repository currently contains one Claude Code skill: `frontend-design`. The skill is a Markdown guide for creating frontend interfaces. There is no plugin manifest, installer, runtime package, or application code in the current repository tree.

## Included

- [Frontend design skill](frontend-design/SKILL.md): design direction and implementation guidance for requested web interfaces.

The skill describes design practices. It does not itself provide a framework, component library, automated accessibility validation, or guaranteed production readiness. Review generated code and run project-specific checks before shipping.

## Use

Clone the repository, then provide the skill file to the Claude Code environment you use, following that environment's current skill installation and discovery instructions:

```bash
git clone https://github.com/hmzainjamil/anthropic-claude-code-plugins.git
cd anthropic-claude-code-plugins
```

No install command is included in this repository. Do not assume that placing the folder under a particular path will activate the skill; follow the current host documentation.

## Scope and limits

- The repository contains a single skill file and this README.
- The skill is instruction text, not executable plugin code.
- The skill header references `LICENSE.txt`, but that file is not present in the current tree. The repository root includes [LICENSE](LICENSE); confirm redistribution terms before repackaging the skill.
- No tests, build process, or supported host-version matrix are included.

## Contributing

Open an issue with the affected file, expected behavior, and a reproducible example. Avoid including credentials or private project data.

## License

See [LICENSE](LICENSE). The skill metadata points to a missing `LICENSE.txt`; resolve that reference before redistributing the skill.
