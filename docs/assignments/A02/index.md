# A2 – Truss Stress Analysis

## Objective
We are tasked to design a light weight planar truss using A500 structural steel using the shown figure below
<img width="248" height="161" alt="image" src="https://github.com/user-attachments/assets/7ab8182e-a6b2-46e3-84f0-a8988ce9f15b" />

> figure #1

## Analyze
1 & 2
The force and geometric constraints of the truss are provided below  
+ We are to choose a P **between 20kN and 30kN**
+ Distance of a = .4 m
+ Distance of b = .3 m
+ Point A is a pin 
+ point B is a roller

Some things I noticed from the figure is that there is an upward force *P* at point C, and a downward force *P* at point D. There is also 4 joints to take into account, A, B, C, and D. Since A is a pin, that accounts for 2 support reactions. And B is a roller which is 1 support reaction, which totals to 3 support reactions.  How I began to approach my design is by first, choosing the number for P. I decided on a applied force of **25 kN**, simply because it is exactly halfway between the lowest and highest permitted load. The next step in my process was to find external forces which is accomplished by looking at the entire truss as a single structure. This takes into consideration the loads and supporting forces 

## a. Design the truss structure using the parameters in Figure #1.
### + i. Since we are meant to generate the lengths of each element based to support the loads at point C and D, here is the sketch a truss structure i have come up with to fit this criteria. We need to connect load points C & D to supports A & B
 
<img width="449" height="246" alt="image" src="https://github.com/user-attachments/assets/aa038163-6e95-4983-a886-66c31bacb273" />

Because there are four joints, i wanted to make a structure that was stable. that would mean having 5 members. In order for a truss to be stable, the number of members (m) and joints (j) must satisfy the equation m + r = 2j. With my example, I have 5m, 4j, and 3r. therefore, 5+3=2(4) -> 8=8 my design fits this criteria
+ These are two triangles that generate the following, with members **BC, BD, CD, AC, AD**
    + triangle BCD
    + triangle ACD
    
<img width="453" height="253" alt="image" src="https://github.com/user-attachments/assets/658d6a35-0653-42a8-bec3-5d1e9221eca4" />

i then solved for the external forces - i chose to make the moment about a since it has the most unknown forces.  [explain why you made forces the direction]

<img width="458" height="304" alt="Screenshot 2026-09-01 003514" src="https://github.com/user-attachments/assets/e5f75605-7a72-44b5-b8c5-718df90fe78e" />

### ii. Sketch and label a FBD of each joint on the truss.
Internal forces are the pushing (compression) and pulling (tension) forces carried inside the members meeting at each joint. If you'll notice that the direction of my external forces arent the same as my internal forces. Despite the fact that i have By as a positive force, when looking at the result you will find that i got a negative number (-8.3333). Same goes for the Ax value, since the sum ended up being 0 it was removed. 

<img width="348" height="302" alt="image" src="https://github.com/user-attachments/assets/e0b2804c-eb1a-4d33-a4fb-412319c555f8" />

 
### iii. Symbolically solve for all internal forces.

i decided to solve this via method of joints and began with joint A,  
  
### iv. Numerically solve for all internal forces.

## b. Use the largest internal force to calculate the required cross-sectional area of the elements using a safety factor of 3.5, and the yield strength. 

### i. List all the knowns and unknowns.
### ii. Symbolically solve for minimum cross-sectional area (without numbers).
### iii.Numerically solve for the cross-sectional area.
### iv. Determine the approximate weight of the truss


## Decide
3. & 4 Determine the cross-sectional area of the connecting pins which are made of hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in3. Assume that elements that are in compression won’t fail in buckling.
_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

## Communicate
Detail engineering lesson learned and be specific. Eliminate words like good and bad from this section. Be more articulate.
