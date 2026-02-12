---
tags:
  - composites
---
- **Prompt for Development:** The "Black Box" problem of Tsai-Wu was frustrating. Engineers needed to know **how** the part failed to improve the design. If the matrix is weak, adding more fibers won't help. They needed criteria that distinguished between **Fiber Failure (FF)** and **Inter-Fiber Failure (IFF)** (Matrix cracking).

- **Intuition:**

- **Hashin:** Proposed that we need two distinct checks. One equation checks if the fibers break (mostly driven by $\sigma_1$). A separate equation checks if the matrix cracks (driven by $\sigma_2$ and $\tau_{12}$).

- **Puck:** An evolution of Hashin. Puck realized that matrix cracks usually happen on a slanted "fracture plane" (like soil sliding down a hill). Puck's theory searches for this specific angle of fracture to predict failure more accurately in compression/shear.

- **The Equations & Meaning:**
- Instead of one equation $F=1$, you get a set of equations:

1. **Fiber Tension:** $(\frac{\sigma_1}{X_t})^2 + (\frac{\tau_{12}}{S})^2 = 1$ (Note: Hashin includes shear here, acknowledging some interaction).

2. **Matrix Compression:** A complex function of $\sigma_2$ and $\tau_{12}$.

- **Physical Meaning:** These equations map directly to what you see under a microscope. If the "Matrix Mode" equation exceeds 1, you will see cracks between in the matrix. If "Fiber Mode" exceeds 1, you see snapped fibers.

