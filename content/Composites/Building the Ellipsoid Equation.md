---
tags:
  - composites
---
Unlike the max. stress and strain theory, to account for the interactions, we must fit the curve to the experimental data. Thus we introduce the general mathematical approach for "Interactive" criteria (like Tsai-Wu). instead of a box, we want to fit a smooth curve (an ellipsoid) to the failure data.

==The Monster Ellipsoid Equation==

This is just the general equation for a 3D surface (an ellipsoid). It has linear terms ($A$) and quadratic terms ($B$). Since this equation is complex we need to simplify it. We do so by making assumptions. We do not want to run 50 tests to figure out the value of $A$ and $B$ coefficient.
1. Failure must be independent of the direction of shear
2. Normal and Shear Strengths are all uncoupled
3. Transverse Isotropy is assumed

>[Coordinate Invariance and the Idea of Principle Stress and Strain for Failure Theories :]
- **The Logic:**
- **Nature doesn't care about your math:** The material fails when it fails. It doesn't care if you call your axes "X and Y" or rotate them 45 degrees.

- **The Trick:**
1. Imagine a block under **Pure Shear** ($\tau_{23}$).

2. Rotate your view **45 degrees**. In this new view, "Pure Shear" looks exactly like "Tension in one direction + Compression in the other" ($\sigma'_2, \sigma'_3$).

3. Calculate the Failure Index ($F$) for both views using the big equation from Slide 2.

4. Since the failure reality is the same, the two $F$ values must be equal.

The Payoff (Red Box):
By equating them, they prove that $B_{44} = 2(B_{22} - B_{23})$. 

**Why do we care?** 
It saves money. We don't need to test for $B_{44}$ explicitly; we can calculate it from other values we already have ($B_{22}$ and $B_{23}$).


## [Theories :]

|**Criterion**|**f1​**|**f2​**|**f3​**|**f11​**|**f22​**|**f33​**|**f44​**|**f55​**|**f66​**|**f12​**|**f13​**|**f23​**|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|**Tsai-Wu**|$\frac{1}{X_t} - \frac{1}{X_c}$|$\frac{1}{Y_t} - \frac{1}{Y_c}$|$\frac{1}{Z_t} - \frac{1}{Z_c}$|$\frac{1}{X_t X_c}$|$\frac{1}{Y_t Y_c}$|$\frac{1}{Z_t Z_c}$|$\frac{1}{S_T^2}$|$\frac{1}{S_T^2}$|$\frac{1}{S_L^2}$|$-\frac{1}{2\sqrt{X_t X_c Y_t Y_c}}$|$-\frac{1}{2\sqrt{X_t X_c Z_t Z_c}}$|$-\frac{1}{2\sqrt{Y_t Y_c Z_t Z_c}}$|
|**Tsai-Hill**|$0$|$0$|$0$|$\frac{1}{X^2}$|$\frac{1}{Y^2}$|$\frac{1}{Z^2}$|$\frac{1}{S_T^2}$|$\frac{1}{S_T^2}$|$\frac{1}{S_L^2}$|$-\frac{1}{2}(\frac{1}{X^2}+\frac{1}{Y^2}-\frac{1}{Z^2})$|$-\frac{1}{2}(\frac{1}{Z^2}+\frac{1}{X^2}-\frac{1}{Y^2})$|$-\frac{1}{2}(\frac{1}{Y^2}+\frac{1}{Z^2}-\frac{1}{X^2})$|
|**Azzi-Tsai**|$0$|$0$|$0$|$\frac{1}{X^2}$|$\frac{1}{Y^2}$|$0$|$0$|$0$|$\frac{1}{S_L^2}$|$-\frac{1}{X^2}$|$0$|$0$|
|**Hoffmann**|$\frac{1}{X_t} - \frac{1}{X_c}$|$\frac{1}{Y_t} - \frac{1}{Y_c}$|$\frac{1}{Z_t} - \frac{1}{Z_c}$|$\frac{1}{X_t X_c}$|$\frac{1}{Y_t Y_c}$|$\frac{1}{Z_t Z_c}$|$\frac{1}{S_T^2}$|$\frac{1}{S_T^2}$|$\frac{1}{S_L^2}$|$-\frac{1}{2}(\frac{1}{X_t X_c}+\frac{1}{Y_t Y_c}-\frac{1}{Z_t Z_c})$|$-\frac{1}{2}(\frac{1}{X_t X_c}+\frac{1}{Z_t Z_c}-\frac{1}{Y_t Y_c})$|$-\frac{1}{2}(\frac{1}{Y_t Y_c}+\frac{1}{Z_t Z_c}-\frac{1}{X_t X_c})$|
|**Yamada-Sun**|$0$|$0$|$0$|$\frac{1}{X^2}$|$0$|$0$|$0$|$0$|$\frac{1}{S_L^2}$|$0$|$0$|$0$|

