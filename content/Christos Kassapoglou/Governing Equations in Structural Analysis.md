---
tags:
  - structures
---
Structural analysis is more often the delicate balance of stiffness, strength and weight. The governing equations of structural mechanics form a closed-loop system often referred to as the "Holy Trinity" of elasticity: **Equilibrium**, **Kinematics (Compatibility)**, and **Constitutive Laws**.

1. ==Equilibrium Equations (Static & Dynamic)
==
These equations ensures the physics is obeyed, specifically Newton's 2nd Law ($F = ma$)
The equation in 3D continuum mechanics is given as,

$$\nabla \cdot \sigma + f = \rho \ddot u$$
Where,
- $\boldsymbol{\sigma}$ is the Cauchy Stress Tensor.
- $\mathbf{f}$ is the body force (gravity, magnetic).
- $\rho \ddot{\mathbf{u}}$ is the inertial term (mass $\times$ acceleration).

>Imagine a tiny, infinitesimal cube inside a wing spar. For that cube to stay in place (or accelerate predictably), the stresses pushing on its faces plus any gravity pulling on its center must sum to zero (or equal its mass times acceleration)

We derive this by taking an arbitrary volume of material, summing all surface traction vectors and body forces, and setting them equal to the rate of change of momentum. Applying the Divergence Theorem allows us to convert surface integrals to volume integrals, leading to the differential form shown above.

In the historical development : Galileo struggled with describing forces in 3D, 'Loui Cauchy' introduced the idea of a [Stress Tensor]. The idea that stress depends on the direction and he proved that state of stress at a point can be represented by a 3 x 3 matrix. 

2. ==Kinematic Equations (Strain-Displacement)==
These equations describe the geometry of deformation without caring about forces. They relate how points move (displacement) to how the material stretches (strain). 

For small deformations (linear elasticity), the strain tensor $\boldsymbol{\varepsilon}$ is related to the displacement vector $\mathbf{u}$:

$$\boldsymbol{\varepsilon} = \frac{1}{2} (\nabla \mathbf{u} + (\nabla \mathbf{u})^T)$$

Or in index notation:

$$\varepsilon_{ij} = \frac{1}{2} \left( \frac{\partial u_i}{\partial x_j} + \frac{\partial u_j}{\partial x_i} \right)$$
>If you pull a rubber band, the "displacement" is how far the end moves. The "strain" is the percentage change in length. This equation mathematically links the two and it ensures that the material doesn't tear apart or fold into itself  because we have assumed it to be a continuum.

Since we have 6 strain components but only 3 displacement components, the strains cannot vary arbitrarily. This is where [Saint-Venant's Principle] comes in, they must be 'compatible' in the sense of the structures response must be such that it remains continuous. This is enforced by the equation :

$$\nabla \times (\nabla \times \boldsymbol{\varepsilon})^T = 0$$

Historically this equation grew out of geometrical analysis of a beam. In the mid 1700s Euler was fascinated with how a beam bent under load ('Elastic Curve'). He derived the curvature equation

$$k = \frac{d^2 y}{dx^2}$$
which was the 1D version of the strain displacement equation

3. ==Constitutive Equations (Material Law)==
This links the first two pillars. It relates Stress (Force) to Strain (Deformation). The Equation (Generalized Hooke's Law) is given as :


$$\boldsymbol{\sigma} = \mathbf{C} : \boldsymbol{\varepsilon}$$

Where $\mathbf{C}$ is the stiffness tensor (a $4^{th}$ order tensor). For an isotropic material (like aluminum used in fuselages), this simplifies using Young's Modulus ($E$) and Poisson's ratio ($\nu$):


$$\sigma_{ij} = \frac{E}{1+\nu} \left( \varepsilon_{ij} + \frac{\nu}{1-2\nu} \varepsilon_{kk} \delta_{ij} \right)$$

>It tells us that if we squeeze the material (strain), it will push back (stress).

>[!Historical Development :]
>- **1660:** **Robert Hooke** discovered "Ut tensio, sic vis" (As the extension, so the force). He famously published it as an anagram to claim priority without revealing the secret immediately.
>- **1807:** **Thomas Young** formalized this into a constant property of the material (Young's Modulus), separating geometry from material properties.

### Here's where the magic happens :

When you substitute the kinematic and constitutive equations _into_ the equilibrium equation, you get the governing equation for displacement:

$$(\lambda + \mu) \nabla (\nabla \cdot \mathbf{u}) + \mu \nabla^2 \mathbf{u} + \mathbf{f} = 0$$

- (Where $\lambda$ and $\mu$ are Lamé parameters, related to $E$ and $\nu$).

>This equation is what Finite Element Analysis (FEA) solvers (like Nastran or Abaqus) are essentially solving when you run an FEA simulation









---
Take a look at : [[Euler Bernoulli Beam Theory]] , [[Kirchhoff-Plate Theory]], [[Timoshenko-Beam Theory]] , [[Bredt-Batho Theory]] , [[Donnell-Mushtari-Vlasov (DMV) Theory]] 