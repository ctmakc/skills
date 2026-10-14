# INNOVA Product Studio — evaluation and promotion protocol

## Principle
A longer workflow does not prove a better product. Evaluate rendered outcomes and real task completion; don't reward extra planning documents, more agents or prettier descriptions.

## Benchmark projects (run before global installation)
1. **Small service website** — Masha Massage: visitor can understand the offer, trust the practitioner based on verified proof, and submit a real appointment request. Compare current v0.1 mockup to a redesign with the workflow; use the same verified inputs in both. No fabricated credentials, quotes, prices, photos or bookings.
2. **Product/platform** — Real Friend or Food IQ: compare one bounded high-value user task (e.g. first-time user starts a relevant recommendation and saves a result) on an existing baseline vs a workflow-assisted slice. Do not rebuild the whole platform to benchmark.
3. **FAST regression** — one simple UI defect: compare fix quality and elapsed work. Ensure the skill did NOT produce a redundant strategy workshop, rebrand or multi-agent process.

## Blind comparison
- Save a baseline screenshot at 390px and 1440px plus a short recording/notes of the actual task before the workflow build.
- Give both versions the **same** brief, verified assets and functional acceptance test. Keep labels hidden from reviewers if practical.
- Run a mobile and desktop task, using a specific success criterion rather than asking "which is prettier?".
- Mark every untested area as NOT VERIFIED, not PASS.
- Prefer real clients or users when possible; otherwise use at least one independent reviewer and a self-review that identifies uncertainty.

## Scorecard (100 points total)

| Criterion | Weight | What earns a high score |
| --- | ---: | --- |
| User task + conversion clarity | 25 | One clear user goal, smooth path, useful CTA, proper confirmations |
| Distinct, fitting visual identity | 25 | Recognizably tied to the client; strong hierarchy; not a generic AI template |
| Accuracy and real trust | 15 | Evidence-backed claims, approved authentic content, no fake social proof |
| Engineering functionality | 20 | Main path really works end-to-end; errors, empty states, security considered |
| Usability, accessibility, speed | 10 | Mobile layout, contrast, tap/keyboard, sensible assets and loading |
| Delivery efficiency | 5 | Additional work/time is justified by result; no pointless ceremony |

Use values 0..weight and list supporting evidence. **Gate:** never call a concept "better" from visual judgment alone if primary task is broken.

## Release gates
- **Hard blockers:** fabricated claims/reviews/photos attributed to a client, broken booking/checkout/auth presented as working, severe regressions, failed data isolation, unverified production status.
- **Pilot PASS:** hard blockers absent, task path no worse than baseline, visual fit/distinctiveness better in at least one case, and no material FAST slowdown.
- **Pilot FAIL:** more bureaucracy without outcome lift, reduced task success, loss of client identity, or notable increase in bugs. In that case disable rollout, keep the good rules, remove complexity and retest.
- No rollout or universal AGENTS.md changes until two representative STANDARD/DEEP comparisons **and** FAST regression are reviewed.

## Record
For each test capture: date, project, route, brief, baseline URL/commit, candidate URL/commit, screenshots, test steps and outcome, approximate effort, criterion scores, hard blockers, reviewer preference, decision (keep/tune/drop). Never fabricate measurements.

## Example prompt for a test (Masha)
"Given the existing verified content and current source, redesign the hero, service presentation and request flow for a local massage practitioner. Produce two materially different visual directions, select the stronger fit, implement one responsive treatment without inventing business facts, and test both phone and desktop. Compare with the baseline screenshot and record what really works."

## Not tested yet
The skill's presence in GitHub and conformance to the file format are **not** evidence of product quality. Real A/B task outcomes require an agent session and browser access to the selected repositories.
