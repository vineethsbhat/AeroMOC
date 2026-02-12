---
tags:
  - composites
---
#### Calculation procedure for shear stress of a laminated body with varying Young’s modulus through the thickness (method based on the beam-theory for homogeneous bodies)

1. Transformation of the lamina coordinate system (1,2) to the global laminate one (x,y)
2. A reference modulus is introduced (could be either of the moduli $E_a$ or $E_b$  and an equivalent width $b_k^{eq} = \frac{E_k}{E^{ref}} \cdot b$

>The problem of ply-wise varying stiffness and constant width is changed into an imaginary problem with ply-wise varying width and a constant reference Young’s modulus

3. Determine the neutral axis (Axis parallel to the mid-plane with a distance $z_g$, where an applied tensile force results just in an elongation). Where normal force creates on NA a uniform strain. The load if moved to the middle plane needs to be accounted for with a moment.
4. Multiply the [ABD] matrix with the strain vector gives the normal force and moments
5. Use Steiner theorem to find equivalent second moment area $I^{eq}$ 
6. Determination of the equivalent static moment $S^{eq} z$ upto the location of $s$ where ILSS is to be looked at
7. $\tau_{xz} = \frac{q}{I^{eq}} \cdot S^{eq} (z)$ shear stress equation is setup where $q = \frac{F_q}{b}$

>Note : The shear stress is continuous through 𝑧 but has kinks at the locations where the stiffness changes, since the real width 𝑏 is constant. The higher interlaminar shear stress in the stiffer layers result from the higher equivalent width

>[!Important]
>ILSS depends on the change of the in-plane stress $\sigma_x$ along $dx$; the stiffer plies attract  more normal stresses and thereby the change in the normal stresses is higher

### ILSS (Composites vs. Metals)
The area under the shear flux curve is equal to the shear force $F_q$. For isotropic materials the max. shear flux is given as,
$$t_{max} = \frac{3 F_q}{2h}$$
### Remarks :
1. Stiff layers take more shear stress 



---
Read : [[Interlaminar Tensile Stress]] , [[FEM Sub-Modelling for Out-of-plane Stress]], 