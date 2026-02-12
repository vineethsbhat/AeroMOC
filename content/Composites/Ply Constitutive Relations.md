---
tags:
  - composites
---
From CLT we now have,

$$\sigma_k = [\bar Q] \cdot \epsilon_k$$
$$\sigma_k = [\bar Q] \cdot (\epsilon^0 + {k} \cdot z_k ) $$
$\bar Q$  is the stiffness matrix in the global CS

>Note that the orientation of the z-axis is downward facing and thus the $z$ values are positive below the mid plane and negative above the mid plane

# [ABD Matrix]

Now, the mathematical step of summing up all the stresses in every layer to find the total force and moment on the laminate
$$
\{n\} = \sum_{k=1}^{N} \int_{z_{k-1}}^{z_k} [\overline{Q}]_k \cdot (\{\epsilon^0\} + z \cdot \{\kappa\}) \, dz \tag{1}
$$

$$
\{m\} = \sum_{k=1}^{N} \int_{z_{k-1}}^{z_k} [\overline{Q}]_k \cdot (\{\epsilon^0\} + z \cdot \{\kappa\}) \cdot z \, dz \tag{2}
$$

$$
\text{The constant terms can be shifted in front of the sum / integral:}
$$

$$
\{n\} = \{\epsilon^0\} \cdot \underbrace{\sum_{k=1}^{N} [\overline{Q}]_k \int_{z_{k-1}}^{z_k} dz}_{A} + \{\kappa\} \cdot \underbrace{\sum_{k=1}^{N} [\overline{Q}]_k \int_{z_{k-1}}^{z_k} z \, dz}_{B} \tag{3}
$$

$$
\{m\} = \{\epsilon^0\} \cdot \underbrace{\sum_{k=1}^{N} [\overline{Q}]_k \int_{z_{k-1}}^{z_k} z \, dz}_{B} + \{\kappa\} \cdot \underbrace{\sum_{k=1}^{N} [\overline{Q}]_k \int_{z_{k-1}}^{z_k} z^2 \, dz}_{D} \tag{4}
$$
[How did we get from "stress in a fiber" to "stiffness of a plate"?]

Imagine you want to know the total pulling force ($N$) on a sandwich. You can't just multiply "Average Stress" by "Total Area" because the bread is soft and the meat is tough—they carry different loads.

- **The Math:** You have to look at every tiny slice of thickness ($dz$), calculate the stress in that specific slice, and add them all up.
- **Equation (1):** This is exactly what $\int \sigma \, dz$ represents. It sums the stress across the thickness to get total force.
Now imagine you want to know the bending moment ($M$).

- **The Physics:** Stress at the _top_ of the sandwich creates more leverage (bending power) than stress in the _middle_.
- **The Math:** You take that same stress, multiply it by its distance from the center ($z$), and then sum it up.
- **Equation (2):** This is $\int \sigma \cdot z \, dz$. The extra $z$ is the "lever arm."

>Since composites are made of discrete layers (plies) rather than a smooth gradient, we don't need a complex calculus integral. We can just do a simple summation ($\Sigma$) for each layer.

- **Matrix A (Extensional Stiffness):** You just add up the stiffness ($Q$) of every layer multiplied by its thickness. It’s like adding up the strength of every sheet of paper in a stack.

- **Matrix B (Coupling Stiffness):** This measures asymmetry. If you have strong layers on top and weak layers on the bottom, this value becomes non-zero. It means if you pull the plate, it will curl up.

- **Matrix D (Bending Stiffness):** This is the "Parallel Axis Theorem" applied to stiffness. It calculates how hard it is to bend the stack based on how far the stiff layers are from the center.

> _Note:_ The term $t_k^3/12$ is the stiffness of the layer rotating about its _own_ axis.
  _Note:_ The term $t_k \cdot (z)^2$ is the stiffness of the layer rotating about the _laminate's_ axis (Parallel Axis Theorem).

$$
\begin{Bmatrix}
n_x \\ n_y \\ n_{xy} \\
m_x \\ m_y \\ m_{xy}
\end{Bmatrix}
=
\begin{bmatrix}
A_{11} & A_{12} & A_{16} & B_{11} & B_{12} & B_{16} \\
A_{12} & A_{22} & A_{26} & B_{12} & B_{22} & B_{26} \\
A_{16} & A_{26} & A_{66} & B_{16} & B_{26} & B_{66} \\
\hline
B_{11} & B_{12} & B_{16} & D_{11} & D_{12} & D_{16} \\
B_{12} & B_{22} & B_{26} & D_{12} & D_{22} & D_{26} \\
B_{16} & B_{26} & B_{66} & D_{16} & D_{26} & D_{66}
\end{bmatrix}
\cdot
\begin{Bmatrix}
\epsilon_x^0 \\ \epsilon_y^0 \\ \gamma_{xy}^0 \\
\kappa_x \\ \kappa_y \\ \kappa_{xy}
\end{Bmatrix}
$$

$$
[A] = \sum_{k=1}^{n} [\overline{Q}_k] \cdot t_k
$$

$$
[B] = \sum_{k=1}^{n} [\overline{Q}_k] \cdot t_k \cdot \left( z_k - \frac{t_k}{2} \right)
$$

$$
[D] = \sum_{k=1}^{n} [\overline{Q}_k] \cdot \left( \frac{t_k^3}{12} + t_k \cdot \left( z_k - \frac{t_k}{2} \right)^2 \right)
$$

$$
\text{Where: } t_k = \text{thickness of layer } k, \quad z_k = \text{vertical coordinate of layer interface}
$$
---
Read Also : [[How Global Stiffness Matrix is Assembled in FEA]] , [[Sub-Matrices of ABD Matrix]], [[What does ABD Matrix really tells us]], [[Key Takeaways from ABD Matrix]]


