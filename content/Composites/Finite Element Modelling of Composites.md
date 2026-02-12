---
tags:
  - composites
---
Basic Approaches to Finite Element modeling of laminates :
1. Shell models for “thin” structures : ==Layered Shell== has displacement and rotation at every node
2. Continuum elements for “thick” structures : ==One element per ply== has only displacement DOF at every node, the geometry is represented by a volume 
3. Continuum shell element : has the topology of solid elements and but kinematics of shell elements 

A better way to approach modelling :
a. Layered Shell : Several plies are stacked in one shell element, most commonly used, less numerical effort, no stresses in thickness direction
b. Continuum Elements : one layer of elements represents one ply, changes require re-meshing, enhanced modelling effort

