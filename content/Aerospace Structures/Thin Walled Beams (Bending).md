---
tags:
  - structures
dg-publish: false
---
## [Loads in Beams]

Things to be considered :
1. Bending Moment 
2. Shear Forces
3. Torsion 
4. Axial Forces/Loads 

All of them have a particular stress associated with the kind of loading. The loads themselves can be derived from statics but for the stresses we need the beam dimensions and how the material is distributed

[Wing root relief is given for +g in flight conditions where the wing bends upwards and thus moving the engine to the tip offers wing root relief. Note the shear force will remain same because we haven't change the mass, only the location of the point load (engine)]

==Wing Relief (inertia relief) refers to the reduction in the shear force and bending moment that results from including inertia forces (mass * acc. * load factor) of the wing structure, fuel, and wing mounted engines==

Fun Fact : In a Boeing 787 the wing tip bends by about 12ft. relative to the cabin floor. 

### How do we find stresses due to bending :
1. Pick position on beam where you want to find the stresses
2. Define the section(dimensions/type of cross-section)
3. Find the centroid of the section
4. Find the second moment area relative that centroid (MOI) [Ixx, Iyy, Ixy]
5. Calculate stresses using beam theory $\sigma = \frac{M \cdot y}{I_{xx}}$ (simplest form)
6. Calculate max. and min. stress

[But why do we need a centroid ?]
It tells us where the neutral axis is going to be, i.e., when the beam bends it tells us which part of the beam is not experiencing any strain. We can have multiple neutral axis in some cases and they all go through the CG.

Definition of centroid is based on first moment of area :
Which gives the measure of distribution of mass relative to an axis
$$M_x = \int y \cdot dA$$
$$M_y = \int x \cdot dA$$
So therefore, centroid is the point about which the first moment of area is zero for any orthogonal axis system. [Center of the Area]
Given by, for any arbitrary set of CS 
$$\bar x = \frac{\int x dA}{\int dA} = \frac{\sum x dA}{\sum dA}$$
$$\bar y = \frac{\int y dA}{\int dA} = \frac{\sum y dA}{\sum dA}$$
 It's used to understand how far the material is away from the N-A

[What is Second Moment of Area and why do we need it ?]
