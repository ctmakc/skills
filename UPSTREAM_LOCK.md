# Pinned upstream import

- **Author:** Matt Pocock
- **Origin:** https://github.com/mattpocock/skills
- **Release:** `v1.3.1` (2026-10-04)
- **Tag target commit:** `24fe0ef7737efae15c87225755e9f6f5965e4888`
- **Original license:** MIT, copyright Matt Pocock; see `LICENSE`
- **Import strategy:** Copy source files verbatim at the upstream tag into skill directories in this fork. Legacy directories not on this list are preserved.

| Fork path | Upstream source |
| --- | --- |
| `retro/` | `skills/engineering/retro/` |
| `pr/` | `skills/engineering/pr/` |
| `implement-spec/` | `skills/engineering/implement-spec/` |
| `code-review/` | `skills/engineering/code-review/` |
| `to-spec/` | `skills/engineering/to-spec/` |
| `to-tickets/` | `skills/engineering/to-tickets/` |
| `setup-matt-pocock-skills/` | `skills/engineering/setup-matt-pocock-skills/` |
| `tdd/` | `skills/engineering/tdd/` |
| `writing-for-agents/` | `skills/productivity/writing-for-agents/` |

Imported `SKILL.md`, adjacent reference material and `agents/openai.yaml` descriptors where available. Recheck upstream license, diffs, dependencies and security posture before a future update. Avoid silent skill updates on production hosts; test in a separate agent/session first.

`GLOSSARY.md` is the new upstream domain-doc standard replacing `CONTEXT.md`. Project-specific renames must be performed by reviewing actual contents, not by deleting files.

This pinned import has not yet been installed in a running host environment; see installation instructions in README.
