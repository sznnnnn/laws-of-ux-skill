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
**Status**: promoted
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
Promoted into `SKILL.md`, `references/review-rubric.md`, `references/design-governance-workflow.md`, and `references/agentic-long-task-ux.md` as long-task progress and recovery checks.

### Metadata
- Source: research
- Related Files: references/self-iteration-workflow.md, references/research-sources.md
- Tags: daily-intake, ux-research, progress-feedback, apple-hig, google-ux
- Evidence: Validated

---

## [LRN-20260610-001] insight

**Logged**: 2026-06-10T12:22:58Z
**Priority**: high
**Status**: promoted
**Area**: interaction

### Summary
Agentic and long-running interfaces should pause at meaningful choice points, not only report that work is happening.

### Details
- Source: Google UX Design Professional Certificate public Coursera page, accessed 2026-06-10, frames UX as empathize, define, ideate, prototype, test, and iteration around user pain points: https://www.coursera.org/professional-certificates/google-ux-design
- Source: W3C WCAG 2.2 Understanding SC 4.1.3 Status Messages, accessed 2026-06-10, requires important non-focus status changes to be programmatically determinable without unnecessarily interrupting work: https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html
- Source: Nielsen Norman Group, Response Times: The 3 Important Limits, accessed 2026-06-10, recommends feedback and interruptibility for operations that exceed attention limits: https://www.nngroup.com/articles/response-times-3-important-limits/
- Source: Morae: Proactively Pausing UI Agents for User Choices, ACM UIST 2025 / arXiv, accessed 2026-06-10, shows a mixed-initiative UI agent pausing during real web tasks so blind and low-vision users can choose among meaningful alternatives: https://arxiv.org/abs/2508.21456
- Case: In Morae's shopping example, an agent asked to buy the cheapest sparkling water picked one automatically, missing user-relevant alternatives such as flavor and rating; the improved pattern pauses when options are materially equivalent or preference-sensitive.
- Pattern: For AI agents, imports, checkout, search, matching, or setup flows, classify status moments into "inform only" versus "needs user choice"; use accessible status messages for the former and explicit pause/resume choice surfaces for the latter.
- Counterexample: Treating every intermediate uncertainty as either silent automation or a blocking modal can both fail: silent automation reduces agency, while excessive confirmation destroys flow.
- What changed in product judgment: UX reviews should evaluate automation by decision rights, not just task completion speed.
- Where this skill should apply it: agent-memory tools, browser extensions, AI generation, recommendation/matching flows, checkout substitutions, and any interface that acts on behalf of users.

### Suggested Action
Promoted into `SKILL.md`, `references/review-rubric.md`, `references/design-governance-workflow.md`, and `references/agentic-long-task-ux.md` as a decision-rights model for agentic flows.

### Metadata
- Source: research
- Related Files: references/self-iteration-workflow.md, references/research-sources.md
- Tags: daily-intake, ux-research, agentic-ux, accessibility, status-messages, user-agency
- Evidence: Contextual

---

## [LRN-20260614-001] insight

**Logged**: 2026-06-14T01:54:48Z
**Priority**: medium
**Status**: pending
**Area**: interaction

### Summary
Progressive disclosure should preserve orientation and decision context, not merely hide complexity.

### Details
- Source: Apple Design private Notion source was treated as an inaccessible theme; Apple HIG Disclosure Controls, accessed 2026-06-14, frames disclosure controls as reveal/hide mechanisms for related information or functionality: https://developer.apple.com/design/human-interface-guidelines/disclosure-controls
- Source: Google UX Design Certificate public Google page, accessed 2026-06-14, emphasizes user-centered foundations, wireframes/prototypes, usability studies, and test-and-iterate practice: https://grow.google/certificates/ux-design/
- Source: NN/g, Few Guesses, More Success: 4 Principles to Reduce Cognitive Load in Forms, accessed 2026-06-14, recommends showing only what is relevant at the current step while making requirements and progress transparent: https://www.nngroup.com/articles/4-principles-reduce-cognitive-load/
- Case: Shopify Polaris IA uses "one home and many doors" for Help Center content: shipping help lives in one canonical place, but contextual links from admin settings give merchants access when the extra context becomes relevant: https://polaris-react.shopify.com/foundations/information-architecture
- Pattern: Keep the primary path visible, reveal secondary details near the object they explain, use descriptive icon+text triggers, and maintain breadcrumbs/progress/context so the user knows where the hidden detail fits.
- Counterexample: GitHub Primer cautions that disclosure should be used sparingly and should not disorient the user's initial focus; GitLab Pajamas warns that three or more nested disclosure levels can signal that the feature itself is too complex: https://primer.style/product/ui-patterns/progressive-disclosure/ and https://design.gitlab.com/patterns/progressive-disclosure/
- What changed in product judgment: In reviews, collapses, accordions, "more" menus, and step flows should be judged by orientation and recoverability, not by screen cleanliness alone.
- Where this skill should apply it: long forms, settings, filters, dashboards, onboarding, help links, AI/agent setup, and dense product-admin workflows.

### Suggested Action
Keep as a daily research note; promote if future reviews repeatedly find hidden controls, nested accordions, or "clean" screens that lose user context.

### Metadata
- Source: research
- Related Files: references/self-iteration-workflow.md, references/research-sources.md
- Tags: daily-intake, ux-research, progressive-disclosure, information-architecture, apple-hig, google-ux
- Evidence: Validated

---

## [LRN-20260616-001] insight

**Logged**: 2026-06-16T01:38:15Z
**Priority**: medium
**Status**: pending
**Area**: accessibility

### Summary
Tap-target quality is about the whole activation area and spacing, not the visible icon size.

### Details
- Source: Google UX Design Professional Certificate private Notion source was treated as an inaccessible theme; the public Coursera page, accessed 2026-06-16, frames UX foundations around user-centered design, accessibility, equity-focused design, research, prototyping, and usability testing: https://www.coursera.org/professional-certificates/google-ux-design
- Source: Apple Design private Notion source was treated as an inaccessible theme; Apple HIG Buttons, accessed 2026-06-16, recommends a hit region of at least 44x44 pt for buttons: https://developer.apple.com/design/human-interface-guidelines/buttons
- Source: W3C WCAG 2.2 Understanding SC 2.5.8 Target Size (Minimum), accessed 2026-06-16, sets a 24x24 CSS pixel AA floor or sufficient spacing for pointer targets: https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html
- Source: Material Design 3 Touch Targets, accessed 2026-06-16, recommends touch targets of at least 48x48dp for most platforms: https://m3.material.io/foundations/designing/structure
- Case: Baymard's promoted-filter research shows mobile product-list filters can reduce trips into a separate filter panel, but only if chips and remove/apply controls remain easy to hit and are still available in their normal filter location: https://baymard.com/blog/promoting-product-filters
- Pattern: In dense mobile toolbars, filter chips, card actions, and inline icon buttons, inspect the tappable box and neighbor spacing separately from the visual glyph; allow invisible padding when visual density matters.
- Counterexample: A row of tiny close icons on selected filters can look clean but makes accidental filter removal likely, especially one-handed or on moving transport.
- What changed in product judgment: In reviews, Fitts's Law should be checked as a measurable target/spacing issue before praising compact visual hierarchy.
- Where this skill should apply it: mobile filters, chip rows, icon-only buttons, carousels, table row actions, quick actions, and any control cluster near screen edges.

### Suggested Action
Keep as a daily research note; promote into the acceptance checklist if future reviews repeat small icon-only controls or crowded chip rows.

### Metadata
- Source: research
- Related Files: references/self-iteration-workflow.md, references/research-sources.md
- Tags: daily-intake, ux-research, accessibility, target-size, fitts-law, mobile-filters
- Evidence: Validated

---
