---
tags:
  - fea
  - structures
---
There are two distinct approaches to buckling analysis,
1. [Linear] or more commonly called as 'Eigenvalue'
2. [Non-Linear] or P-Delta/Post Buckling Analysis

The goal of a linear analysis is to find the theoretical 'perfect' buckling load, while in a non-linear analysis the goal is to figure out the 'real world' failure load. The most common assumptions that we generally hold for linear analysis are true, ==small deflections, linear elastic material== but for non-linear buckling the assumptions change, ==large deflections, material yielding, imperfections==

The output in FEA that we are looking for are also vastly different, 
1. Linear - BLF = Buckling Load Factor and Mode Shapes
2. Non-Linear - Load vs. Displacement Curve and Ultimate Strength


### Linear Eigenvalue Buckling (LBA)

This is an idealized mathematical approach. It solves the equation $([K]+ \lambda_i​[Kg​]){\psi_i}​=0$, where [K] is the stiffness matrix and [Kg​] is the geometric stiffness matrix.

- **The "Perfect" World:** It assumes the structure is geometrically perfect and remains linear until it suddenly snaps.

- Use Case: It is often used as a quick screening tool to find the **Buckling Load Factor (BLF)**. If the BLF is 1.5, the structure theoretically buckles at 150% of the applied load.

- Short Computing Time

- Easy to define

- No convergence problems

- The ultimate outcome/result may be wrong since we aren't accounting for real world conditions 

### Nonlinear Buckling Analysis

This approach is more computationally expensive but necessary for flight-critical hardware. It accounts for "real world" physics:

- **Geometric Nonlinearity:** Accounts for the fact that as the structure deforms, the direction of the loads changes.

- **Imperfections:** Real aerospace parts aren't perfect; they have "dents" or manufacturing variances that significantly lower the buckling capacity.

- **Material Nonlinearity:** Accounts for the metal yielding or composite plies failing before buckling occurs.

- You can animate instability failure process

- Outcome is more robust

- Requires much more computational effort (memory allocation, symmetry, solver settings), convergence problems, far more difficult to set up


