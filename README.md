# Agent Skills

A collection of agent skills that extend capabilities across planning, development, and tooling.

## Planning & Design

These skills help you think through problems before writing code.

- **write-a-prd** — Create a PRD through an interactive interview, codebase exploration, and module design. Filed as a GitHub issue.

  ```
  npx skills@latest add mattpocock/skills/write-a-prd
  ```

- **prd-to-plan** — Turn a PRD into a multi-phase implementation plan using tracer-bullet vertical slices.

  ```
  npx skills@latest add mattpocock/skills/prd-to-plan
  ```

- **prd-to-issues** — Break a PRD into independently-grabbable GitHub issues using vertical slices.

  ```
  npx skills@latest add mattpocock/skills/prd-to-issues
  ```

- **grill-me** — Get relentlessly interviewed about a plan or design until every branch of the decision tree is resolved.

  ```
  npx skills@latest add mattpocock/skills/grill-me
  ```

- **design-an-interface** — Generate multiple radically different interface designs for a module using parallel sub-agents.

  ```
  npx skills@latest add mattpocock/skills/design-an-interface
  ```

- **request-refactor-plan** — Create a detailed refactor plan with tiny commits via user interview, then file it as a GitHub issue.

  ```
  npx skills@latest add mattpocock/skills/request-refactor-plan
  ```

## Development

These skills help you write, refactor, and fix code.

- **tdd** — Test-driven development with a red-green-refactor loop. Builds features or fixes bugs one vertical slice at a time.

  ```
  npx skills@latest add mattpocock/skills/tdd
  ```

- **triage-issue** — Investigate a bug by exploring the codebase, identify the root cause, and file a GitHub issue with a TDD-based fix plan.

  ```
  npx skills@latest add mattpocock/skills/triage-issue
  ```

- **improve-codebase-architecture** — Explore a codebase for architectural improvement opportunities, focusing on deepening shallow modules and improving testability.

  ```
  npx skills@latest add mattpocock/skills/improve-codebase-architecture
  ```

- **migrate-to-shoehorn** — Migrate test files from `as` type assertions to @total-typescript/shoehorn.

  ```
  npx skills@latest add mattpocock/skills/migrate-to-shoehorn
  ```

- **scaffold-exercises** — Create exercise directory structures with sections, problems, solutions, and explainers.

  ```
  npx skills@latest add mattpocock/skills/scaffold-exercises
  ```

## Tooling & Setup

- **setup-pre-commit** — Set up Husky pre-commit hooks with lint-staged, Prettier, type checking, and tests.

  ```
  npx skills@latest add mattpocock/skills/setup-pre-commit
  ```

- **git-guardrails-claude-code** — Set up Claude Code hooks to block dangerous git commands (push, reset --hard, clean, etc.) before they execute.

  ```
  npx skills@latest add mattpocock/skills/git-guardrails-claude-code
  ```

## Writing & Knowledge

- **write-a-skill** — Create new skills with proper structure, progressive disclosure, and bundled resources.

  ```
  npx skills@latest add mattpocock/skills/write-a-skill
  ```

- **edit-article** — Edit and improve articles by restructuring sections, improving clarity, and tightening prose.

  ```
  npx skills@latest add mattpocock/skills/edit-article
  ```

- **ubiquitous-language** — Extract a DDD-style ubiquitous language glossary from the current conversation.

  ```
  npx skills@latest add mattpocock/skills/ubiquitous-language
  ```

- **obsidian-vault** — Search, create, and manage notes in an Obsidian vault with wikilinks and index notes.

  ```
  npx skills@latest add mattpocock/skills/obsidian-vault
  ```

## Engineering skills v1.3.1 (October 2026)

Updated from Matt Pocock's upstream [v1.3.1](https://github.com/mattpocock/skills/releases/tag/v1.3.1), pinned to source commit `24fe0ef7737efae15c87225755e9f6f5965e4888`. The original MIT license and credit remain in `LICENSE`. Earlier skills have **not** been deleted; the existing `tdd` has been refreshed to match v1.3.1.

New or refreshed skill entrypoints (actual vendored `SKILL.md` files, not just setup notes):
- `retro` — review session traces and propose environment / guardrail improvements for human approval.
- `pr` — evidence-backed PR descriptions and merge risk.
- `implement-spec` — dependency-aware ticket execution using isolated worktrees.
- `code-review`, `to-spec`, `to-tickets`, `setup-matt-pocock-skills`, `writing-for-agents`, `tdd` — dependencies for the end-to-end loop.

Quick install **from our repository** using the open skills installer (choose a coding-agent target as prompted):

```sh
npx skills add ctmakc/skills --skill retro
npx skills add ctmakc/skills --skill pr
npx skills add ctmakc/skills --skill implement-spec
npx skills add ctmakc/skills --skill code-review
npx skills add ctmakc/skills --skill to-spec
npx skills add ctmakc/skills --skill to-tickets
npx skills add ctmakc/skills --skill tdd
npx skills add ctmakc/skills --skill writing-for-agents
npx skills add ctmakc/skills --skill setup-matt-pocock-skills
```

**Choose one source per coding agent:** either this editable and pinned fork **or** the official auto-updating plugin. Installing both causes duplicate skill registrations. This is only a source repository: updating it does not automatically alter any running Codex/Claude instance or VPS environment.

Read `UPSTREAM_LOCK.md` for the file mapping and upgrade policy.
