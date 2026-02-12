---
tags:
  - composites
---
Imagine the fibers and matrix are stacked one on top of the other.

- **Scenario:** You pull on the composite perpendicular to the fibers (transverse loading).
- **Intuition:** The load must pass through the matrix, then the fiber, then the matrix again. They feel the **same force** (Iso-stress).
- **Result:** The weakest link (the matrix) dominates the deformation. Even if you have super-stiff fibers, the soft matrix effectively "bottlenecks" the stiffness. This gives you the **Lower Bound** of stiffness.

>iROM for transverse modulus shows poor corelation with physical tests because of inhomogeneous stress strain field in the cross-section

We are basically saying: **"The Inverse Rule of Mixtures (iROM) assumes a simplistic scenario that doesn't match the complex way stress actually flows around round fibers."**  
The prediction is if you pull on this stack, every layer feels the **exact same stress** (Iso-stress). The soft matrix layers are free to squish as much as they want. But because the soft matrix is "free" to deform, it dominates the behavior. The iROM predicts a very "soft" material (a low modulus).

The major reason for this is due to the '==Unconstrained Poisson's Effect==' : In a composite, the matrix is glued to stiff fibers that _don't_ want to get thinner. The fibers act like rigid clamps, preventing the matrix from shrinking sideways. Because the matrix is prevented from contracting naturally, it becomes stiffer 

Certain advanced approaches can be used to better predict $E_2$ such as the square-cylinder model, high fidelity FE Model etc.

ROM : Math is dominated by fibers in longitudinal direction therefore it is the upper limit
iROM : Math is dominated by matrix in transverse direction therefore it is the lower limit

Here's the table of how it is to be understood :

|**Condition**|**Geometry**|**Constraint**|**Correct Model**|
|---|---|---|---|
|**Longitudinal**|Fibers are continuous from end to end.|Matrix is forced to follow fiber.|**Iso-strain** (RoM)|
|**Transverse**|Fibers are discontinuous (interrupted by matrix).|Matrix is free to stretch between fibers.|**Iso-stress** (iROM)|

