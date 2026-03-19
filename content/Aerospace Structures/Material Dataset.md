---
tags:
  - structures
---
### 1. Aluminium Alloys : 
Aluminum is the primary structural material for airframes due to its high strength-to-weight ratio and ease of fabrication.

|**Material**|**Key Property**|**Common Aerospace Use**|
|---|---|---|
|**Al 2024-T3**|High Fatigue Resistance|Fuselage skins, tension members.|
|**Al 7075-T6**|Very High Yield Strength|Wing spars, ribs, compression members.|
|**Al 6061-T6**|Weldable / Corrosion Resistant|Secondary structures, fluid lines, brackets.|
|**Al 2219**|Cryogenic Strength|Rocket fuel tanks (LOX/LH2 tanks).|
|**Al-Li 2099**|Low Density / High Stiffness|Modern fuselage panels (e.g., SpaceX Falcon 9).|

### 2. Titanium Alloys :
Used where aluminum will melt or fail under extreme loads.

| **Material**           | **Key Property**           | **Common Aerospace Use**                         |
| ---------------------- | -------------------------- | ------------------------------------------------ |
| **Ti-6Al-4V (Gr 5)**   | General Purpose Excellence | Landing gear, engine pylons, wing-to-body joins. |
| **Ti-6Al-2Sn-4Zr-2Mo** | Creep Resistance           | High-temp engine compressor disks.               |
| **Ti-10V-2Fe-3Al**     | High Hardenability         | Heavily loaded landing gear beams.               |

### 3. Steel & Superalloys (Extreme Environments)
Used for fasteners, landing gear, and the "hot section" of rocket engines.

|**Material**|**Key Property**|**Common Aerospace Use**|
|---|---|---|
|**PH 15-5 / 17-4**|Corrosion + High Strength|Actuators, fasteners, structural pins.|
|**4130 / 4340 Steel**|High Toughness|Engine mounts, landing gear struts.|
|**Inconel 718**|Extreme Heat Resistance|Turbine blades, rocket engine nozzles (Merlin).|
|**Maraging Steel**|Ultra-High Tensile Strength|Solid rocket motor cases, high-load shafts.|


### 4. 4. Composites & Others (High Stiffness)
Modern aerospace has shifted towards these to save massive amounts of weight

| **Material**             | **Key Property**       | **Common Aerospace Use**                         |
| ------------------------ | ---------------------- | ------------------------------------------------ |
| **CFRP (Carbon Fiber)**  | Tailored Stiffness     | Wing skins (787/A350), payload fairings.         |
| **Kevlar (Aramid)**      | Impact Resistance      | Ballistic shielding, containment rings.          |
| **Honeycomb (Al/Nomex)** | High Moment of Inertia | Floor panels, control surfaces (flaps/ailerons). |

---
## Critical FEA Input Parameters
|**Material Group**|**Young's Modulus (E)**|**Poisson's Ratio (ν)**|**Density (ρ)**|
|---|---|---|---|
|**Aluminum**|$70 - 75\text{ GPa}$|$0.33$|$2700 - 2800\text{ kg/m}^3$|
|**Titanium**|$110 - 115\text{ GPa}$|$0.31 - 0.34$|$4400 - 4500\text{ kg/m}^3$|
|**Steel**|$190 - 210\text{ GPa}$|$0.27 - 0.30$|$7800 - 8000\text{ kg/m}^3$|

>[!Tip]
>When extracting data from **[[MMPDS]]**, always check if you need **A-Basis** or **B-Basis** values:
>- **A-Basis:** 99% probability with 95% confidence (used for single-load-path, "fail-safe" critical parts).
>- **B-Basis:** 90% probability with 95% confidence (used for redundant structures).



























### Steel

|**Property**|**Mild/Structural Steel**|**Elastic (Spring) Steel**|
|---|---|---|
|**Yield Strength**|Low (deforms permanently easily)|Very High (resists permanent deformation)|
|**Ductility**|High (stretches like taffy before breaking)|Lower (snaps if pushed too far past yield)|
|**Carbon Content**|Low (approx. 0.05% to 0.25%)|Medium to High (approx. 0.5% to 1.0%)|
|**Typical Use**|I-beams, car frames, pipes|Springs, lock picks, saw blades, clips|


>Note : Almost all steels have the same **Young’s Modulus** (approx. 200 GPa). This means that if you hang a weight from a mild steel wire and a spring steel wire of the same size, they will both stretch the **exact same amount**. The difference is that the mild steel will stay stretched (plastic deformation), while the elastic steel will bounce back

