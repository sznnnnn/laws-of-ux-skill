# UX Review Rubric

Use this rubric when reviewing a UI, product flow, Figma design, frontend implementation, or prototype.

## Review Output

```markdown
**Verdict**
- Score: X/10
- Release risk: low / medium / high
- Main UX issue: one sentence.

**Keep**
- Do not break these working patterns.

**Findings**
- [P0/P1/P2/P3] Issue: impact. Recommendation.

**Quick Wins**
- [ ] Highest leverage small fix.
- [ ] Second fix.
- [ ] Third fix.

**Applied Laws**
- Law: why it matters here.

**Acceptance Checks**
- Concrete condition to verify.

**Evidence Tags**
- Recommendation -> Validated / Contextual / Experimental

**Metrics**
- Primary metric(s):
- Guardrail metric(s):

**Visual Evidence**
- Screenshot, diagram, funnel, or flow reference if available.
```

## Severity

- P0: Blocks task completion, causes serious data loss, or creates a high-risk action with no recovery.
- P1: Causes major confusion, high abandonment risk, or repeated errors in a core flow.
- P2: Adds noticeable friction, cognitive load, or inconsistency but has a workaround.
- P3: Polish, clarity, consistency, or edge-case improvement.

## Score Guide

Use scoring only when it helps compare options or communicate release risk.

- 9-10: Clear task path, strong hierarchy, low error risk, polished states, and measurable confidence.
- 7-8: Usable and mostly clear, with a few fixable friction points.
- 5-6: Understandable but effortful; users must pause, compare, remember, or recover too often.
- 3-4: Core flow is unreliable or confusing for many users.
- 1-2: Users are likely blocked, misled, or exposed to serious unrecoverable errors.

Score dimensions:

- Task clarity: can users tell what this screen is for and what to do next?
- Decision load: are choices grouped, sequenced, defaulted, or explained?
- Action ergonomics: are primary actions reachable, stateful, and recoverable?
- Feedback quality: does the interface respond clearly before, during, and after action?
- Fit to expectations: does the design match familiar domain and platform patterns?
- Craft and responsiveness: does layout survive realistic desktop/mobile sizes?

## Keep / Fix / Quick Wins

- `Keep`: name the patterns that already reduce effort or build trust. This prevents redesigns from destroying useful existing behavior.
- `Fix`: list material problems sorted by P0-P3 severity, with user impact and implementation direction.
- `Quick Wins`: choose small, shippable changes with high leverage; avoid vague items like "improve visual hierarchy."

## Review Passes

### First-Use Clarity

- Can a new user identify the page purpose within a few seconds?
- Is the primary action obvious?
- Are familiar patterns used where users expect them?
- Are terms user-facing rather than implementation-facing?

Relevant laws: Jakob's Law, Mental Model, Hick's Law, Cognitive Load.

### Visual Grouping

- Are related items closer to each other than unrelated items?
- Are groups visually clear without extra labels?
- Does responsive layout preserve relationships?
- Are same-level actions styled consistently?

Relevant laws: Proximity, Common Region, Similarity, Uniform Connectedness, Prägnanz.

### Action Ergonomics

- Are frequent and primary controls easy to reach and large enough?
- Are destructive or high-cost actions separated from routine actions?
- Are disabled, loading, error, and success states clear?
- Does every action have feedback?

Relevant laws: Fitts's Law, Doherty Threshold, Postel's Law, Peak-End Rule.

### Decision Load

- Are users asked to choose from too many options at once?
- Are defaults, recommendations, filters, or grouping used to reduce comparison effort?
- Is advanced complexity deferred until needed?
- Does the interface preserve control while reducing effort?

Relevant laws: Hick's Law, Choice Overload, Miller's Law, Tesler's Law, Occam's Razor.

### Memory And Momentum

- Does the user need to remember information from another screen?
- Are progress, drafts, next steps, and completion states visible?
- Does the flow protect partially completed work?
- Does the ending leave the user confident about what happened?

Relevant laws: Working Memory, Zeigarnik Effect, Goal-Gradient Effect, Peak-End Rule.

### Innovation Cost

- Which convention is being changed?
- What benefit does the new pattern create after learning?
- How often will users repeat the task?
- Is there onboarding, gradual rollout, opt-out, or rollback?

Relevant laws: Jakob's Law, Learning Curve, Cognitive Load, Paradox of the Active User.

## Product Spec Pass (BuddyUp / v0-ai)

When reviewing this product, also verify against `references/buddyup-product-design-spec.md`:

- Tokens and semantic colors come from `app/globals.css` (no stray hex).
- Primary flow vocabulary is consistent: 问卷 → 匹配 → 工作台 → 文书.
- List rows use `interactive-hover` / `interactive-active`; one primary CTA per screen.
- ⌘K / ⌘B shortcuts respect input focus and `data-skip-workspace-cmdk`.
- Irreversible actions use `AlertDialog`; empty states include a next action.
- Icon-only controls have `aria-label`; clickable cards support Enter/Space.
- Guest/local storage is perceptible when data is not cloud-synced.
- New onboarding uses `data-tour` + centralized storage keys.

Run `references/design-governance-workflow.md` for full five-domain audit and PR self-check.

### Visual Evidence

- Is there a screenshot or prototype state for the issue?
- Can the finding be shown as before/after, flow, funnel, or annotated region?
- Does the visual evidence support the recommendation rather than decorate it?
- Are captions specific about the user impact?

Relevant laws: Selective Attention, Von Restorff Effect, Proximity, Common Region.

## Acceptance Checklist

- Primary action is visible, reachable, and visually dominant.
- Secondary actions are present but visually subordinate.
- Labels, controls, helper text, and errors sit near the relevant object.
- The UI avoids forcing users to compare too many choices at once.
- Feedback appears immediately after every important action.
- Users can recover from mistakes through undo, edit, retry, or saved drafts.
- Responsive layouts preserve grouping and task order.
- Novel interactions have a clear user benefit and support first-time learning.
