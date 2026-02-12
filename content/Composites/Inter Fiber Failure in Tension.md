---
tags:
  - composites
---
- IFF is due to :
	- Micro cracks - caused by residual stresses in matrix due to mismatch of thermal expansion factor, matrix shrinking during the curing process
	- Locally increased strain in matrix 

[What is happening ?]

> “Inter-fiber failure (IFF) in tension” is basically matrix / interface cracking between the fibers while the fibers themselves are still mostly intact.

IFF is mainly caused by :
1. Transverse tension ($\sigma_2 > 0$)
2. In-plane shear ($\tau_{12}$)
3. Out of plane shear ($\tau_{13}, \tau_{23}$)
Therefore it is super common in 90 deg plies in tension, off axis plies, multiaxial laminates. Note that the cracks grow in the direction of the fiber/or along the fiber. This leads to damage accumulation, load redistribution, stiffness drops. 

>[!Important]
>This mode is actually a progressive and damage tolerant mode; as in, you get "warning" but it is dangerous because it reduces strength in shear, triggers delamination.
>And even if the global load is tension, individual plies can see lateral loads due to off axis fiber angle etc.

[Note :] This can be a limiting factor for the design if the structure is dimensioned for first-ply-failure

What this means :
It means IFF in tension happens before any of the fibers actually break. So if the design philosophy is (First Ply Failure - _“the structure is considered to have reached its allowable as soon as any one ply meets a failure criterion”_) then IFF is the design limit since the matrix could fail long before the fibers fail in tension or compression, so whatever mode is seen first is the design mode or acts as the design criteria. 

To understand how we know what mode it fails in, we have to apply all the different [[Failure Criteria in Composites]] and see which one gives us the lowest possible load capacity, and then we use that as the design criteria. 



