---
tags:
  - composites
---
The laminate behaviour in composite macromechanics is understood using a combination of beam and plate theory.

>**Classical Laminate Theory (CLT)** is essentially the "User Manual" for calculating the strength and stiffness of a complete composite stack. It takes the properties of individual layers and combines them in a way to help us understand how the entire stack is behaving.

>It acts as the bridge between the simple material properties of a single ply and the complex structural behavior of a finished part.

Generally represented as,
$$\begin{Bmatrix} N \\ M \end{Bmatrix} = \begin{bmatrix} A & B \\ B & D \end{bmatrix} \begin{Bmatrix} \epsilon^0 \\ \kappa \end{Bmatrix}$$
Relating the force and moments to the strain and curvature through the stiffness matrix called ==ABD Matrix==
To apply the theory of beams and plates from solid mechanics there are a few assumptions that have to be made since we are dealing with a heterogenous and anisotropic material and these are :

>We are keeping the same geometric assumptions as [Kirchhoff-Love Plate Theory] but allows the material properties ($Q_{ij}$) to change from layer to layer and direction to direction



>[!Important]
>1. The layers are perfectly bonded, it is a practical constraint of manufacturing 
>2. Straight lines perpendicular to the middle surface remain straight and perpendicular to the middle surface after deformation. ["We are ignoring the sliding (shear) between layers. We assume the beam is thin enough that it bends perfectly without any 'squishiness' in the thickness direction."] ($\gamma_{xz} = \gamma_{yz} = 0$)
>3. The thickness is assumed to remain constant. he plate doesn't get thinner or thicker (thickness strain $\epsilon_z = 0$)
>4. **Small Deflections:** The plate doesn't bend so much that it stretches significantly just from the geometry of the curve.

CLT requires the material is linear elastic in nature or we are dealing with the linear-elastic region and that the laminates are thin enough.

## Kinematic Relations :

Using the Kirchhoff plate hypothesis and applying the plate theory we get the following kinematic relations which gives the deflection of some point "c" at the end face of the plate as a function of mid point "B" moved by a distance of "$u_0$" and point "c" from point "B" in the x-axis, where $z_c$ is the distance from point "B" to point "c" on the edge
$$u_c = u_{0} - z_c \cdot 
\frac{\partial w_0}{\partial x}$$
For y axis,

$$v_c = v_{0} - z_c \cdot 
\frac{\partial w_0}{\partial y}$$
where, $w_0$ is the displacement of point B over the z-axis and $\tan \beta = \frac{\partial w_0}{\partial x}$ and since $\beta$ is small, $\tan \beta \approx \beta$

>Key Kinematic Relationship :

1. Displacement in $x$ and $y$ 

$$
u = u_0 - z \frac{\partial w_0}{\partial x} \tag{1}
$$

$$
v = v_0 - z \frac{\partial w_0}{\partial y} \tag{2}
$$



2. We know from [[Strain-Displacement Relationship]]
$$
\epsilon_x = \frac{\partial u}{\partial x}, \quad 
\epsilon_y = \frac{\partial v}{\partial y}, \quad 
\gamma_{xy} = \frac{\partial u}{\partial y} + \frac{\partial v}{\partial x} \tag{3}
$$
3. The master kinematic equation then becomes :
$$
\begin{Bmatrix} 
\epsilon_x \\ 
\epsilon_y \\ 
\gamma_{xy} 
\end{Bmatrix} 
= 
\underbrace{
\begin{Bmatrix} 
\frac{\partial u_0}{\partial x} \\ 
\frac{\partial v_0}{\partial y} \\ 
\frac{\partial u_0}{\partial y} + \frac{\partial v_0}{\partial x} 
\end{Bmatrix}
}_{\{\epsilon^0\}}
- z \cdot 
\underbrace{
\begin{Bmatrix} 
\frac{\partial^2 w_0}{\partial x^2} \\ 
\frac{\partial^2 w_0}{\partial y^2} \\ 
2 \frac{\partial^2 w_0}{\partial x \partial y} 
\end{Bmatrix}
}_{\{\kappa\}}
\tag{4}
$$
>The simplified vector form used in CLT is :

$$
\{\epsilon\} = \{\epsilon^0\} + z \cdot \{\kappa\} \tag{5}
$$
Where :

$$
\{\epsilon\} = \text{Strain in the laminate}
$$
$$
\{\epsilon^0\} = \text{Mid-surface strain}
$$
$$
z = \text{Lever arm (distance from mid-plane)}
$$
$$
\{\kappa\} = \text{Mid-surface curvature}
$$
[Please Refer to Laminate Strain Distribution on Ch.2-Pg. 89]

Up Next : [[Ply Constitutive Relations]]

---
Read Also :