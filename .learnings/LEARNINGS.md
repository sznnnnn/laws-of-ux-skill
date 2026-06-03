# Learnings

Corrections, insights, best practices, and evidence gaps captured while using this skill.

**Categories**: correction | insight | best_practice | evidence_gap

Use `references/self-iteration-workflow.md` for entry format and promotion rules.

---

## [LRN-20260603-001] best_practice

**Logged**: 2026-06-03T00:17:26Z
**Priority**: medium
**Status**: promoted
**Area**: governance

### Summary
A skill-level self-iteration system should start as explicit behavior plus local logs, not heavy automation.

### Details
For a UX/design skill, the useful minimum loop is: make `SKILL.md` tell agents when to reflect, provide `.learnings/` files for learnings/errors/feature requests, and document a promotion path from repeated logs back into `SKILL.md`, `references/`, `templates/`, or `examples/`.

### Suggested Action
Keep future self-iteration additions small until a pattern repeats in real design work.

### Metadata
- Source: implementation
- Related Files: SKILL.md, references/self-iteration-workflow.md, README.md
- Tags: self-iteration, skill-governance, local-first
- Evidence: Contextual

---

## [LRN-20260603-002] insight

**Logged**: 2026-06-03T01:11:44Z
**Priority**: medium
**Status**: pending
**Area**: interaction

### Summary
Progress feedback should move from "the app is busy" to "the user can judge, wait, pause, cancel, or continue elsewhere."

### Details
- Source: Google UX Design Professional Certificate public Coursera page, accessed 2026-06-03, frames UX work as empathize/define/ideate/prototype/test and includes usability studies, accessibility, and iteration: https://www.coursera.org/professional-certificates/google-ux-design
- Source: Apple Human Interface Guidelines, Progress indicators, accessed 2026-06-03, says determinate indicators are preferable when duration is knowable, progress should remain accurate and moving, descriptions should be concrete, and pause/cancel should appear when interruption is feasible: https://developer.apple.com/design/human-interface-guidelines/progress-indicators
- Source: Apple Human Interface Guidelines, Loading, change log includes June 9, 2025 guidance revision for storing downloads and large background assets: https://developer.apple.com/design/human-interface-guidelines/loading
- Case: Apple's Mail refresh control pattern keeps the refresh affordance near the content being updated and can show value-adding context like last update time; this is better than forcing users to initiate every refresh manually.
- Pattern: Use a stable progress location plus a determinate bar/ring once scope is knowable; pair long operations with concise task-specific copy and Pause/Cancel when safe.
- Counterexample: A spinner that sits still, switches shape mid-task, or says only "Loading..." gives no estimate and can feel stalled or deceptive, especially if the final percent takes much longer than the early percent.
- What changed in product judgment: In UX reviews, loading states should be judged as decision-supporting controls, not just visual reassurance.
- Where this skill should apply it: imports, file conversion, AI generation, onboarding setup, search/indexing, background sync, and any flow where waiting blocks the next user decision.

### Suggested Action
Keep as a daily research note; promote into the acceptance checklist if future reviews repeat weak loading/progress states.

### Metadata
- Source: research
- Related Files: references/self-iteration-workflow.md, references/research-sources.md
- Tags: daily-intake, ux-research, progress-feedback, apple-hig, google-ux
- Evidence: Validated

---
