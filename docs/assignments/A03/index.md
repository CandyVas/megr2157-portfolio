# A3 – [Topic]

## Objective
We are to design a bar which has a circular cross section using the values of the criteria given for the material, maximum deflection, and load. This is meant to determine the bar’s minimum geometry, for example its length, diameter, and weight, through parametric design while under direct tension. Only then can we verify the geometry through finite element analysis.

<img width="650" height="143" alt="image" src="https://github.com/user-attachments/assets/61611d9c-ad92-49cf-9e84-eff8cf7c3304" />

## 1. Parametric Design
The first set of instruction is to parametrically design a bar in CAD with an <ins>applied direct load</ins> between **300 lbf < F < 500 lbf** and the <ins>max axial</ins> deflection of the bar being **.009 inches.** The material it will be designed with is from <ins>Aluminum</ins> with a range of Young’s Modulus from **(8.5 - 11.5) x 10^6 psi.**


### a.  

Choose the values for the cross sectional area of the bar. (width, height, and thickness)

I decided to choose a direct load of 500 lbf because it is the largest load within range. Since the bar should not exceed 0.009-in deflection, if I were to choose 300 lbf, there could be a chance of it deflecting when the load reaches 500 lbf.   would be best to design it. 

We are also tasked to choose from the Young’s Modulus range, and I settled on 10 x 10^6 (10,000,000) psi for the sake of convenience, same for my width of .600 inches and thickness of .300 inches. 

with that in mind then... 
+ Maximum load: F = 500 lbf
+ Aluminum modulus: E = 10 x 10^6 psi
+ Maximum axial deflection: δ = 0.009 in
+ t = .600 inches
+ w = .300 inches

using the direct tension elongation equation in the Machinery’s Handbook, i found the length of the bar 32.4 inches. 

### c.

Generate the bar in CAD by assigning the parameters of Modulus of Elasticity, max deflection, load, width, height, and thickness to parametric equations in order to determine the length of the bar.
. 
## 2. Conduct FEA

### a.
### b.
### c.

(20%) Generate a deflection map in the FEA.
(20%) Generate a von Mises Stress map.
(5%) Check the maximum stress is lower than the strength of Aluminum (Sy = 40 ksi) and note the safety factor.

## 3. Design Reflection

### a.
### b.

## 4. Lessons Learned
