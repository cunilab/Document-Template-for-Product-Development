---
id: <REPO>-EVID-NNN
title: "Validation and Evidence — <Scope>"
status: draft
---

# Validation and Evidence — <Scope, e.g. Phase 2 / v0.3>

<One sentence: what must be demonstrated before this scope claims a behavior works.>

<!--
Owns pass/fail claims and their recorded results. The product document owns the
required outcome; this document owns the proof. Status describes the text; the
Evidence section below is the only place a feature may be claimed to work.
One document per phase or release keeps results reviewable — copy this file
instead of overwriting old results.
-->

## Checks

| # | Check | How to verify | Result |
| --- | --- | --- | --- |
| <C-1> | <Observable pass/fail statement> | <Command / manual step / CI lane> | ⏳ pending |
| <C-2> | <Observable pass/fail statement> | <Command / manual step / CI lane> | ⏳ pending |

<!-- Result vocabulary: ✅ pass, ❌ fail, ⏳ pending, ⏭️ not run (with a reason). -->

## Evidence

<!-- Recorded results with enough detail to re-verify. Link CI runs, logs, screenshots.
Record the source identity (commit/tag), platform, exact command, and outcome. -->

### <Check ID or date>

- **Result:** ✅ / ❌ / ⏭️
- **How verified:** <command, CI run, manual steps>
- **Observed:** <what was actually seen, not what was expected>
- **Artifact:** <link to CI run, log, screenshot>

## Deferrals and limits

<!-- Checks deliberately postponed or out of scope. Each needs a reason and tracking.
Unrun checks and unmeasured capacity remain explicit limitations. -->

| Check | Reason | Tracking |
| --- | --- | --- |
| <C-n> | <why it was deferred> | <issue / milestone> |

## Open questions

- <What still blocks a complete pass>
