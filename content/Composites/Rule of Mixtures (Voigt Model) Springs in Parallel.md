---
tags:
  - composites
---
Consider the fiber and matrix to be as two springs connected in parallel. If the modulus are $E_m$ and $E_{f,1}$. Loading in the longitudinal direction results in the strain being the same in fiber and matrix. Therefore, we have

Isostrain = $\epsilon_{f,1} = \epsilon_{m} = \epsilon_{1}$

The longitudinal stiffness is given as,
$$E_1 = E_{f,1} \cdot \phi_f + E_m \cdot (1 - \phi_f)$$
Assumed perfect bonding between fiber and matrix and the cross section to be quadratic in nature. 
Steps in derivation :
1. Force equilibrium = Total force = force on fiber in direction 1 + force on matrix in direction 1
2. Isostrain condition 
3. Hook's law = write stress in fiber, matrix and direction 1 as a function of strain and young's modulus
4. Simplify

>Due to the high modulus of the fiber in longitudinal direction, the composite modulus is very much driven by the fiber

>[!Important]
>The **Rule of Mixtures (RoM)** and the **Inverse Rule of Mixtures (iROM)** are the foundational mathematical models used to estimate the properties of composite materials. They serve as the "Upper Bound" and "Lower Bound" for predicting how a mixture of two materials will behave. 

ROM : The stiffer material (fiber) takes the majority of the load. This arrangement is very efficient, providing high stiffness. This gives you the **Upper Bound** of stiffness. 

This is the table that is to be remembered : 

| **Property to Estimate**              | **Rule Used**        | **Formula**                                            | **Direction of Load**       |
| ------------------------------------- | -------------------- | ------------------------------------------------------ | --------------------------- |
| **Longitudinal Modulus ($E_1$)**      | **Rule of Mixtures** | $E_c = V_f E_f + V_m E_m$                              | **Parallel** to fibers      |
| **Transverse Modulus ($E_2$)**        | **iROM**             | $\frac{1}{E_c} = \frac{V_f}{E_f} + \frac{V_m}{E_m}$    | **Perpendicular** to fibers |
| **Density ($\rho$)**                  | **Rule of Mixtures** | $\rho_c = V_f \rho_f + V_m \rho_m$                     | N/A (Scalar property)       |
| **Poisson's Ratio ($\nu_{12}$)**      | **Rule of Mixtures** | $\nu_{12} = V_f \nu_f + V_m \nu_m$                     | Longitudinal                |
| **In-plane Shear Modulus ($G_{12}$)** | **iROM**             | $\frac{1}{G_{12}} = \frac{V_f}{G_f} + \frac{V_m}{G_m}$ | Shear loading               |

