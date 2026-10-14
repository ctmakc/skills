---
name: innova-product-studio
description: Product-first workflow for building or redesigning websites, landing pages, online stores, CRM, SaaS products and mobile apps. Use when a user asks to build a site/app/platform, improve a major screen or user journey, or avoid generic AI-generated design. Adapts to FAST fixes, STANDARD websites and DEEP products, aligning business goals, UX, distinct art direction, engineering and real QA without unnecessary agent bureaucracy.
metadata:
  author: innova
  version: "0.1.0"
---

# INNOVA Product Studio

Deliver a useful, distinctive, working product rather than a generic AI template or a polished mockup. This is a **workflow**, not a visual style or a requirement to spawn multiple agents. Prefer one capable implementer; parallelize independent research, design or engineering only when the expected benefit exceeds coordination overhead.

## Route by scope before doing anything

| Route | Trigger | Required work | Skip |
| --- | --- | --- | --- |
| **FAST** | Bug, copy, small CSS/UI adjustment, tiny existing feature | Inspect relevant code and actual behavior; fix; targeted tests; before/after check | Bizdev workshop, multiple visual directions, PRD |
| **STANDARD** | New landing page, local-business website, store front, material redesign or new UX flow | Business brief, context/research, art-direction alternatives, key-task UX, build, visual/functional QA | Elaborate multi-agent planning unless needed |
| **DEEP** | SaaS, CRM, mobile app, marketplace, AI platform, significant backend or multi-role system | Strategy, journeys and architecture, design system, phased vertical slices, security/data and reliability tests, rollout | Big-bang scaffold with fake modules |

Existing design systems, client decisions, user constraints and relevant repository instructions override stylistic suggestions here. Don't redesign a component for a bug fix. If a previous version or another repo might exist, locate and inspect it **before** creating another.

## Shared guardrails

1. **Evidence before invention.** Read the current code, earlier versions, brief and available assets. Separate verified facts from assumptions and placeholders. Never fabricate clients, credentials, reviews, treatment outcomes, images attributed to real people, prices or working integrations.
2. **Commercial purpose before decoration.** Identify customer, target job, offer, desired behavior (lead, purchase, booking, activation), primary conversion, and a plausible success signal. For internal products, use task completion rather than marketing conversions.
3. **No visual default.** Do not automatically choose oversized serif headlines, italic highlighted words, arch/gravestone portrait masks, sage/beige/purple palettes, generic gradient blobs, three uniform cards, floating badges or excessive empty space. Such elements are allowed **only when justified by the brand and audience**, not forbidden for every client. Avoid decorative clutter disguised as originality.
4. **Respect existing product.** Reuse established design tokens, domain language, accessibility patterns and code conventions where sound. If a redesign is requested, explain what changes and why.
5. **No fake deliverables.** A screenshot is not a site; a static request composer is not a booking backend; dummy dashboard data is not a real integration; a GitHub commit is not a live deployment. State actual status.
6. **User time matters.** Infer reasonable defaults, present concise choices only for consequential uncertainties, and keep moving. Do not ask for a long intake form or schedule calls for straightforward decisions.
7. **Infrastructure.** Prefer the user's own MMIX VPS for production when working on Innova projects. Inspect project deployment conventions, do not quietly switch to Vercel SaaS, and do not publish or overwrite production without the required approvals.

## STANDARD and DEEP pipeline

### 0. Recover context and define the job
Check the target repo, current routes, production site, previous code/branches and reusable assets. Write a **five-line internal brief**: audience; pain/job; offer/value; desired action; constraints + known unknowns. Use actual customer phrases where available. For DEEP, note actors, key data objects, permission boundaries and business model. Avoid lengthy strategy prose unless requested.

### 1. Research and commercial logic (product/bizdev)
Inspect real references and 2–4 competitors/adjacent products **when access and time make this useful**. Capture concrete differentiation and likely conversion or task friction, not trendy styling. Identify mandatory trust elements, content proof, compliance, realistic onboarding/booking/checkout flow. For small sites, keep this to minutes, not hours. If sources aren't available, proceed transparently with assumptions.

### 2. Art direction — before frontend implementation
For new brands or material redesigns, propose **two or three genuinely different directions**, not three palette swaps:
- a name and single-sentence positioning;
- layout/composition and information density;
- typography strategy, color logic, actual image/art strategy;
- distinguishing interaction detail, maintenance/accessibility cost;
- reason it fits the customer and a failure mode.

Use existing brand identity to narrow options when appropriate. Prefer quick above-the-fold **visual treatments or low-fidelity sketches** over building 3 full websites. Compare on *fit, distinctiveness, legibility, conversion and engineering cost*. Select one and record why. If user already supplied a design, implement it rather than redoing this choice. Keep labels internal if the user asked simply to build.

### 3. UX and content architecture
Define the principal visitor journey: entry → understand → trust → action → confirmation. On platforms, define 1–3 complete primary jobs and key states (empty, loading, error, access denied). Make the key content, CTA, navigation and mobile behavior explicit. Real photos, names, licenses and claims must be verified before publishing. Don't let placeholder copy determine final IA.

### 4. UI system and technical shape
Make a small, coherent set of reusable tokens and components **after** selecting art direction. Check contrast, type sizes, touch targets, keyboard flows and responsive breakpoints. Choose the smallest maintainable stack suited to the existing repo; add backend/database/auth only for actual requirements. For DEEP: permission matrix, contracts/schema and threat/data review before implementation.

### 5. Build end-to-end, not as disconnected scenery
Implement a working vertical slice from UI through relevant API/persistence and confirmation state. For bookings, forms, checkout, auth, search or CRM, verify the real server-side path and error behavior; label absent integrations as preview. Use genuine approved assets or visibly neutral placeholders. Avoid early mass generation of hollow pages and dead links.

### 6. Test with evidence and revise
- Run existing tests and check build. Test primary action end-to-end; inspect data writes, notifications, validation and errors when applicable.
- Inspect *actual rendered* desktop and mobile (suggest 1440px and 390px; tablet if distinct). Check overflow, hierarchy, text, images, spacing, touch interaction, keyboard and console; use screenshots or browser verification if available.
- Evaluate against the brief, not just code correctness. Look for default AI aesthetic, invented trust signals, confusing user journeys, broken functional promises and slow/heavy assets.
- Fix the highest-impact defects and recheck. Where execution/browser access is unavailable, be explicit about the unverified item.

### 7. Delivery is an evidence trail
Report concisely: what exists; main user path; what was actually tested; what isn't working yet; repo + commit SHA; deployed URL + observed health **only if verified**. For DEEP: the next vertical slice and its acceptance criteria. Do not say "done" after merely drafting code.

## Autonomous decision rule

Use separate agents only for genuinely independent high-risk questions (e.g. accessibility audit vs engineering implementation, or alternative concepts); merge their **artifacts and conclusions**, not their personas. Do not make art direction a blocking approval ceremony. If the evidence supports one direction, choose it and implement; ask the user only when two materially different business decisions cannot safely be resolved.

## Quality gate and rollback rule

Read [references/evaluation.md](references/evaluation.md) for a compact quality rubric and A/B pilot. Before promoting this workflow globally, compare a baseline build against a workflow-assisted build on at least two representative projects. If task success, usability, design distinctiveness or delivery speed becomes materially worse, simplify or disable the skill instead of blindly adding more stages.

## Compatible supporting skills (optional)

Reuse existing `design-an-interface` for **code/API interfaces**, not art direction; `to-spec`, `implement-spec`, `tdd`, `code-review` for substantial engineering work; and conversion/copywriting skills when the job calls for them. Don't invoke them all by default.
