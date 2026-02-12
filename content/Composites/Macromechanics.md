---
tags:
  - composites
---
The goal in Macromechanics is to understand how a lamina and laminate behaves under applied load.

A few assumptions have to be made :
1. Averaged material behaviour (smeared approach) of fiber and matrix
2. Linear elastic behaviour 
3. No detailed investigation of fiber and matrix

A few mechanical assumptions are also made :
1. Small deformations (linear)
2. Linear Elastic Behaviour
3. Thin laminate ($t << l, w$)

==There are different kinds of fiber architecture that can be used for lamina but we restrict ourselves to UD lamina==
For a thin UD lamina [plane stress] assumption is valid. This is not merely an assumption it is an objective because the lamina has to be loaded in plane where the fibers can withstand high stresses. e.g., thin panels include fuselage panels
We have Stress-Strain Relationship as,
$$
\begin{Bmatrix} 
\epsilon_1 \\ 
\epsilon_2 \\ 
\epsilon_3 \\ 
\gamma_{23} \\ 
\gamma_{31} \\ 
\gamma_{12} 
\end{Bmatrix} 
= 
\begin{bmatrix} 
S_{11} & S_{12} & S_{13} & 0 & 0 & 0 \\ 
S_{12} & S_{22} & S_{23} & 0 & 0 & 0 \\ 
S_{13} & S_{23} & S_{33} & 0 & 0 & 0 \\ 
0 & 0 & 0 & S_{44} & 0 & 0 \\ 
0 & 0 & 0 & 0 & S_{55} & 0 \\ 
0 & 0 & 0 & 0 & 0 & S_{66} 
\end{bmatrix} 
\cdot 
\begin{Bmatrix} 
\sigma_1 \\ 
\sigma_2 \\ 
\sigma_3 \\ 
\tau_{23} \\ 
\tau_{31} \\ 
\tau_{12} 
\end{Bmatrix}
$$
Reduced matrix due to plane stress condition gives us :
$$
\begin{Bmatrix} 
\epsilon_1 \\ 
\epsilon_2 \\ 
\gamma_{12} 
\end{Bmatrix} 
= 
\begin{bmatrix} 
S_{11} & S_{12} & 0 \\ 
S_{12} & S_{22} & 0 \\ 
0 & 0 & S_{66} 
\end{bmatrix} 
\cdot 
\begin{Bmatrix} 
\sigma_1 \\ 
\sigma_2 \\ 
\tau_{12} 
\end{Bmatrix}
$$

$$
\text{Where the compliance terms are:}
$$

$$
S_{11} = \frac{1}{E_1}, \quad 
S_{22} = \frac{1}{E_2}, \quad 
S_{66} = \frac{1}{G_{12}}
$$

$$
S_{12} = -\frac{\nu_{12}}{E_1} = -\frac{\nu_{21}}{E_2}
$$
For the stiffness matrix,
$$
\begin{Bmatrix} 
\sigma_1 \\ 
\sigma_2 \\ 
\tau_{12} 
\end{Bmatrix} 
= 
\begin{bmatrix} 
Q_{11} & Q_{12} & 0 \\ 
Q_{12} & Q_{22} & 0 \\ 
0 & 0 & Q_{66} 
\end{bmatrix} 
\cdot 
\begin{Bmatrix} 
\epsilon_1 \\ 
\epsilon_2 \\ 
\gamma_{12} 
\end{Bmatrix}
$$

$$
\text{Stiffness terms (Reduced Stiffness } Q_{ij} \text{):}
$$

$$
Q_{11} = \frac{E_1}{1-\nu_{12}\nu_{21}}
$$

$$
Q_{22} = \frac{E_2}{1-\nu_{12}\nu_{21}}
$$

$$
Q_{12} = \frac{\nu_{12}E_2}{1-\nu_{12}\nu_{21}} = \frac{\nu_{21}E_1}{1-\nu_{12}\nu_{21}}
$$

$$
Q_{66} = G_{12}
$$
For stress in direction 1 :
$$
\sigma_1 = \frac{E_1}{1-\nu_{21}\nu_{12}} \cdot \epsilon_1^{(b)}
$$
Where $\epsilon_1^{(b)}$ is technically a vector consisting of strain in direction 1 due to stress in direction 1 and strain in direction 2 due to stress in direction 1 ([Poisson's Effect])

To achieve a uniaxial strain a strain in the opposite direction has to be applied laterally, this is done via a biaxial state of stress and when you do this, the vector that was $\epsilon_1^{(b)}$ does not exist, only strain in the direction 1.

==''Please remember that there is an underlying assumption to always get directional equations is you assume you're holding the material so it can't contract in the other directions''== 

---
Read Also : [[Off Axis Loading - What happens and Why co-ordinate system is the culprit]]
