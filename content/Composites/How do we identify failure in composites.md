---
tags:
  - composites
---
A failure function identifies stress states leading to failure. Failure function (curve) based on stress interactions should represent the critical stress states for multi-axial stress states. 

To distinguish between stress states, the failure criteria is given as :
$$F (\sigma_1, \sigma_2, \sigma_3, \tau_{12} , \tau_{13}, \tau_{23}, X_{t/c}, Y_{t/c}, Z_{t/c}, S_T, S_L) < 1 $$
If, 
< 1 : No Failure
= 1 : Failure Point , > 1 : Failure

The value of $F$ is commonly referred to as ['Failure Index'], it is a non-linear function applied to the load. Since this is the case, with a $F = 0.5$ the structural load can't be doubled before reaching the failure. Since  $F (0.5 \times 2) = 1$ which is the [Failure Point]

### [Example of Failure Index using Tsai-Wu (2D) criteria]
The equation as we'll see is given as, 
$$
\text{Tsai-Wu Failure Index (2D Plane Stress)}
$$

$$
F(\sigma_1, \sigma_2, \tau_{12}, X_{t/c}, Y_{t/c}, S_L) = f_1 \sigma_1 + f_2 \sigma_2 + f_{11} \sigma_1^2 + f_{22} \sigma_2^2 + 2 f_{12} \sigma_1 \sigma_2 + f_{66} \tau_{12}^2
$$

$$
\text{Failure occurs when: } FI \ge 1
$$

$$
\text{The failure envelope (boundary) is defined by the intersection plane:}
$$

$$
\{ FI = 1 \}
$$



```tikz
\begin{document}
\begin{tikzpicture} 
   \draw[->] (-3,0) -- (4,0) node[right] {$\sigma_1$}; 
   \draw[->] (0,-2) -- (0,3) node[above] {$\sigma_2$};
   
   \draw[thick, fill=blue!20, rotate=15] (0.5,0.5) ellipse (3cm and 1.5cm);

   
   \filldraw (3.3,0) circle (2pt) node[anchor=south west] {$X_t$};
   \filldraw (-2.3,0) circle (2pt) node[anchor=south east] {$X_c$};
   \filldraw (0,1.9) circle (2pt) node[anchor=south west] {$Y_t$};
   \filldraw (0,-0.9) circle (2pt) node[anchor=north west] {$Y_c$};
   \node at (0,-2.5) {\textbf{Tsai-Wu Failure Function (2D)}};
\end{tikzpicture}
\end{document}
```


Note that failure index does not give us the risk of fracture, so we need a way to define that. Because you have unequal stresses in the laminate, it is better to talk of failure in terms of 'risk of fracture' or 'risk of failure' on the lamina and laminate level. 

Hence we define ==Stress Exposure== ($f_E$) for the lamina level, it helps us visualize the failure envelope which basically gives us where the intersection is happening with the z-axis (failure index axis)

It is defined as :
$$f_E = \frac{\text{length of actaul stress vector} \space (\sigma)}{\text{length of the stress vector leading to fracture} \space (\sigma_{fr)}} $$
$$f_E = \frac{ |\sigma_r |}{|\sigma_{fr}|}$$
[It basically tells us how much the loading can be increased until the failure index equals 1]

---
[[Failure Index vs. Stress Exposure and how it connects]]

