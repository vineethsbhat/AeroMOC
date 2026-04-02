---
tags:
  - structures
---
Hooke's Law is given as :

$$\epsilon_x = \frac{1}{E}[\sigma_x - \mu(\sigma_y + \sigma_z)]$$
$$\epsilon_y = \frac{1}{E}[\sigma_y - \mu(\sigma_x + \sigma_z)]$$
$$\epsilon_z = \frac{1}{E}[\sigma_z - \mu(\sigma_y + \sigma_x)]$$

But for shear strain :
$$\gamma_{xy} = \frac{\tau_{xy}}{G}$$
$$\gamma_{xz} = \frac{\tau_{xz}}{G}$$
$$\gamma_{yz} = \frac{\tau_{yz}}{G}$$

To understand why $\mu$ appears explicitly in normal strain but not shear strain, we have to look at what the forces are actually doing to the atoms:

**Normal Strain (ϵ):** When you pull a block (axial load), you are trying to change its **volume**. Because the atoms are bonded together, if you stretch them apart in the x-direction, they naturally pull closer together in the y and z directions to compensate. That "cross-talk" between axes is exactly what Poisson's ratio measures.

**Shear Strain (γ):** Shear is about changing **shape** (distortion), not volume. You are sliding layers of atoms past each other. In a pure shear scenario, the lengths of the sides of the infinitesimal element don't actually change initially; only the **angles** between them do. Since there's no primary "stretching" in one direction to cause a "shrinking" in another, ν doesn't need to act as a scaling factor in the basic $\tau = G \gamma$ equation.

While ν doesn't appear in the _form_ of the shear equation, it is mathematically required to define the relationship between E (stretching stiffness) and G (sliding stiffness).

For an isotropic material, the three constants are linked by this fundamental identity:

$$G = \frac{E}{2(1 + \mu)}$$
>If you plug this G into the shear strain equation you will see,

$$\gamma_{xy} = \frac{\tau_{xy}(2 (1 + \mu))}{E}$$

>Suddenly, Poisson's ratio is back! We just use G as a shorthand because it represents the material's specific resistance to that "sliding" motion, which already accounts for how the material's internal structure handles lateral effects.


>[! Important]
> Why this matters
> This relationship is why you only need **two** independent constants (usually E and ν, or E and G) to fully describe the elastic behavior of an isotropic material. If you know how it stretches (E) and how it shrinks laterally (ν), the universe dictates exactly how it must behave in shear (G).

