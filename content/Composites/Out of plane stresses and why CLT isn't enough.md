---
tags:
  - composites
---
As seen earlier in [[Classical Laminate Theory]] , it is incredible for initial composite design. It assumes the laminate is very thin and behaves like a 2D plane state. The reason this is the case is because it is based on [Kirchhoff-Plate Theory] - 

>It assumes the laminate is so thin compared to its width and length that any stress trying to pull the layers apart (up/down) or slide them over each other (shear through the thickness) is negligible.

In the real world, composites are actually 3D structures. The matrix (resin) holding the layers together is the weak link. While fibers are strong in the plane ($x, y$), the resin is weak out-of-plane ($z$). Ignoring these stresses is usually fine for thin, flat sheets, but it becomes dangerous for thick parts, curved parts, or edges.

In the context of out of plane stresses we have :
1. [ILSS (Interlaminar Shear Stress)] - Also more commonly called as Transverse Shear Stress ($\tau_{xz}, \tau_{yz}$). Imagine taking a deck of cards and bending them, the individual cards slide past each other at the edges. In a composite, the layers are "glued" together by resin. When you bend the composite, the layers _want_ to slide like the cards, but the resin stops them. This resulting force is ==is the force of the resin fighting that sliding motion==. Now if the bending is too sharp, the shear stress overcomes the resin's strength, and the laminate splits in half (delamination).

2. [Normal Stresses] - Through-thickness normal stress ($\sigma_z$) : This is the force directly pulling the layers apart (tension) or crushing them together (compression). Imagine trying to peel a piece of tape off a table by pulling it straight up. In a laminate, this pulls the fibers away from the resin. Since there are no fibers running vertically to take this load, the resin must take it all. This is the primary driver of delamination. 

3. [Curved Beam Effect (Stress at a Radius)] - Imagine you have a composite part with a corner or a curve (like an L-bracket). Now try to pull the ends apart to straighten it, the physics of the curve creates a radial stress component. This creates a strong **tensile normal stress ($\sigma_z$)** right at the elbow (the radius). It is trying to rip the layers apart radially. ==Because there are no fibers running radially to hold the layers together, curved composite parts often fail suddenly at the radius by delaminating==

4. [Free Edge Effect] : This occurs at the physical edge of a laminate where you have cut it. Imagine two layers of rubber glued together. You stretch them. One layer wants to shrink sideways a lot (high Poisson's ratio), and the other doesn't want to shrink much. In the middle of the sheet, they constrain each other. But at the **free edge**, there is nothing holding them back from the outside. This mismatch creates a sudden spike in stress at the very edge as one layer tries to curl up or pull away from the other. This creates a concentration of shear and normal stresses ($\sigma_z$) at the edge, causing the laminate to peel open like a banana, starting exactly at the cut edge.

5. [Ply Drop Off] : You need a part to be thick at one end and thin at the other, so you stop some ply layers halfway through. Think of water flowing down a smooth river channel. If you suddenly put a large step or ledge in the bottom, the water becomes turbulent. In a similar way, the load flows like water through the fibers and the layers, when there is a sudden stop or drop the load needs to jump into the next layer or ply. This creates a [resin-rich pocket] and a massive stress concentration ($\sigma_z$ and $\tau_{xz}$) at the tip of the drop-off. ==The load "jumping" creates a peeling force that tries to start a crack right where the ply end==

For Reference :

| **Phenomenon**    | **What's happening intuitively?**                                   | **Critical Stress Component**    |
| ----------------- | ------------------------------------------------------------------- | -------------------------------- |
| **ILSS**          | Layers trying to slide past each other during bending.              | $\tau_{xz}, \tau_{yz}$ (Shear)   |
| **Normal Stress** | Layers being pulled straight apart.                                 | $\sigma_z$ (Tension)             |
| **Radius Stress** | A curved part trying to straighten out creates radial tension.      | $\sigma_r$ (which is $\sigma_z$) |
| **Free Edge**     | Mismatch in "shrinking" between layers creates peeling at the edge. | $\sigma_z$ and $\tau_{yz}$       |
| **Ply Drop**      | Load has to "jump" layers where one ends, causing turbulence.       | $\sigma_z$ and $\tau_{xz}$       |
