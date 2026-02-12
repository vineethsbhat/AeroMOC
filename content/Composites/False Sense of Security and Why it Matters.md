---
tags:
  - composites
---
Using the Failure Index leads to a false sense of security (or over-conservatism depending on the theory) because it doesn't scale linearly with the physical loads. The Reserve Factor corrects this by solving the quadratic equation for the exact load multiplier.

Consider this,
Imagine a shelf made of a composite laminate.

- **Limit:** It breaks at 100 kg.
- **Current Load:** You put 50 kg on it.
- **Stress Exposure ($f_e$):** $50/100 = 0.5$
- **Reserve Factor ($RF$):** $1 / 0.5 = 2.0$ (You can double the weight).
- **Failure Index ($F$):** (Assuming quadratic) $0.5^2 = 0.25$.

If you looked at $F=0.25$, you might intuitively think "I can quadruple the load!" (since $0.25 \times 4 = 1$). **That is wrong.** You can only double it (RF = 2.0).

