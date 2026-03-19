---
tags:
  - structures
---
Metallic Materials Properties Development and Standardization - It is the globally recognized handbook used by the FAA, DoD, and NASA for the design of aircraft and space vehicles.

The MMPDS is a massive, multi-volume document that provides **statistically binned** material properties. When a manufacturer creates a new batch of 7075-T6 Aluminum, the strength isn't exactly the same every time.

In an aerospace Margin of Safety (MoS) calculation, you cannot just use the "average" strength of a material. If you did, 50% of your planes would fail. Instead, MMPDS defines:

- **A-Basis:** At least **99%** of the population is expected to equal or exceed this value with **95%** confidence.
- _Use case:_ Critical, single-load-path parts where if it breaks, the plane goes down (e.g., a wing spar attachment).

- **B-Basis:** At least **90%** of the population is expected to equal or exceed this value with **95%** confidence.

- _Use case:_ Redundant structures where the load can redistribute if one part fails (e.g., fuselage skin panels).

- **S-Basis:** The minimum value specified by the material's governing specification (like an AMS spec). This is the "default" but carries the least statistical weight.

>MMPDS is the alternative to MIL-HDBK-5 or more commonly referred to as Mil-Spec-5

>It is important to note that **MMPDS is only for metals**. If you are analyzing Carbon Fiber or Fiberglass, you have to look at its sister document: [[CMH-17 (Composite Materials Handbook)]]



