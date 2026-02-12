---
tags:
  - composites
---
- **Prompt for Development:** Experimental data showed that the "rectangular box" of Max Stress was wrong. Under combined loading (e.g., pulling and twisting), parts failed earlier than Max Stress predicted. Engineers needed a mathematical shape (an envelope) that fit the data points better.

- **Intuition:** They borrowed the **Von Mises** yield criterion from metals (which describes an ellipse) and stretched it to fit anisotropic composites.

    - **Tsai-Hill:** An adaptation of Hill's yield criterion for metals. It assumes the material is homogeneous but anisotropic.

    - **Hoffman:** Improved Tsai-Hill by allowing different strengths for Tension vs. Compression (which composites definitely have).
    
    - **Tsai-Wu:** The "Golden Standard" of curve fitting. It added even more terms to allow the ellipse to shift and rotate to fit experimental data perfectly.

- The Equations & Meaning (Tsai-Wu example):
$$F_1\sigma_1 + F_2\sigma_2 + F_{11}\sigma_1^2 + F_{22}\sigma_2^2 + 2F_{12}\sigma_1\sigma_2 + \dots = 1$$
- **Physical Meaning:** This represents a smooth surface (ellipsoid) in stress space.

- **The "Interaction Term" ($F_{12}$):** This is the key. It represents the "coupling" between stresses. It mathematically adjusts the strength based on how stresses interact.

- **Flaw:** It is a "black box." If Tsai-Wu says $F=1.1$ (Failure), you don't know if the fibers snapped (catastrophic) or just the matrix cracked (less critical).
