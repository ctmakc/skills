# ChatGPT web-chat execution profile — INNOVA Product Studio

This profile is intended for the **ordinary ChatGPT web conversation**, not ChatGPT Work, Claude Code, Codex CLI, a local IDE, or an autonomous background agent. It is the default delivery profile **when the user is talking here**.

## Tool reality check at the start of each task

Discover current tools; availability can differ by session, connector, permission and repository. Do not assume any operation is possible because it worked in another mode. For today's connected session, the relevant tool families include:

| Need | In Chat, use when available | Must not assume |
| --- | --- | --- |
| Recover project, read/update source | Connected GitHub actions: get repo, fetch_file, create/update_file, commit/tree, PR | An automatically cloned checkout or writable local repo |
| Find old materials | Files (current/Library), personal context, Gmail/Drive/search, GitHub history | Full access to every prior chat, private account or offline workspace |
| Business and competitor evidence | Web search and grounded user-provided/connected resources | That a source is factual, public imagery belongs to client, or reviews can be fabricated |
| Product research/art direction | Reason here; compare 2-3 distinct rationales in short text, optionally verified references | Multiple parallel agent instances; visual concepts must be images by default |
| Actual files/code | Chat-connected working container/Python if available; inspect/test generated files; deliver archive via verified sandbox path | That file creation automatically pushes to GitHub |
| Browser/visual QA | Use available browser connector, actual screenshots, browser tooling in working container where supported | Always-on Playwright, screenshot access to every site, background browser |
| Production deployment | User's connected MMIX VPS/INNOVA deployment actions, only for existing supported sites/operations | Cloud terminal/SSH, site provisioning if no action exists, successful auto-deploy solely from commit |
| Long task | Continue within this chat through sequential tool calls and progress reports | Unattended asynchronous work unless user set an automation (and an automation is not a dev runner) |

A tool existing in a different agent or a README **does not make it available here**. Query connector/tool capabilities before making plans. If user says "continue", use existing repo/project state and perform the next available action; do not make up the last state.

## Specific operating sequence in normal Chat

1. **Scope in one sentence.** FAST, STANDARD or DEEP. Use existing user context and repo inspection first.
2. **Write/keep a minimal decision record** within this chat and/or the repo. Business goal, user, task, evidence vs assumptions, key acceptance criterion. No mandatory PRD form.
3. **For STANDARD/DEEP new designs:** internally compare 2-3 materially distinct art directions before coding. Show alternatives when choice materially affects identity; otherwise choose one based on audience and user constraints. Do not require separate agent processes.
4. **Implementation in actual available tools:** use GitHub connector to read and edit the user's repo, or create locally in the chat container and deliver verifiable artifacts. Prefer small, reviewable commits. For projects already deployed, use the connected MMIX site/deploy tools after verifying site repo/branch. When connectors block an operation, record the exact blocker and offer the viable route; do not claim "done".
5. **QA with evidence:** validate generated files (syntax/build/tests) and render at mobile/desktop if a browser is actually available. If browser checks cannot run, record "not verified", don't fabricate test results, screenshots or metrics. For forms, prove a real recipient/persistence and confirmation before calling them live.
6. **Final delivery:** distinguish (a) planned, (b) file generated, (c) committed to GitHub, (d) deployed, (e) tested live. Give verified links and commit SHA. Keep responses compact.

For platform-heavy builds, implement one complete vertical slice, not an imaginary all-at-once build. If read/write permissions do not permit a repo operation, preserve source in verified artifacts and say which step remains uncommitted.

## ChatGPT limitations that affect skill installation

- Files in `ctmakc/skills`, `.agents/skills` and `.claude/skills` are **available to agents only if those agents are configured to read them**. Ordinary ChatGPT web-chat does **not** automatically load GitHub `AGENTS.md`, `SKILL.md` or user repo documentation.
- ChatGPT's currently available `skills.list` / `skills.read` expose only skills installed in the active session. A GitHub commit is not installation. If `innova-product-studio` is absent there, fetch the canonical content through GitHub at task time when the conversation asks for this workflow.
- The user can make cross-chat routing more likely by putting a short pointer in ChatGPT Custom Instructions / personalization (not modified through the GitHub connector):
  "For new INNOVA websites, redesigns, stores or apps, first load ctmakc/skills/innova-product-studio/SKILL.md and references/chatgpt-web-chat.md from connected GitHub when accessible; use FAST/STANDARD/DEEP as appropriate. Work with tools actually available in ChatGPT web chat, not imaginary CLI agents. Confirm GitHub commits, live deployments and tests separately."
- Even that pointer cannot grant tool access, guarantee auto-fetch in every chat, or circumvent connector permissions. In the **current conversation**, follow the profile immediately without user setup.

## Pilot-only constraints

- Do not mass-install into client repos or change global infrastructure just to enable instructions.
- Update `ctmakc/mashamassage` pilot copies for Codex/Claude, but recognize those copies alone do not activate ChatGPT web-chat.
- A/B evaluation must run in the same chat/tool environment. Do not compare imaginary browser results with a real screenshot.
- Treat the earlier false-positive source transfer as a regression example: README committed != HTML/CSS source committed != site deployed. Verify each separately.
