# A3 – [Topic]

## Objective
We are to design a bar which has a circular cross section using the values of the criteria given for the material, maximum deflection, and load. This is meant to determine the bar’s minimum geometry, for example its length, diameter, and weight, through parametric design while under direct tension. Only then can we verify the geometry through finite element analysis.

<img width="650" height="143" alt="image" src="https://github.com/user-attachments/assets/61611d9c-ad92-49cf-9e84-eff8cf7c3304" />

## 1. Parametric Design
The first set of instruction is to parametrically design a bar in CAD with an <ins>applied direct load</ins> between **300 lbf < F < 500 lbf** and the <ins>max axial</ins> deflection of the bar being **.009 inches.** The material it will be designed with is from <ins>Aluminum</ins> with a range of Young’s Modulus from **(8.5 - 11.5) x 10^6 psi.**


I decided to choose a direct load of 500 lbf because it is the largest load within range. Since the bar should not exceed 0.009-in deflection, if I were to choose 300 lbf, there could be a chance of it deflecting when the load reaches 500 lbf.   would be best to design it. 

We are also tasked to choose from the Young’s Modulus range, and I settled on 10 x 10^6 (10,000,000) psi for the sake of convenience, same for my width of .600 inches and thickness of .300 inches. 

with that in mind then... 
+ Maximum load: F = 500 lbf
+ Aluminum modulus: E = 10 x 10^6 psi
+ Maximum axial deflection: δ = 0.009 in
+ t = .600 inches
+ w = .300 inches

<img width="655" height="237" alt="image" src="https://github.com/user-attachments/assets/eedf38bf-b4b4-4d21-a27c-28da6b0ab9f7" />

Using the direct tension elongation equation in the Machinery’s Handbook, I found the length of the bar 32.4 inches. I wanted to confirm this manual calculation was correct, so using the Equations Tab in solidworks, I added all the given values I provided above. This helped me confirm that my Length of the axial deflection was indeed correct. 

<img width="590" height="254" alt="image" src="https://github.com/user-attachments/assets/04654e5b-96e6-44d6-8bed-17746a8bb34e" />

I used the global variables inserted into Solidworks's equation tab to then build the shape of my bar. 

<img width="696" height="347" alt="image" src="https://github.com/user-attachments/assets/035dde4a-972a-4ac6-8e8a-1d3de12b4d0f" />
<img width="487" height="183" alt="image" src="https://github.com/user-attachments/assets/0ef1ff94-d194-4d76-aa8a-408e78eda969" />

I then extruded using the thickness 

<img width="688" height="364" alt="image" src="https://github.com/user-attachments/assets/06cc74a4-963e-4116-9e76-c1275247f992" />
<img width="566" height="282" alt="image" src="https://github.com/user-attachments/assets/6a176d2b-4eed-48a2-b02f-e744d5dd1b80" />


## 2. Conduct FEA

WE are then taskjed to work with solidworks stimulation, also known as FEA. 
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
