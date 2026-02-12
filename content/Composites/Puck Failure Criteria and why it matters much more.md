---
tags:
  - composites
---
**Puck is indeed a mode-dependent criterion** (like Hashin), but it goes much deeper into **Inter-Fiber Failure (IFF)**—which is where the matrix cracks.
The reason Puck uses terms like "Action Plane" and "Mohr-Coulomb" is that he realized **matrix failure is actually a friction problem.** We will look at what all if it means.

To understand Puck, you have to stop thinking of the matrix as a solid block that just snaps. Think of it instead like **soil** or **sand** (which is where the Mohr-Coulomb theory comes from).

Consider this :
**The Physics:** If you push two blocks of concrete together (Compression) and try to slide them past each other (Shear), it is _harder_ to slide them than if you weren't pushing them. This is because friction is contributing to the shear strength. Friction caused by the compressive force. 

>**Mohr-Coulomb Hypothesis:** A material fails (slides/cracks) on a specific plane when the **Shear Stress** on that plane exceeds the **Cohesion** (glue strength) plus the **Friction** caused by the normal pressure.

Equation in general is given by :
$$\tau_{critical} = c + \mu \cdot \sigma_n$$
- $\tau_{critical}$: The shear stress required to break it.
- $c$: The inherent shear strength (Cohesion).
- $\mu \cdot \sigma_n$: The friction boost (Friction coefficient $\times$ Normal clamping force).

>[!Important]
>If you compress a composite laminate perpendicular to the fibers (transverse compression $\sigma_2$), you are "clamping" the matrix cracks shut. This makes the material **stronger** in shear. Theories like Tsai-Wu struggle to capture this "strengthening" effect accurately. Puck relies on it.

In simple theories (Max Stress), we check failure on the X, Y, and Z planes.

In Puck, we acknowledge that the crack might not happen perfectly along the Y-axis. It might happen at an angle, say $37^\circ$ or $52^\circ$, running through the matrix parallel to the fibers.

- **Fracture Plane:** The physical plane where the crack actually forms.
- **Action Plane:** This is the mathematical concept used to find the fracture plane. Since we don't know _which_ angle is the weakest beforehand, Puck's theory mathematically "rotates" a plane around the fiber axis ($\sigma_1$), checking every single angle ($\theta$) from $0^\circ$ to $180^\circ$.

#### [Why does resistance in a action plane matter :]
In the Action Plane (the worst-case angle), the "Resistance" (Strength) is not a constant number from a datasheet (like "Transverse Tensile Strength = 50 MPa"). **The Resistance changes based on the stress state.**

- **Scenario A (Tension):** If the normal stress on the action plane is _Tensile_ (pulling apart), friction is zero. The resistance is just the base strength of the resin.

- **Scenario B (Compression):** If the normal stress on the action plane is _Compressive_ (pushing together), the "internal friction" kicks in. The matrix effectively becomes stronger.
Puck's Innovation:

He realized that the failure curve isn't a simple circle. As you add compression, the material can handle massive amounts of shear before breaking.

- The "Resistance" is calculated dynamically using inclination parameters (often denoted as $p_{\perp \parallel}$ or $p_{\perp \perp}$).
 
 >These $p$ values are effectively slope parameters that describe how much "friction" the material gains as you compress it.

[Inclination Parameter's :]
They define the **slope** (or inclination) of the failure envelope line when you plot it on a graph.
Imagine a graph where:

- **X-axis:** Normal Stress ($\sigma_n$) - Clamping pressure.
- **Y-axis:** Shear Stress ($\tau$) - Sliding force.

If the material followed a simple theory (like Max Stress), the failure line would be **flat**. (e.g., "The glue breaks at 50 MPa, regardless of how hard you press").

In Puck's theory, because of friction, the line **slopes upward**.

- The more you compress (move left on X), the more shear (move up on Y) the material can take.
- **The Slope of this line is $p$.**
- **Steep Slope (High $p$):** The material is very rough; compression adds a _lot_ of strength.
- **Shallow Slope (Low $p$):** The material is slippery; compression helps, but only a little.
#### A. $p_{\perp \parallel}$ (or $p_{21}$ in some codes)

- **Direction:** This is the friction coefficient for shear stresses acting **parallel** to the fibers ($\tau_{21}$).
- **Physical Scenario:** Think of "Mode A" fracture. You are trying to slide the matrix _along_ the length of the fibers.
- **Typical Value:** For CFRP (Carbon Fiber), this is usually around **0.30 - 0.35**.

#### B. $p_{\perp \perp}$ (or $p_{22}$ in some codes)

- **Direction:** This is the friction coefficient for shear stresses acting **perpendicular** to the fibers ($\tau_{22}$).
- **Physical Scenario:** You are trying to slide the matrix _across_ the fibers. The fibers themselves act like obstacles (speed bumps), creating more resistance.
- **Typical Value:** For CFRP, this is often lower, around **0.20 - 0.25** (though it varies by resin type).

==Resistance in the action plane is give by :==
$$R(\theta) = S + p \cdot |\sigma_n(\theta)|$$

Where:

- $R$: The calculated resistance (Strength limit for this specific moment).
- $S$: The base shear strength (from your datasheet).
- $p$: **The Inclination Parameter.**
- $\sigma_n$: The compressive normal stress.
