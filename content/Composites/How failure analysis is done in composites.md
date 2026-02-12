---
tags:
  - composites
---
A failure criteria allows us to know whether the applied stress state leads to ply failure. It basically covers the first macroscopic failure event that happens within a laminate. The mechanical behaviour post failure is done by something called as ['Degradation Analysis']

First, we need to understand what failure means in our case :
As seen earlier there are many ways in which a composite can fail. For a realistic prediction of how and if failure occurs there are two important things to keep in mind :
1. You should be able to reproduce typical failure modes seen in the composite 
2. Understand how the interaction between material strength and stresses leads to initiation of a certain failure mode

>No one mathematical criteria can predict every mode. And that is not the purpose as well. As seen earlier, we know the stress through the entire laminate is non-uniform. So it is natural to assume failure will not occur everywhere all at once, but rather in the ply where the ratio of applied stress to the strength of the material is max. 

To capture this effect, failure analysis is always done at the ply/lamina level. No doubt the interaction of stresses is complex. 

### [Here's what we do :]

We have the following terms coming out of tests or experiments :
1. Longitudinal Tension/Strength
2. Longitudinal Compression/Strength
3. Transverse Tension and Compressive Strength
4. Transverse Shear Strength

### [Assumptions :]
1. UD lamina shows brittle fracture for fiber fracture and IFF
2. Fiber fracture is caused by normal stresses 
3. IFF is caused by combination of stresses that are not acting parallel to the fiber direction
4. Strength in tension is > compression for both fiber fracture and IFF

> Fiber undulation helps in tension but doesn't under compression
> In transverse compression the matrix behaves as if it has a higher strength because of inner friction and matrix failure under compression is caused by shear.


>[!The Most Important Thing to Remember :]
>1. Failure Index is given by the ellipsoidal equation curve fit from experimental data
>2. RF and Stress Exposure is a way of understanding when the material approaches failure and not just if it fails or not
>3. Max. stress and strain, Tsai-Wu, Tsai-Hill and Hoffman all have a single equation for $F$ that gives interaction between stresses or independent behaviour
>4. Hashin, Puck are partially interactive but they distinguish between failure modes (for e.g saying FF in tension is happening specifically because of $\sigma_1 , \tau_{12}, \tau_{13}$ etc.) and so we get one equation for each of the different ways in which the material can fail. 
>5. The failure envelope is giving this limit in a graphical way. 












---
[[How do we identify failure in composites]]