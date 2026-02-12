---
tags:
  - composites
---
For a lamina, the failure index 𝐹 and the stress exposure $f_E$ are generally not equal. 

[Why ?]
Because failure criteria are often non-linear (usually quadratic), whereas stress exposure is a linear scaling factor. To understand the difference, we must look at how each is calculated :

 >For $F$  it is the value output by the polynomial equation of a specific failure theory (like Tsai-Wu or Tsai-Hill). It is a "check" value. Most modern criteria include quadratic terms (stress squared)
 >$F \approx A\sigma + B \sigma^2$
 
 >As for stress exposure $f_E$ it represents the "load level" relative to the allowable limit. It answers the question: "What percentage of the allowable load is currently being applied?
 >$f_E = \frac{\text{Applied Load}}{\text{Allowable Stress}}$
 >So if the applied load doubles, then the exposure doubles. 
 
 This is where the difference is, because failure index is quadratic and stress exposure is linear, they do not scale the same way and thus are not equal. 
 Example : Consider a simple failure criteria of $$F = \left(\frac{\sigma}{\sigma_{\text{limit}}}\right)^2$$
 And lets assume the applied load is half the allowable load, then $f_E = 0.5$ and $F = 0.5^2 = 0.25$
 Thus not equal.
[When are they equal ?]
1. When the material fails, they are equal. i.e., the moment of failure
2. When you use a linear criteria ([[Max. Stress and Strain Theory]])

[Why the hell does this even matter ?]

>[! Important]
>Extremely Important :
>If you interpret a Failure Index of **0.5** as "I have a safety factor of 2" (meaning I can double the load), you could be dangerously wrong. In a quadratic theory (Tsai-Wu), an index of **0.5** might mean you are actually at $\sqrt{0.5} \approx 0.71$ (71%) of your load limit. You can only increase the load by roughly **41%**, not **100%**.

---
[[Reserve Factor (RF)]] , 

