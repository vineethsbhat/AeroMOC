---
tags:
  - composites
---
As we know in isotropic linear elastic material, we have only two independent engineering constants. Any two of $E, G, \mu$ which are related by the equation
$$E = 2G (1 + \mu)$$
- Laminated composite material properties are modelled as orthotropic materials
- Thus we need 9 independent constants. But the standard coupon tests that we perform in lab measures only 4 of the 9 constants ($E1,E2,G12, \mu_{12}$)
- Thin plates, including most laminated composites are generally considered to be in 'Plane Stress' due to the thickness being much smaller than width and length dimension

## The CLT Workflow :

1. Standard coupon tests (UD fibers + matrix) gives us $E1,E2, G12, \mu_{12}$
2. This then allows us to form the stiffness matrix of a single layer
3. This then can be transformed into stiffness for each layer considering the ply angle
4. Now we form the ABD matrix for the entire laminate which relates normal forces and moments with the corresponding mid plane strains and curvatures (derived from Kirchhoff plate hypothesis) 
5. Once we have the strains at the lamina level in global CS, we transform this into strains at the lamina level in local ply level CS
6. This then allows us to figure out the stresses at each layer in the local CS
7. If needed transform the stress into global CS
8. Apply a failure criteria and see if the lamina fails

For an anisotropic material, the 21 independent engineering constants that define the anisotropic stiffness matrix are determined by placing a specimen of material under 6 different strain boundary conditions within the linear elastic regime. 

