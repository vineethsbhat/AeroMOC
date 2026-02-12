---
tags:
  - composites
---
### [Key Issue :]

The central problem in composites is anisotropy. Unlike steel (isotropic), which yields the same way no matter how you pull it, a composite is strong in one direction (fibers) and weak in another (matrix). The different theories attempt to capture this complexity with varying degrees of fidelity.

### The Classification 

The classification is based on whether the stress in one direction interacts with stress developed in another direction and thus they are classified as :
1. Independent : Do not interact with each other - ==No interaction between different stress/strain components. The failure mode can be predicted. Failure analysis is often not conservative==
2. Interactive : Interact with each other and influence behaviour
	1. Partial - ==The Failure Function is represented by different equations. Hence, these criteria allow a distinction between different failure modes (e.g. fiber or matrix failure / tension or compression) and a physically plausible interaction of different stresses==

	2. Fully Interactive - ==All the different stresses are combined in a single equation. The failure mode cannot be predicted==

==Independent Criteria==
**Concept:** Failure in one direction is completely unaffected by stress in another direction. If you pull a fiber until it breaks, it doesn't matter if you are also squeezing the matrix sideways. 

**Why the distinction?**
It assumes failure mechanisms are uncoupled. It is mathematically simple (a box shape in stress space) but physically often inaccurate because combined loads _do_ often weaken the material faster.

==Fully Interactive==
**Concept:** All stress components ($\sigma_1, \sigma_2, \tau_{12}$) contribute to a single failure event. A small shear stress might reduce the tensile strength significantly. 

**Why the distinction?** 
These use polynomial equations (like ellipses) to "curve fit" experimental data. They capture the interaction well but lose the "why." They tell you the part failed, but not if the fiber broke or the matrix cracked.

==Partial Interactive==
**Concept:** A middle ground. They recognize that fibers and matrix fail differently. They allow interaction _within_ a failure mode (e.g., matrix failure is caused by a mix of transverse stress and shear), but they keep the modes separate (e.g., fiber tension is not affected by matrix shear).

**Why the distinction?** 
This is the modern standard (Hashin, Puck). It provides accuracy _and_ physical insight.

---
