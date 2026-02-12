---
tags:
  - composites
---
Imagine the layers are stacked in a way that isn't lining up with the global CS, this would inherently make the analysis and understanding of the interaction even more complex. 

>1,2 = Local CS
>x, y = Global CS

If you look at the transformation stresses in aerospace structures, we are essentially doing the same thing here to understand the behaviour locally. For example, stress on an inclined plane could be $$\sigma_1 = \sigma_x \cdot cos^2(\theta)$$
So we get the transformation matrix as,
$${\sigma_{12}} = [T] \sigma_{xy}$$
and,
$$\sigma_{xy} = [T]^{-1} \cdot \sigma_{12}$$
For strain you need the [Reuter Matrix] to be included in the transformation so we handle shear strains properly when transforming between CS

$$\epsilon_{xy} = [R] \cdot [T]^{-1} \cdot [R]^{-1}$$
This is what the workflow looks like :

1. We start with the known load and beam geometry, local stiffness matrix based on the layers and direction we are using them in
2. Use beam theory to find the global strain 
3. Transform global strain to local strain using transformation matrix and the [Reuter Matrix]
4. Calculate local lamina level stresses using local $[Q]$ and now known local strain
5. Transform the local lamina level stresses to global using transformation matrix times the local stresses
6. Note : Here we are not yet dealing with curvature, that comes into play when you talk about laminates and use part of beam theory to construct [[Classical Laminate Theory]]


---
Read Also : [[Classical Laminate Theory]] , [[Stress on an Inclined Plane]] 