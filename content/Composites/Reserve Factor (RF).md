---
tags:
  - composites
---
>The **Reserve Factor (RF)**—often called the **Strength Ratio** in composite mechanics—is the most practical metric for an engineer because it translates complex failure theories into a simple, linear multiple.

- It is used to define the risk of failure on the laminate level.
- RF is defined with the applied load
- If $RF = 2$ then it means the load can be doubles before FPF occurs

>The intuition behind the Reserve Factor is strictly linear. It represents the factor by which you can multiply your current applied loads before the part fails.

Mathematically it is the inverse of the stress exposure

### [Geometric Meaning :]
Imagine a 2D graph where the X-axis is stress in the fiber direction ($\sigma_{1}$) and the Y-axis is stress in the transverse direction ($\sigma_{2}$).

1. **The Failure Envelope:** A shape (usually an ellipse for Tsai-Wu) drawn around the origin. Anything outside this shape is failed.
2. **The Load Vector:** Draw a line from the origin $(0,0)$ to your current applied stress point.

3. **The Reserve Factor:** This is the ratio of the total distance to the boundary versus the distance to your current point.

$$RF = \frac{\text{Distance from Origin to Failure Envelope}}{\text{Distance from Origin to Applied Stress Point}}$$
==Key Takeaway==
Because it is a ratio of lengths, it is linear. If you double the load, the "Distance to Applied Stress Point" doubles, and the RF is cut exactly in half.

[How is this related to Margin of Safety (MOS) ?]
The Reserve Factor tells you the total capacity, while the Margin of Safety tells you the **excess** capacity.
$$M.S. = RF - 1$$
- **If RF = 1.5:** You can take 1.5 times the load.
- **M.S. = 0.5 (or 50%):** You have 50% _extra_ capability beyond what is required.

---
[[False Sense of Security and Why it Matters]]