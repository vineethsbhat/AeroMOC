
The "Sense of Scale" Table

|**Stress Level**|**"Feel" / Intuition**|**Material Context**|
|---|---|---|
|**1–10 MPa**|"Hand-tight"|Plastic toys, thick wood, rubber seals.|
|**30–50 MPa**|"The Buckling Zone"|Where thin aerospace sheets start to warp or "oil-can."|
|**250–300 MPa**|"The Yield Wall"|Most 6061-T6 Aluminum starts to permanently deform here.|
|**450–500 MPa**|"The Limit"|High-strength 7075 Aluminum or Mild Steel peaks here.|
|**1,000+ MPa**|"The Super Zone"|High-strength Titanium or Heat-treated Steel territory.|

### Statics vs. Dynamics
| **Category** | **Time Factor**           | **Aerospace Example**                                      | **Key Tool**                 |
| ------------ | ------------------------- | ---------------------------------------------------------- | ---------------------------- |
| **Statics**  | Constant or very slow.    | A plane sitting on the tarmac; steady level flight.        | Static Structural (ANSYS)    |
| **Dynamics** | Changes rapidly ($F=ma$). | Landing impact; bird strike; engine vibration; turbulence. | Modal / Transient / Explicit |

- **Creep:** This is a "Statics" problem that happens over a long time (years). The part is under a constant load at high heat (like a turbine blade) and slowly "stretches" like taffy.

- **Fatigue:** This is a "Dynamics" problem. The load might be small, but the _repetition_ (vibration or pressurization cycles) is what causes the crack.

### The "Three Pillars" of Failure

#### A.  Material Failure (The "Micro" Scale)

The atoms give up. The stress is simply too high for the chemical bonds.

- **Yielding:** It bends and stays bent (Ductile).
    
- **Fracture:** It snaps like glass (Brittle).
    
- **Fatigue:** A tiny crack grows until the remaining metal can't hold the load.

#### **B. Structural Failure (The "Macro" Scale)**

The material is perfectly fine, but the **Shape** is unstable.

- **Buckling:** A thin column or sheet "snaps" out of plane under compression.
    
- **Crippling:** Localized buckling of a flange or an edge.

#### **C. Functional Failure (The "Limit" Scale)**

Nothing broke, and nothing buckled, but the part is **useless**.

- **Excessive Deflection:** The wing bends so much it hits the fuel tank or jams a hinge.
    
- **Aeroelasticity (Flutter):** The wing vibrates so wildly in the wind that it eventually rips off (this is a mix of Dynamics and Statics).

### 3. The "Load Type" Matrix

When you look at a part, ask: **"How is the force being delivered?"**

1. **Point Load:** A bolt pulling on a hole. (High stress concentration!)
    
2. **Distributed Load:** Air pressure pushing on a wing skin. (Smooth stress.)
    
3. **Thermal Load:** The engine heat trying to stretch a mount.
    
4. **Inertial Load:** The "G-force" during a turn making the heavy engine want to fly off the wing.


How to analyze a system : A mental checklist 

- **Statics:** "What is the maximum 'G' load this will ever see? I'll check Von Mises stress against Yield."

- **Stability:** "Is any part of this bracket thin and in compression? If so, I need a Buckling analysis."

- **Dynamics/Fatigue:** "Does this part sit near the engine? If so, I need to check for vibration (Modal) and Fatigue life."

- **The Margin:** "I will calculate the Margin of Safety. If it’s between 0.1 and 0.5, the design is optimized."

### The strength cheat sheet :

|**Material**|**Yield Strength (σy​)**|**The "Mental Anchor"**|
|---|---|---|
|**Aluminium (6061-T6)**|**~270 MPa**|The baseline for "sturdy."|
|**Aluminium (7075-T6)**|**~500 MPa**|Aerospace grade; nearly as strong as mild steel.|
|**Titanium (Ti-6Al-4V)**|**~850–900 MPa**|The "Workhorse"; roughly **3x** stronger than 6061 Al.|
|**Steel (High Strength)**|**~1,000–1,200 MPa**|Landing gear territory; roughly **4x** stronger than 6061 Al.|
|**CFRP (Unidirectional)**|**~1,200–1,500+ MPa**|**Highest**, but only in the direction of the fibers.|

#### Common Failures :

| **Failure Mode** | **Primary "Fix"**        | **Key Variable to Change**        |
| ---------------- | ------------------------ | --------------------------------- |
| **Buckling**     | Add stiffeners/stringers | Increase $I$, Decrease $L$        |
| **Fatigue**      | Increase radii/Shot-peen | Decrease $K_t$ (Concentrations)   |
| **Creep**        | Cooling/Single crystals  | Temperature ($T$), Material Grain |
| **Bending**      | Taller beams (I-beams)   | Increase Section Modulus ($I/y$)  |
| **Torsion**      | Use Closed Boxes         | Increase Polar Moment ($J$)       |
