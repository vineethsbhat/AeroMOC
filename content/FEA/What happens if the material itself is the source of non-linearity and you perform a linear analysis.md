---
tags:
  - fea
  - structures
---
If the material itself is nonlinear (e.g., it yields or follows a power-law stress-strain curve) and you perform a **Linear Eigenvalue Buckling Analysis**, the results will be unconservative

In simple terms: The FEA results will tell you the structure is safe, but it will likely fail much earlier in the real world.

Linear buckling assumes the material maintains its initial **Young’s Modulus** forever. However, if the stress in your aerospace component exceeds the proportional limit, the actual stiffness of the material drops. 

Inelastic Buckling :

In aerospace, we categorize compression members into two groups. A linear analysis fails to distinguish between them properly :

1. **Long/Slender Members:** These buckle while the material is still elastic. Here, linear analysis is _mostly_ okay
2. **Short/Stubby Members:** These reach their material yield point _before_ they reach their theoretical Euler buckling load.

>[!The Catch :]
>If you run a linear analysis on a "stubby" fitting, the solver might give you a Buckling Load Factor (BLF) of **2.0**. However, because the material yields and loses stiffness at a BLF of **0.8**, the part will actually fail before it even reaches the design load.

### The Idea of Mode Switching :
When material nonlinearity is present, the **mode shape** can actually change

In a linear analysis, the structure might show a nice, global flexural buckling mode. In a nonlinear reality, a local area might yield first (like a flange on a stringer). This local softening causes the structure to "cripple" or fold in a way the linear solver can never predict. 


### The tangent modulus approach  and how engineers fix this -

Before modern high-speed FEA, engineers used the **Engesser** or **Shanley** theories. They would manually replace the Young's Modulus with the an equivalent modulus at the predicted stress level. In modern tools like NASTRAN we use SOL 106 pr 400 and the workflow is as follows :

- You input the **Stress-Strain table** from the MMPDS.
- You apply the load in small increments.
- The solver updates the stiffness matrix at every step based on the current stress state.
- If the solver "diverges" (cannot find an equilibrium), the structure has buckled or collapsed.


