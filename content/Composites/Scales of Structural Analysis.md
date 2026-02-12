---
tags:
  - "#structures"
  - composites
---
The primary goal in performing mechanical analysis is :

1. To understand requirements regarding the performance of the material
2. To verify the behaviour
3. Influence design as best as possible
4. In most cases you are optimizing for performance, safety and cost and mechanical analysis allows you to achieve the that.

When performing analysis we almost never jump directly into simulating an airplane. We use a building block approach or more commonly referred to as a "Test Pyramid". ==And the reason this is done is because new behaviour/failure modes/ appear as you add geometry, loads, joints, defects, and manufacturing variability== 

The pyramid goes like this (bottom-up)
1. Coupon Level : You are analyzing small, simple specimens, this is done to isolate material behaviour. Think of tensile tests done in UTM, the specimens are designed (dog bone) such that they only isolate material behaviour. ==It teaches you what the material can do in idealized conditions==
2. Element Level : Still small, but now you introduce real structural features : Holes, notches, stiffeners, ply drop off, bonded/bolted etc. You start caring about manufacturing details. ==Teaches you how the material behave when you make it a structure with real features==
3. Component Level : A meaningful chunk of the aircraft, e.g., stiffened panel, or a wing box section, with some assemblies are tested. This level deals with integration of the structure to understand BCs and load paths
4. Structure Level : Full scale integrated structure e.g., full wing, airframe, is tested for certification and you are trying to understand ==whether the entire system is behaving as expected==


- [k] What is to be remembered
	1. Geometric complexity increases as you move up
	2. Loads become more real (from ideal grips to distributed loads)
	3. Failure mode interaction becomes more apparent
	4. Cost and time per data point becomes expensive




---
Read Also : [[Scales of Analysis in Composites]]