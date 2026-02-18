---
tags:
  - composites
  - structures
---
The von Kármán equations are a cornerstone of structural mechanics, specifically used to describe the **large deflections** of thin plates.

For a composite plate, the von Kármán theory is expressed as a system of two coupled partial differential equations. These involve the **out-of-plane deflection** (w) and the [[Airy stress function (ϕ)]], which represents the in-plane internal forces.

The key idea is this :

>**Von Kármán theory** applies when deflections are "moderately large" (roughly on the order of the plate's thickness). In this regime, **geometric nonlinearity** kicks in.

$$D_{11}\frac{\partial^4 w}{\partial x^4} + 2(D_{12} + 2D_{66})\frac{\partial^4 w}{\partial x^2 \partial y^2} + D_{22}\frac{\partial^4 w}{\partial y^4} = N_x\frac{\partial^2 w}{\partial x^2} + \dots + p_z$$
The LHS represents the bending resistance, The $D_{ij}$ terms are the bending stiffnesses of the composite laminate. This side says, "The stiffer the plate ($D$), the harder it is to curve ($w$)." The RHS is where the coupling happens,
- $p_z$: The external pressure pushing down on the plate.
- $N_x, N_y, N_{xy}$: These are the in-plane (membrane) forces (tension/compression).
- $\frac{\partial^2 w}{\partial x^2}$: This is the curvature of the plate.

