---
tags:
  - composites
---
Multiscale modeling is essentially the art of "zooming in and out" of a material. For composites, this is crucial because what happens at the microscopic level (a tiny crack between a fiber and resin) eventually dictates whether a massive structure like an airplane wing fails.

Since modeling every single fiber in a large structure is computationally impossible, we use a "divide and conquer" approach across three primary scales.

### 1. The Three Primary Scales

To model a composite, researchers typically break the problem down into these levels:

- **Micro-scale:** We look at individual fibers, the surrounding matrix (resin), and the "interface" where they bond.

- **Meso-scale:** This focuses on the **Representative Volume Element (RVE)** or a single "ply." We treat the material as a repetitive pattern of fibers.

- **Macro-scale:** The "big picture." The entire component is treated as a single, homogenous material with averaged properties.

### 2. The Core Methods

There are two main ways to link these scales together: **Hierarchical** and **Concurrent** modeling.

#### A. Hierarchical Modeling (The "Bottom-Up" Approach)

This is the most common method. You start at the smallest scale and pass information upward.

1. **Homogenization:** You analyze a small RVE at the micro-scale to find its "effective" properties. For example, if you know the stiffness of the fiber (Ef​) and the matrix (Em​), you calculate the overall stiffness of the ply (Eeff​).
2. **Information Transfer:** These calculated properties are then plugged into a macro-scale Finite Element Analysis (FEA) model as constant values.

#### B. Concurrent Modeling (The "Real-Time" Approach)

This is much more computationally "expensive." Instead of pre-calculating values, the macro-scale model talks to the micro-scale model in real-time.

- If the macro-model detects high stress in a specific area, it "calls" the micro-model to simulate exactly what is happening to the fibers in that spot.

- This is often done using **FE² methods**, where every integration point in a large mesh is actually another smaller mesh.

|**Step**|**Technique**|**Goal**|
|---|---|---|
|**RVE Definition**|Statistical Analysis|Finding the smallest unit that accurately represents the whole material.|
|**Boundary Conditions**|Periodic Boundary Conditions (PBCs)|Ensuring the small "cube" of material behaves as if it's part of a larger continuous sheet.|
|**Localization**|De-homogenization|Once you know the macro-stress, "zooming back in" to see if that stress caused a fiber to snap.|
