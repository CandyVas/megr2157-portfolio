# A2 – Truss Stress Analysis

## Objective
We are tasked to design a light weight planar truss using A500 structural steel using the shown figure below
<img width="248" height="161" alt="image" src="https://github.com/user-attachments/assets/7ab8182e-a6b2-46e3-84f0-a8988ce9f15b" />

> figure #1

## Analyze
1 & 2
The force and geometric constraints of the truss are provided below  
+ We are to choose a P **between 20kN and 30kN**
+ distance of a = .4 m
+ distance of b = .3 m
+ Point A is a pin 
+ point B is a roller

Some things I noticed from the figure is that there is an upward force *P* at point C, and a downward force *P* at point D. There is also 4 joints to take into account, A, B, C, and D. Since A is a pin, that accounts for 2 support reactins. And B is a roller which is 1 support reaction, which totals to 3 support reactions.  How I began to approach my design is by first, choosing the number for P. I decided on a applied force of **25 kN**, simply because it is exactly halfway between the lowest and highest permitted load. The next step in my process was to find external forces, 

### a. Design the truss structure using the parameters in Figure #1.
+ i. Since we are meant to generate the lengths of each element based to support the loads at point C and D, here is the sketch a truss structure i have come up with to fit this criteria. We need to connect load points C & D to supports A & B There are two triangles that generate the following, with members BC BD CD AC AD
    + triangle BCD
    + triangle ACD
<img width="449" height="246" alt="image" src="https://github.com/user-attachments/assets/aa038163-6e95-4983-a886-66c31bacb273" />
<img width="453" height="253" alt="image" src="https://github.com/user-attachments/assets/658d6a35-0653-42a8-bec3-5d1e9221eca4" />

+ ii. Sketch and label a FBD of each joint on the truss.


+ iii. Symbolically solve for all internal forces.
  
+ iv. Numerically solve for all internal forces.
<img width="422" height="261" alt="image" src="https://github.com/user-attachments/assets/2a59798b-d5ba-44f1-9488-519e4a726828" />

### b. Use the largest internal force to calculate the required cross-sectional area of the elements using a safety factor of 3.5, and the yield strength. 
+ i. List all the knowns and unknowns.
+ ii. Symbolically solve for minimum cross-sectional area (without numbers).
+ iii.Numerically solve for the cross-sectional area.
+ iv. Determine the approximate weight of the truss


## Decide
3. & 4 Determine the cross-sectional area of the connecting pins which are made of hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in3. Assume that elements that are in compression won’t fail in buckling.
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate
Detail engineering lesson learned and be specific. Eliminate words like good and bad from this section. Be more articulate.
