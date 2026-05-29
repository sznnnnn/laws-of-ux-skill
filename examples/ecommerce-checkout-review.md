# Example: E-commerce Checkout UX Review

## Context

- Surface: mobile checkout page
- Task: complete payment
- Pain points: high abandonment on shipping step

## Findings

- [P1] Too many shipping options shown at once creates decision paralysis.
  - Recommendation: show one recommended option + "view all methods."
  - Laws: Hick's Law, Choice Overload.
  - Tag: `Validated`

- [P1] Pay button is visually weak and below fold on small screens.
  - Recommendation: sticky primary CTA in thumb zone.
  - Laws: Fitts's Law, Selective Attention.
  - Tag: `Validated`

- [P2] Coupon, points, invoice settings are mixed with required fields.
  - Recommendation: collapse optional settings under "Advanced payment options."
  - Laws: Tesler's Law, Cognitive Load.
  - Tag: `Contextual`

## Acceptance Checks

- Checkout completion rate increases without higher refund/dispute rates.
- Median time from shipping step to payment confirmation decreases.
- Repeated tap rate on pay CTA decreases.

## Visual Evidence (Example Structure)

![Figure 1 - Checkout before](../assets/images/checkout-before.svg)
Figure 1. Before: shipping options and optional tools are mixed, causing decision overload.

![Figure 2 - Checkout after](../assets/images/checkout-after.svg)
Figure 2. After: recommended shipping shown by default, advanced options collapsed, sticky pay CTA added.

![Figure 3 - Funnel by step](../assets/images/checkout-funnel.svg)
Figure 3. Supporting metric view: drop-off by step to validate whether shipping-step changes improve completion.
