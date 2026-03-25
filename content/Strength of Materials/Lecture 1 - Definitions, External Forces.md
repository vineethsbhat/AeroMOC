---
tags:
  - "#crashcoursesom"
---
In strength of materials, we talk about real solids, and how physical systems respond to the applied load. The applied load can change 3 things,
1. state of motion when the system overcomes inertia (Rigid Body Mechanics)
2. shape change
3. size change

So we are looking at the effect of external force on the system. We are also looking at energy transfer (mechanical energy) and its effect upon physical contact between systems. 

The system can be analyzed when it is at rest/stationary and when it is in motion. In strength of material we restrict ourselves to systems at rest. When the system is in motion, we deal with in ==Vibrations and Dynamics of Mechanical Systems==


>So now we need to ask ourselves, what are the sources of the external forces ?

1. External Forces with physical contact - Surface Forces/Traction [Pressure, Friction, Point Loads, Tension/Compression]
2. External Forces without physical contact - Body Forces - [Gravity, Inertial Forces, Magnetic Forces]

>Load : An external force that needs physical surface contact. Note that friction is a reactive force and thus isn't considered a load despite being external and having surface contact.

>[! Important]
>Sometimes, the line gets blurry. If you have a pipe expanding due to heat and it rubs against its support, that friction creates a force that the support must be strong enough to handle. In that specific context, a designer might call it a "frictional load."


A system of forces can be resolved into an equivalent force or resultant. It is often the case we simplify the forces into its equivalent point load.

### Effect of Force :

Assuming the system is restricted sufficiently, we are interested in the way the shape and size changes for the system. This is more commonly referred to as 'Deformation' or 'Deformable Solids'

When we study deformation, we start with small deformations. Failure of common amenities including buckling of plastic chairs, failure of false ceiling, etc. Failures are often due to design defects, choice of materials, cross-section, and aging. 

We've also heard of spectacular failures, failure of the Tacoma Narrows Bridge Collapse which failed by torsional mode of vibration, led to the development of cross-bracings to support bridges.

Failures have been precipitated by temperature change, [[Ductile-to-Brittle Transition]]. Happens at very low temperatures, which gave rise to [[Fracture Mechanics]]

Failures have also been precipitated by corrosion and fatigue. 


We start with idealizations :
1. All systems are complex and non-linear. Considering of all features is difficult or impossible
2. Mathematical model must account for the physical behaviour
3. Model must be validated through experiments

>Engineering Mechanics is classified as follows :
1. Mechanics of Rigid Bodies - Statics and Dynamics - Kinematics and Kinetics
2. Mechanics of Deformable Bodies - Strength of Materials (make assumptions such that you don't have to solve differential equations), Theory of Elasticity (solve DEs), Theory of Plasticity 
3. Mechanics of Fluids - Ideal Fluid (DEs), Viscous Fluids, Incompressible Fluids, Compressible Fluids


## Rigid Body Mechanics 

- One of the idealizations used in mechanics, where all particles remain at fixed distances from each other irrespective of the forces that act on the body - it does not deform under the action of forces
- Physical actions are also idealized 
- If you look at truss members in transverse loading, the rafters, or purlins are only supported at joints, we designed the truss structures such that even under transverse load, the members themselves saw axial loads and the rafters supported bending.
- Floor beams also take transverse loads and they resist it by bending. 
- We also confined ourselves to slender members. In bridge structures we see that the force system at the joints must concurrent. You have a gusset plate and the members are joined, so none of the members are subjected to bending. 
- We also saw that there are various cross sectional members possible for a truss. The choice is entirely dependent design philosophy. This is the case for axial loaded members. But if bending and torsion is involved the cross-section matters

### Classification of Beams
1. Cantilever
2. Simply Supported
3. Overhang 

Statically Indeterminate - Insufficient from static equations, so we have to bring in deformation to solve the problem.
1. Continuous
2. Propped Cantilever
3. Fixed Beam

>Diagrams in Design
>1. Axial Force Diagram
>2. SFD
>3. BMD
>4. Twisting Moment Diagram

==So we find the maximum values in these diagrams we can find the appropriate cross section of the beams==

Once we start with the idea of deformation, we know there is resistance to deformation. This resistance is termed 'Stress' or the internal force/unit area developed inside a body due to the applied external load. 

>Now we ask the question : What is the variation of stress in these members to resist the external load ?

For a axial loaded member the resistance is uniformly developed all across the cross section. For a beam in bending, the resistance is not uniform the distribution is triangular, with the center having 0 stress and the outer layers having the highest stress. The same with torsion, the inner core is not participating in load sharing. Central core does not take any load. 

>This is exactly why truss members are designed the way they are, every part of the member is contributing to load sharing. Quiet clever in how transverse loads are made to act as axial loads.

>Now consider railway lines which has to resist bending loads, which has cavity and are typically I beams. Thus tons of material was saved. 

#### Can one visualize the stress developed ?
Take a look at [[Photoelasticity]] and how stress is viewed through a polariscope. The colours and fringes correspond to the stress developed in the body. 
Complexity of the stress field changes dramatically when a hole, notch, or any irregularity is introduced. 

Looking back at the idealisations, 
- Small Deformations allow us to work with undeformed configurations of the body
- Material is Homogenous, elastic property of a material remain same at every point. 
- Material is isotropic, elastic property is same along any direction
- Material is an elastic continuum - meaning no defects

## Historical Evolution of Stress Variations in Beams

1. Da Vinci, Galileo, Parent, Mariotte, Coulomb, - took about 400 years! 
2. Da Vinci documented the theory but the document was lost. It was eventually found in 1967
3. Until calculus was developed, mathematical model wasn't formed and Hook's law was not yet figured out
4. Galileo published the solution of a cantilever beam, strength of the material was looked at. He saw that the way the beam was aligned changed how the beam bent under the same load. This was of course due to 'Moment of Inertia' of the cross-section
5. It was not understood how a hollow beam could be stronger than a solid beam.
6. Robert Hooke eventually figured out that most materials when loaded behaved like a spring, wherein the material returned to it's initially position linearly upon the removal of the force.
7. This meant that there was elastic recovery and force was proportional to the displacement. And this formed the basis of Hooke's Law