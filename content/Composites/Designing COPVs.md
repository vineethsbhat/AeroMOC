---
tags:
  - composites
---
The design must focus on the liner, overwrap and the interaction between the two. Generally, COPV liner can be made of 
1. Soft aluminium with minimal load sharing capability
High Load Sharing :
2. High strength steel 
3. Inconel
4. Titanium
5. Cryogenically formed SS liner 

We should ideally go for ductile material. The pressure vessel liner and the dispensing head move in a way as to wrap the liner a desired pattern. If the vessel is cylindrical the fiber winding is done in both longitudinal (helical) and circumferential (hoop) directions with more fibers in hoop direction due to hoop stress.

There are a few major things to keep in mind :
1. Resin Content
2. Fiber Configuration
3. Winding Tension
4. Pattern of overwrap 

### [Autofrettage :]

1. Following post cure inspection, the pressure vessel may be autofrettaged to improve structural performance. ==It is the process where the COPV is pressurized above liner yield strength so that the liner deforms plastically and expands==
2. The liner now is permanently expanded so that when it is depressurized there is tensile stress on the fiber composite and a compressive stress on the liner. This residual strain/stress in the liner improves cycle life performance of the liner, [Fatigue Life]
3. The thermal expansion coefficient of the composite system is typically an order of magnitude lower than the liner. The liner does expand by some margin, after it cools down this induces stress between the liner and the overwrap. So you can have a bond that makes sure the overwrap and the liner shrink together.
4. If not gaps can form between composite and liner. ==The composite typically has a limit of 1.4 % strain compared to liner==

[But why does this improve fatigue life performance ?]
1. The compressive stress exists in the liner, so then next time I pressurize the vessel, there in some compressive stress that I need to overcome to for the liner to feel tension, so this means, net lower stress as a result of already having compressive stress. 
2. Composite stress-strain behaviour is linear. 



## [First Order Sizing in COPVs]

1. MEOP (Max. expected operating pressure) and pressure life (how long its going sit at that pressure and how many cycles (how many times is it going to be pressurized))
2. Fluid ($He/N_2/O_2/H_2$) temperature range, and compatibility 
3. Volume (diameter, length, boss features)
4. Mass target (burst factor, proof factor, leak-before burst, damage tolerance)
5. L**ife drivers**: cycles + sustained pressure time (stress rupture is huge in space COPVs)

---
Vocab : MEOP, MDP (Max. Design Pressure - it includes worst case scenario in terms of temperature, relief, etc), Proof and Burst pressure are derived from MEOP and MDP

## Thin walled pressure vessels
For a **thin-walled closed-end cylinder** (radius $r$, thickness $t$, internal pressure $p$)
$$\sigma_{\theta} \approx \frac{pr}{t}$$
$$\sigma_{z} \approx \frac{pr}{2t}$$
**Meaning:** pressure tries to split the cylinder in half; the wall carries that as membrane tension. Hoop is ~2× axial because pressure acts on the endcap area.
Spheres are more efficient than cylinders (lower membrane stress for same (radius $r$, thickness $t$, internal pressure $p$) thus,

$$\sigma_{z} \approx \frac{pr}{2t}$$
Using membrane forces is much more efficient :
$$N_{\theta} = pr$$
$$N_z = \frac{pr}{2}$$
[Netting Analysis :]
1. Assume fibers carry the load. If fiber is aligned at an angle $\alpha$ to the cylinder axis ($\alpha = 0$ for axial and $90$ for hoop)
$$\tan^2 \alpha = \frac{N_{\theta}}{N_z} = 2 $$
$$\alpha \approx 54.7 \degree$$
This is what's called the magic angle. It shows up constantly in filament wound pressure vessels. 

>**Intuition:** the winding angle sets how much of the fiber tension goes into hoop vs axial load. The vessel _needs_ 2:1 hoop:axial, so the “most efficient” pure-helical design hits that ratio.


Required fiber thickness :
$$N_{\theta} = \sigma_{f,allow} \cdot t_f \cdot sin^2 \alpha$$

$$N_z = \sigma_{f,allow} \cdot t_f \cdot cos^2 \alpha$$
We pick an allowable fiber stress given from ultimate, standards or company allowables and find what the thickness should be of the fiber. Solve for $t_f$ and then use this formula to find composite thickness

$$t \approx \frac{t_f}{V_f \cdot \eta}$$
$\eta$ is the efficiency factor based on (knockdown, voids, waviness, and cure effect)

**Meaning of the equation:** you’re equating “required membrane load” to “what the fibers can carry projected into that direction.”

>[!Important]
>1. We don't use 55 $\degree$ everywhere because cylinder likes hoop layers to handle hoop efficiently. 
>2. Dome requires a change of angle because it should be covered with no voids or gaps (isotensoid dome)
>3. The boss region requires some form of local reinforcement
>4. In reality its a mix of circumferential hoops and helical wrap for the domes





---
[[Failure Modes in COPVs]] 
