---
tags:
  - composites
  - structures
---
**Prompt for Development:** In the early days, engineers needed a starting point. They applied the logic used for simple isotropic brittle materials: "If it breaks at 100 MPa in a test, don't exceed 100 MPa in the design."

**Intuition:** Imagine a chain. The chain breaks when the weakest link snaps. This theory assumes the composite has distinct "links" (longitudinal, transverse, shear) and checks them one by one. If _any_ link limit is exceeded, the whole thing fails.

The Equations & Meaning:

$$\sigma_1 < X_t$$

$$\sigma_2 < Y_t$$

$$\tau_{12} < S$$

- **Physical Meaning:** These define a rectangular "failure box." It assumes that applying a massive transverse load ($\sigma_2$) has **zero effect** on the fiber's ability to take longitudinal load ($\sigma_1$).

- **Flaw:** In reality, if you twist the material (shear), it usually reduces the amount of tension it can handle. This theory ignores that, often leading to unsafe predictions in combined loading.