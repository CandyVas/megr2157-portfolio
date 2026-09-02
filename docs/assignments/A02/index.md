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
### + i. Since we are meant to generate the lengths of each element based to support the loads at point C and D, here is the sketch a truss structure i have come up with to fit this criteria. We need to connect load points C & D to supports A & B. The constraints were to keep the design simple, therefore i didnt deicde to add any additional joints 
 
<img width="449" height="246" alt="image" src="https://github.com/user-attachments/assets/aa038163-6e95-4983-a886-66c31bacb273" />

Because there are four joints, i wanted to make a structure that was stable. that would mean having 5 members. In order for a truss to be stable, the number of members (m) and joints (j) must satisfy the equation m + r = 2j. With my example, I have 5m, 4j, and 3r. therefore, 5+3=2(4) -> 8=8 my design fits this criteria
+ These are two triangles that generate the following, with members **BC, BD, CD, AC, AD**
    + triangle BCD
    + triangle ACD
    
<img width="453" height="253" alt="image" src="https://github.com/user-attachments/assets/658d6a35-0653-42a8-bec3-5d1e9221eca4" />

i then solved for the external forces - i chose to make the moment about a since it has the most unknown forces.  [explain why you made forces the direction]

<img width="458" height="304" alt="Screenshot 2026-09-01 003514" src="https://github.com/user-attachments/assets/e5f75605-7a72-44b5-b8c5-718df90fe78e" />

however, at this point i realized that at both points A and B, there are two diagonal chords that are not only facing the same direction, but also bth angled downwards. This made me think about solving the potential internal forces. If i wanted to solve for the joints, lets say either A or B since those supports will be solved via solving external forces. If i wanted to solce for the internal, I'd either be unable to solve for the hypotehiical Fac and Fad unknwon, or it would give me a hard time progressing onto the other joint its chorded to. This made me change my approach of the problem. Still considering the earlier equation m + r = 2j, i would need to be able to keep the total of 5 members. This resulted me in this as my final design 
+ These are two triangles that generate the following, with **<u>NEW</u>** members **BC, BD, CD, AB, AD**
    + triangle BCD
    + triangle ABD
    

<img width="382" height="192" alt="image" src="https://github.com/user-attachments/assets/31a7d989-ca49-4b15-a2cd-91cef57f0f84" />

I essentially did the same last steps as written before, except with my new and improved design 

<img width="359" height="236" alt="image" src="https://github.com/user-attachments/assets/ee9c23c7-973a-47fa-a533-b5dd6fd0452c" />

you'll notice we got the same result, which makes sense since this is the external forces which is __. 

### ii. Sketch and label a FBD of each joint on the truss.
Internal forces are the pushing (compression) and pulling (tension) forces carried inside the members meeting at each joint. If you'll notice that the direction of my external forces arent the same as my internal forces. Despite the fact that i have By as a positive force, when looking at the result you will find that i got a negative number (-8.3333). Same goes for the Ax value, since the sum ended up being 0 it was removed. 

<img width="324" height="247" alt="image" src="https://github.com/user-attachments/assets/5d9a5be9-f0f8-4f4c-963b-b5e49582b579" />
 
### iii. Symbolically solve for all internal forces.

i decided to solve this via method of joints and began with joint A. In the free body diagram it may look like we have 3 unknowns, but its actually only 2 since we have already solved for Ay. 

i then proceeded onto joint AC since we have just solved for Fac when solving joit A's internal forces. Once again that leaves us with only 2 unknowns (since we know the value for P) ewhich makes this equatin=on solvable 

<img width="512" height="265" alt="image" src="https://github.com/user-attachments/assets/d924a9a1-dcf6-4488-852c-8f32c486d94f" />
solving this symbolically helps me visualize when inserting the numbers of which joint t start withthen which one to proceed to. 

### iv. Numerically solve for all internal forces.
I worked o joint A, then proressed onto joint C since it was similar in structure to joint A, int he sense that there was only two chords.  
<img width="446" height="316" alt="image" src="https://github.com/user-attachments/assets/f16d48e2-2d46-45f2-bd45-8ab8cc17d439" />
Despite the steps i took when labeling my joints, i wored out of line when it came to solving. By the time i reached the Fx of joint c, i realized that i have solved for a total of 5 members, meaning all my unknowns have been solved for. 

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
