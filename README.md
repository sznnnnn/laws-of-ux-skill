# Laws of UX Skill

A Codex/Cursor skill that combines **Laws of UX** (psychology-driven design decisions) with **BuddyUp/v0-ai product design spec** and **design-governance checklists** for implementation-ready reviews.

Designed for:

- UX/UI critique and heuristic review
- **设计规范** enforcement and **UI 审查**
- Product flow design (问卷 → 匹配 → 工作台 → 文书)
- Frontend implementation guidance (Tailwind v4, shadcn/ui, tokens)
- Interface acceptance checks with P0–P3 severity
- Turning UX principles into concrete, verifiable product decisions

## Two Layers

### UX laws (why)

- **Primary laws**: Jakob's Law, Fitts's Law, Miller's Law, Hick's Law, Postel's Law, Peak-End Rule, Aesthetic-Usability Effect, Von Restorff Effect, Tesler's Law, Doherty Threshold.
- **Secondary laws**: Choice Overload, Chunking, Cognitive Load, Flow, Goal-Gradient Effect, Common Region, Proximity, Similarity, Mental Models, Occam's Razor, Pareto Principle, Selective Attention, Serial Position Effect, Working Memory, Zeigarnik Effect, and more.

Each recommendation can be tagged **Validated / Contextual / Experimental** to avoid over-claiming.

### Product design spec (what)

Executable rules for BuddyUp/v0-ai: Notion-like tokens, shadcn components, interaction (⌘K, ⌘B, modals), onboarding tours (`data-tour`), copy/IA, accessibility, and maintenance conventions.

## Files

| Path | Purpose |
|------|---------|
| `SKILL.md` | Triggers, dual workflow (UX + governance), acceptance checklist |
| `references/laws-map.md` | Primary/Secondary laws map |
| `references/ux-thinking.md` | Overall UX thinking frame |
| `references/review-rubric.md` | Severity model + review passes + product spec pass |
| `references/design-governance-workflow.md` | Five-domain audit, P0–P3, PR self-check |
| `references/buddyup-product-design-spec.md` | Full product design spec (tokens → tours) |
| `references/cn-open-ux-notes.md` | Chinese examples and framing |
| `references/metrics-mapping.md` | Laws → measurable metrics |
| `references/visual-evidence-guide.md` | Screenshots and diagram evidence |
| `templates/ux-review-template.md` | Generic review template |
| `templates/buddyup-design-review-template.md` | Law + spec combined template |
| `examples/ecommerce-checkout-review.md` | Sample checkout review |
| `assets/images/*` | Visual examples for README/reviews |
| `agents/openai.yaml` | Codex skill UI metadata |

## Install

```bash
# Cursor / Codex skills directory (example)
git clone https://github.com/sznnnnn/laws-of-ux-skill.git ~/.codex/skills/laws-of-ux-2
```

Or symlink from your project's `.cursor/skills/` if you vendor skills per repo.

## Source

- [Laws of UX](https://lawsofux.com/) by Jon Yablonski
- BuddyUp/v0-ai `设计规范.md` and design-governance practice
