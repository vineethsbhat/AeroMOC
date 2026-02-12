---
tags:
  - composites
---
Elasticity : Refers to the behaviour of a material within the elastic region of the stress strain curve wherein the deformation on said material is reversible, i.e., the deformation vanishes completely upon unloading. This inherently means that ==the material does not exhibit inner friction or damping==

Since the equation of stress is given as, $\sigma \propto \epsilon$ 
We have, $$\sigma = E \cdot \epsilon$$
This is called Hookean elasticity. In the generalised model for a 3D stress state, we have 3 normal stresses, 3 shear stress, thus a $(6 \times 6)$ matrix and a need for 36 constants to define the material behaviour at that point. Given the stress element is in equilibrium then the shear stress terms must be equal and now reduce the number of constants in the stiffness matrix to 21

## Types of Behaviour 

1. Anisotropic : With the derivation of strain energy density function we can see that compliance and stiffness matrix are symmetric and thus we need 21 constants. Coupling between all normal and shear stresses and strains are present.
2. Orthotropic : 3 planes of symmetry, 9 constants. No shear-shear coupling and no normal-shear coupling.
3. Transversely Isotropic : As name suggests the material is isotropic in the transverse axis. 5 independent constants.
4. Isotropic : Infinite number of planes of symmetry, 2 constants needed ($E,\mu,$ or $E,G$)
5. Plane Stress Condition : Simplifies this further - stress in the thickness direction is not applicable since the thickness is considered to be less. Therefore, $\sigma_3 = \tau_{13} = \tau_{23} = 0$ which now gives a $3 \times 3$ matrix. We need 4 independent constants

Constants used to define material behaviour
a. Young's Modulus
b. Shear Modulus
c. Poisson's Ratio


