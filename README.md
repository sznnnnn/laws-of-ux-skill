# Laws of UX Skill

A Codex/Cursor skill that turns **Laws of UX** into concrete product judgment: UX reviews, product-flow redesign, frontend acceptance checks, and BuddyUp/v0-ai design-governance audits.

Inspired by the packaging discipline in `alchaincyf/huashu-design`: clear trigger surface, opinionated workflow, visual examples, and deliverables that look useful before you read every reference file.

```bash
npx skills add sznnnnn/laws-of-ux-skill
```

Try it with:

```text
Use $laws-of-ux-2 to review this checkout flow. Give me P0-P3 findings, applied laws, metrics, and acceptance checks.
Use $laws-of-ux-2 to redesign this onboarding screen for lower cognitive load.
Use $laws-of-ux-2 to inspect this frontend implementation before release.
Use $laws-of-ux-2 to review this BuddyUp page against UX laws and the product design spec.
```

## Two Layers

### UX laws (why)

- **Primary laws**: Jakob's Law, Fitts's Law, Miller's Law, Hick's Law, Postel's Law, Peak-End Rule, Aesthetic-Usability Effect, Von Restorff Effect, Tesler's Law, Doherty Threshold.
- **Secondary laws**: Choice Overload, Chunking, Cognitive Load, Flow, Goal-Gradient Effect, Common Region, Proximity, Similarity, Mental Models, Occam's Razor, Pareto Principle, Selective Attention, Serial Position Effect, Working Memory, Zeigarnik Effect, and more.

Each recommendation can be tagged **Validated / Contextual / Experimental** to avoid over-claiming.

### Product design spec (what)

Executable rules for BuddyUp/v0-ai: Notion-like tokens, shadcn components, interaction (Cmd+K, Cmd+B, modals), onboarding tours (`data-tour`), copy/IA, accessibility, and maintenance conventions.

## What It Delivers

| Task | Output | Best used for |
|---|---|---|
| UX review | Verdict, P0-P3 findings, Keep/Fix/Quick Wins, applied laws, evidence tags | Existing UI, Figma, screenshots, prototypes |
| Flow redesign | IA/hierarchy decisions, interaction states, defaults, recovery paths | Checkout, onboarding, settings, dashboards |
| Frontend acceptance | Visual, responsive, state, and interaction pass conditions | Before shipping a coded interface |
| BuddyUp governance | Token/component/copy/accessibility/tour audit | 设计规范, UI 审查, visual consistency |
| Metrics plan | Primary/guardrail metrics and experiment hypothesis | Turning design advice into validation work |
| Visual evidence | Before/after diagrams or annotated screenshots | Explaining impact quickly to teammates |

## Visual Example

![Checkout before](assets/images/checkout-before.svg)
Before: shipping options and optional settings are mixed, increasing decision load.

![Checkout after](assets/images/checkout-after.svg)
After: recommended shipping is default, advanced options are collapsed, and primary CTA is emphasized.

![Checkout funnel](assets/images/checkout-funnel.svg)
Supporting chart: drop-off concentration at shipping step to validate optimization priority.

## Review Shape

```markdown
**Verdict**
- Score: 7.2/10
- Release risk: medium
- Main UX issue: users must compare too much before they can continue.

**Keep**
- The checkout step order matches user expectations.

**Fix**
- [P1] Shipping choices are all exposed at once, raising decision load.
  Recommendation: default to the recommended option and collapse advanced methods.

**Quick Wins**
- [ ] Make the primary CTA sticky on mobile.
- [ ] Move optional coupon/invoice controls into a collapsed section.
- [ ] Add immediate feedback after shipping selection.

**Applied Laws**
- Hick's Law -> reduce simultaneous choices.
- Fitts's Law -> keep the primary action reachable.

**Acceptance Checks**
- Mobile CTA remains visible at 390px width.
- Users can change shipping method after accepting the default.
```

## Files

| Path | Purpose |
|------|---------|
| `SKILL.md` | Triggers, dual workflow (UX + governance), acceptance checklist |
| `references/laws-map.md` | Primary/Secondary laws map |
| `references/ux-thinking.md` | Overall UX thinking frame |
| `references/review-rubric.md` | Severity model, review passes, scoring, visual evidence, product spec pass |
| `references/design-governance-workflow.md` | Five-domain audit, P0-P3, PR self-check |
| `references/buddyup-product-design-spec.md` | Full product design spec (tokens -> tours) |
| `references/cn-open-ux-notes.md` | Chinese examples and framing |
| `references/metrics-mapping.md` | Laws -> measurable metrics |
| `references/visual-evidence-guide.md` | Screenshots and diagram evidence |
| `templates/ux-review-template.md` | Generic review template |
| `templates/buddyup-design-review-template.md` | Law + spec combined template |
| `examples/ecommerce-checkout-review.md` | Sample checkout review |
| `assets/images/*` | Visual examples for README/reviews |
| `agents/openai.yaml` | Codex skill UI metadata |

## Install

```bash
git clone https://github.com/sznnnnn/laws-of-ux-skill.git ~/.codex/skills/laws-of-ux-2
```

Or symlink from your project's `.cursor/skills/` if you vendor skills per repo.

## Source

- [Laws of UX](https://lawsofux.com/) by Jon Yablonski
- BuddyUp/v0-ai design spec and design-governance practice
