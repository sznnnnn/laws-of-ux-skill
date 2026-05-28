---
name: laws-of-ux-2
description: Use when designing, reviewing, or refining UI/UX with Laws of UX principles; prioritizes Primary laws and uses Secondary laws to turn UX psychology into product decisions, interface critiques, frontend guidance, and acceptance checks.
---

# Laws of UX

Use this skill when the user asks to follow Laws of UX, improve usability, critique a UI, design a product flow, implement a frontend, or turn UX psychology principles into concrete interface choices.

This skill distills Laws of UX into a working method. Do not recite the laws unless the user asks. Apply the smallest useful set of laws to the design decision in front of you.

Treat Laws of UX as a systematic UX thinking tool: a collection of psychological and behavioral design principles for understanding user perception, cognition, attention, memory, motivation, and behavioral responses in interfaces. The goal is to turn experience into reusable product judgment.

Use the user's taxonomy:

- Primary laws are the default decision frame. Use these first for core product, interaction, and usability calls.
- Secondary laws are diagnostic and supporting tools. Use these to explain edge cases, refine hierarchy, reduce friction, or add nuance.

## Core Workflow

1. Identify the user's intent and the task type:
   - New design: create structure, hierarchy, interaction states, and copy.
   - Existing UI review: find friction, ambiguity, overload, and mismatch with user expectations.
   - Frontend implementation: encode the UX decision in layout, component behavior, defaults, states, and validation.
   - Product flow: reduce decision cost, improve recovery, and make progress visible.
2. Choose 3-7 relevant laws from `references/laws-map.md`. Start with Primary laws, then add Secondary laws only where they sharpen the recommendation.
3. Convert laws into interface decisions:
   - What should be visible first?
   - What should be grouped, hidden, deferred, or removed?
   - What should be default, constrained, confirmed, reversible, or automated?
   - What state must the UI communicate before, during, and after action?
4. Check the result against the UX acceptance checklist below.
5. When delivering, explain decisions in product language, not academic psychology terms, unless the user asked for the theory.

## UX Acceptance Checklist

Before marking a UI or flow complete, verify:

- Primary action is visually obvious and placed where users naturally finish reading or scanning.
- Secondary actions are available but lower emphasis than the primary path.
- Related controls and information are grouped; unrelated items are separated.
- The screen does not ask users to compare, remember, or decide among too many options at once.
- Defaults are helpful, safe, and easy to override.
- Feedback appears immediately after user action: loading, success, error, empty, disabled, and partial states are designed.
- Destructive or high-cost actions are prevented, confirmed, or reversible.
- The interface uses familiar patterns for the domain unless a clear product reason justifies novelty.
- Important text is concise, concrete, and close to the thing it explains.
- Layout works at realistic desktop and mobile sizes with no overlap, truncation, or unstable controls.

## Practical Heuristics

### Reduce Choice And Memory Load

- Put the common path first, make uncommon paths available later.
- Use recognition over recall: visible labels, examples, previews, recent items, templates, and inline hints.
- Collapse advanced settings until the user demonstrates need.
- Use progressive disclosure for complex forms, dashboards, and configuration tools.

Relevant laws: Hick's Law, Miller's Law, Tesler's Law, Jakob's Law, Choice Overload, Chunking, Working Memory.

### Make Actions Feel Immediate And Recoverable

- Show instant feedback even when the real operation takes longer.
- Use optimistic UI only when failure is low-risk and recovery is clear.
- Make undo, retry, edit, and backtracking obvious for consequential actions.
- Prefer guardrails over blame-heavy error messages.

Relevant laws: Doherty Threshold, Peak-End Rule, Postel's Law, Zeigarnik Effect, Flow, Parkinson's Law.

### Design For Attention

- One screen should have one strongest visual priority.
- Use size, contrast, spacing, and placement to guide attention before adding explanatory text.
- Keep urgent information visually distinct from ordinary decoration.
- Avoid decorative motion or color that competes with task-critical information.

Relevant laws: Von Restorff Effect, Fitts's Law, Prägnanz, Selective Attention, Common Region.

### Align With Expectations

- Reuse platform and domain conventions for navigation, forms, filters, tables, account flows, and commerce flows.
- Put controls where users expect them, especially close to the object they affect.
- Make labels match user vocabulary, not implementation vocabulary.
- When the product must behave unexpectedly, explain before the surprise.

Relevant laws: Jakob's Law, Mental Models, Serial Position Effect, Proximity, Similarity, Cognitive Bias.

### Manage Complexity Honestly

- Do not merely hide necessary complexity; move it to the right moment.
- Break long flows into named steps with visible progress.
- Use summaries and previews before submission.
- Preserve user input when validation fails.

Relevant laws: Tesler's Law, Goal-Gradient Effect, Cognitive Load, Zeigarnik Effect, Pareto Principle, Occam's Razor.

## Output Patterns

For a UX review, use:

```markdown
**Findings**
- [Severity] Issue: impact. Recommendation.

**Applied Laws**
- Law name: why it matters here.

**Acceptance Checks**
- What to verify in implementation.
```

For a design or implementation task, use:

```markdown
**UX Direction**
Short design rationale in product language.

**Key Decisions**
- Layout / hierarchy
- Interaction states
- Defaults and constraints
- Recovery and feedback

**Verification**
- Desktop/mobile visual check
- Interaction and state check
```

## References

- Read `references/laws-map.md` when you need to select laws or explain the rationale.
- Read `references/ux-thinking.md` when you need the user's overall philosophy for applying the laws.
- Read `references/review-rubric.md` when the user asks for a UX review, design critique, Figma review, frontend review, or acceptance criteria.
- Source basis: the user's UX norms and Laws of UX by Jon Yablonski. This skill is a practical distillation, not a verbatim copy.
