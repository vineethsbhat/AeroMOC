---
tags:
  - composites
---
$$
\begin{bmatrix}
A_{11} & \bbox[#C3B1E1]{A_{12}} & \bbox[#FDFD96]{A_{16}} & \bbox[#77DD77]{B_{11}} & \bbox[#77DD77]{B_{12}} & \bbox[#FF6961]{B_{16}} \\
\bbox[#C3B1E1]{A_{12}} & A_{22} & \bbox[#FDFD96]{A_{26}} & \bbox[#77DD77]{B_{12}} & \bbox[#77DD77]{B_{22}} & \bbox[#FF6961]{B_{26}} \\
\bbox[#FDFD96]{A_{16}} & \bbox[#FDFD96]{A_{26}} & A_{66} & \bbox[#FF6961]{B_{16}} & \bbox[#FF6961]{B_{26}} & \bbox[#D3D3D3]{B_{66}} \\
\hline
\bbox[#77DD77]{B_{11}} & \bbox[#77DD77]{B_{12}} & \bbox[#FF6961]{B_{16}} & D_{11} & \bbox[#AEC6CF]{D_{12}} & \bbox[#FFB347]{D_{16}} \\
\bbox[#77DD77]{B_{12}} & \bbox[#77DD77]{B_{22}} & \bbox[#FF6961]{B_{26}} & \bbox[#AEC6CF]{D_{12}} & D_{22} & \bbox[#FFB347]{D_{26}} \\
\bbox[#FF6961]{B_{16}} & \bbox[#FF6961]{B_{26}} & \bbox[#D3D3D3]{B_{66}} & \bbox[#FFB347]{D_{16}} & \bbox[#FFB347]{D_{26}} & D_{66}
\end{bmatrix}
$$
- **Purple ($A_{12}$):** Poisson Extension Coupling (Poisson's Ratio effects).
- **Yellow ($A_{16}, A_{26}$):** Extension-Shear Coupling (Skew).
- **Green ($B_{11}, B_{12}, B_{22}$):** Extension-Bending Coupling (Bimetallic strip effect).
- **Red ($B_{16}, B_{26}$):** Extension-Twist Coupling (Corkscrew effect).
- **Grey ($B_{66}$):** Shear-Twist Coupling.
- **Blue ($D_{12}$):** Anticlastic Bending (Saddle shape).
- **Orange ($D_{16}, D_{26}$):** Bending-Twist Coupling (Propeller effect).

### Extension-Extension Coupling :
Extending the laminate will lead to the material contracting in the lateral direction, the direct poisson's effect is captured by this.

### Extension-Shear Coupling :
$$
\text{Calculation of the shear force } n_{xy} \text{ on the middle surface:}
$$

$$
n_{xy} = \int_{-t/2}^{t/2} \tau_{xy} \cdot dz = \int_{-t/2}^{t/2} \epsilon_x \cdot \overline{Q}_{16} \cdot dz = \epsilon_x \cdot \underbrace{\overline{Q}_{16} \cdot t}_{A_{16}}
$$


Conditions for Zero Coupling
$$\text{1. For } \alpha = 0^\circ \text{ or } 90^\circ, \quad \overline{Q}_{16} \text{ becomes } 0 \implies A_{16} = 0
$$
$$
\text{2. If a second ply with } -\alpha \text{ is added (balanced laminate),}
$$
$$
\text{an opposing shear force } -n_{xy} \text{ is induced} \implies A_{16} = 0
$$
### Extension-Bending Coupling :
This equation proves mathematically why pulling on an asymmetrical laminate (like a $0^\circ/90^\circ$ stack) causes it to curl.
$$
\text{Calculation of the moment } m_x \text{ at a point on the middle surface:}
$$

$$
m_x = \int_{-t/2}^{t/2} \sigma_x \cdot z \, dz = \sum_{k=1}^{N} \int_{z_{k-1}}^{z_k} \sigma_{x_k} \cdot z \, dz
$$

$$
\text{Substituting Hooke's Law } (\sigma = Q \epsilon) \text{ and assuming constant strain } (\epsilon_x):
$$

$$
m_x = \sum_{k=1}^{N} \int_{z_{k-1}}^{z_k} \epsilon_x \cdot \overline{Q}_{11_k} \cdot z \, dz
$$

$$
\text{Solving the integral for a 2-layer (0/90) laminate:}
$$

$$
m_x = \epsilon_x \cdot \underbrace{\frac{t^2}{8} \cdot \frac{(E_2 - E_1)}{1 - \nu_{12}\nu_{21}}}_{B_{11}}
$$

$$
\text{Conclusion:}
$$
$$
\text{Since } E_2 \neq E_1, \text{ a moment } m_x \text{ is induced } \implies B_{11} \neq 0
$$
### Extension-Torsion Coupling :
This explains why pulling a "Balanced" laminate ($+\alpha / -\alpha$) might still twist like a corkscrew.
$$
\text{Calculation of the torsion moment } m_{xy} \text{ induced by extension } \epsilon_x:
$$

$$
m_{xy} = \int_{-t/2}^{t/2} \tau_{xy} \cdot z \, dz = \sum_{k=1}^{N} \int_{z_{k-1}}^{z_k} \epsilon_x \cdot \overline{Q}_{16_k} \cdot z \, dz
$$

$$
\text{For a balanced laminate } (+\alpha \text{ on top}, -\alpha \text{ on bottom}):
$$

$$
m_{xy} = \epsilon_x \left( \overline{Q}_{16_{+\alpha}} - \overline{Q}_{16_{-\alpha}} \right) \cdot \frac{t^2}{8}
$$

$$
\text{Since } \overline{Q}_{16_{-\alpha}} = -\overline{Q}_{16_{+\alpha}} \text{ (Opposite signs add up):}
$$

$$
m_{xy} = \epsilon_x \cdot \overline{Q}_{16_{+\alpha}} \cdot \frac{t^2}{4} \implies B_{16} \neq 0
$$
- **The Setup:** You have $+45^\circ$ fibers on the top half and $-45^\circ$ fibers on the bottom half.

- **The Pull:** You pull the laminate straight ($\epsilon_x$).

- **The Conflict:** The top layer wants to shear right. The bottom layer wants to shear left.

- **The Twist:** Because these opposing shear forces are separated by the thickness of the plate (lever arm $z$), they act like your hands on a steering wheel—one pushing up, one pulling down. This creates a **Torque** ($m_{xy}$) that twists the plate

### Bending-Bending Coupling :
$$
\text{Calculation of the transverse moment } m_y \text{ induced by curvature } \kappa_x:
$$

$$
m_y = \int_{-t/2}^{t/2} \sigma_y \cdot z \, dz = \int_{-t/2}^{t/2} \kappa_x \cdot z \cdot \overline{Q}_{12} \cdot z \, dz
$$

$$
m_y = \kappa_x \cdot \overline{Q}_{12} \int_{-t/2}^{t/2} z^2 \, dz = \kappa_x \cdot \overline{Q}_{12} \cdot \frac{t^3}{12}
$$

$$
\text{Substituting Material Properties:}
$$

$$
m_y = \kappa_x \cdot \underbrace{\frac{\nu_{12} E_2}{1 - \nu_{12}\nu_{21}} \cdot \frac{t^3}{12}}_{D_{12}}
$$
- **The Setup:** A simple unidirectional plate. You try to bend it into a cylinder ($\kappa_x$).

- **The Physics:** When you bend it, the **Top** is compressed and wants to bulge out sideways (Poisson expansion). The **Bottom** is stretched and wants to shrink sideways (Poisson contraction).

- **The Result:** The top gets wider, the bottom gets narrower. This forces the plate to curl in the opposite direction ($y$-axis), creating a saddle shape. If you force the plate to stay flat ($m_y$), you are fighting this $D_{12}$ stiffness.

### Bending-Torsion Coupling :
This explains why a diving board made of angled ply would twist when you jump on it.
$$
\text{Calculation of torsion moment } m_{xy} \text{ induced by curvature } \kappa_x:
$$

$$
m_{xy} = \int_{-t/2}^{t/2} \tau_{xy} \cdot z \, dz = \int_{-t/2}^{t/2} \overline{Q}_{16} \cdot \epsilon_x \cdot z \, dz
$$

$$
\text{Substituting Strain } \epsilon_x = z \cdot \kappa_x:
$$

$$
m_{xy} = \overline{Q}_{16} \int_{-t/2}^{t/2} \kappa_x \cdot z^2 \, dz = \kappa_x \cdot \underbrace{\overline{Q}_{16} \cdot \frac{t^3}{12}}_{D_{16}}
$$
- **The Setup:** You have angled fibers (e.g., $45^\circ$) throughout the thickness.

- **The Bend:** You bend the plate ($\kappa_x$).

- **The Physics:** The Top layer is compressed, so the $45^\circ$ fibers try to shear one way. The Bottom layer is stretched, so the $45^\circ$ fibers try to shear the **opposite** way.

- **The Result:** Just like in the $B_{16}$ case, you have opposing shear forces at the top and bottom. This torque twists the plate.

### Shear-Torsion Coupling :
This explains why shearing a hybrid laminate can cause it to curl.
$$
\text{Calculation of moment } m_{xy} \text{ induced by shear strain } \gamma_{xy}:
$$

$$
m_{xy} = \int_{-t/2}^{t/2} \tau_{xy} \cdot z \, dz = \sum_{k=1}^{N} \int_{z_{k-1}}^{z_k} \gamma_{xy_k} \cdot \overline{Q}_{66_k} \cdot z \, dz
$$

$$
\text{For a laminate with different materials (e.g., } 0^\circ \text{ and } 45^\circ \text{):}
$$

$$
m_{xy} = \gamma_{xy} \cdot (\overline{Q}_{66_{45^\circ}} - \overline{Q}_{66_{0^\circ}}) \cdot \frac{t^2}{8}
$$

$$
\text{Result:} \quad B_{66} \neq 0
$$
- **The Setup:** A "sandwich" where the top bread is very stiff in shear ($45^\circ$ fibers) and the bottom bread is weak in shear ($0^\circ$ fibers).

- **The Shear:** You try to distort the whole sandwich into a parallelogram ($\gamma_{xy}$).

- **The Imbalance:** The stiff top layer fights back hard (High Stress). The weak bottom layer fights back weakly (Low Stress).

- **The Result:** You have a high force on top and a low force on the bottom. This imbalance creates a moment that twists the panel.

---
Read Also : [[Key Takeaways from ABD Matrix]], [[Failure Behaviour of Composite Structures]]
