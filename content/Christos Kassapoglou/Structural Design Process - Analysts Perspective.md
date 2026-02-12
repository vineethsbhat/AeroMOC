---
tags:
  - composites
  - structures
---
The typical requirements can be classified into :
1. Fit, form and function : Goal is to avoid interference between adjacent structures, appropriate material and shape and perform necessary function
2. Applied loads : Must not fail under applied static loads and desired life under applied fatigue load. Also must be able to withstand this in the presence of damage. 
3. Corrosion resistance : The amount of exposure and effect of corrosion must be reduced
4. CTE : Wide variations in temperature must be accounted for, thus a low CTE is better.
5. Frequency placement : Avoid resonance especially with the most dominant modes

As a design engineer we must figure out the hard points for the load application points and attachments and transfer of loads through load path estimation. In most cases the desirable attribute is always weight followed by cost.

Follow these steps :

1. Obtain the loads and design requirements 
2. Start with the simplest possible model and make a choice for the preliminary design and fix and structural configuration
3. Now we fine tune the design based on requirements set through a more detailed analysis, this is where you validate the FEA models for the experiments done
4. At this point it is useful to do an order of magnitude estimation to see how long it takes to produce said part or component.
5. The total number of load cases that have to be analysed is in the order of 1000s
6. Assume we have 3 design concepts, stiffened panel, sandwich panel and isogrid panel. This can also have 3 different ways of fabrication, co-cured, co-bonded and mechanical fasteners. In order to find the optimum which means the design requirements are met as well as the desired attribute is met (cost or weight) a certain optimisation algorithm is to be used ([[Multidisciplinary Design Optimisation]]). Note a ==genetic design== algorithm is used
7. Typically to converge on an optimum it needs at least 1000 iterations, with 15 designs per iteration.
8. This is not feasible by any means, thus certain load cases are ignored. But it wont be optimum because we haven't looked at everything, but it is not economically feasible to do extensive optimisation on large parts since computational effort is very high


Failure Mode in a Lug :
1. Net Section : Material fails in tension between lug hole and edge of part
2. Shear Out : Material fails in shear between at hole edge along two planes parallel to load
3. Bearing Failure : The lug hole becomes an oval/ lug hole elongates and material fails in bearing/compression ahead of hole