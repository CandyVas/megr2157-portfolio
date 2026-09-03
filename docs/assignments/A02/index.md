# A2 – Truss Stress Analysis

We are tasked to design a light weight planar truss using A500 structural steel using the shown figure below
<img width="248" height="161" alt="image" src="https://github.com/user-attachments/assets/7ab8182e-a6b2-46e3-84f0-a8988ce9f15b" />

## Overall Truss

The force and geometric constraints of the truss are provided below  
+ We are to choose a P **between 20kN and 30kN**
+ Distance of a = .4 m
+ Distance of b = .3 m
+ Point A is a pin 
+ point B is a roller

Some things I noticed from the figure is that there is an upward force *P* at point C, and a downward force *P* at point D. There is also 4 joints to take into account, A, B, C, and D. Since A is a pin support, it provides two support reactions, while B is a roller support, providing one support reaction. This gives a total of three support reactions total. I began my design process by first selecting a value for P. I decided to use an applied force of 25 kN, which is exactly halfway between the lowest and highest permitted loads. The next step was to determine the external forces acting on the truss. This can be accomplished by treating the entire truss as a single structure and considering the applied loads and support reactions acting on it.

## a. Design a truss
### + i. sketch truss
Since the goal is to generate lengths that'll support the loads at both C and D, we need to connect the supports at A and B so that the applied loads can be transferred through the truss to the supports. One of the constraints was to keep the design as simple as possible. Therefore, I decided not to add any additional joints beyond the four required points, A, B, C, and D. This results in a straightforward truss configuration while still providing the necessary structural connections between the loads and the supports.

<img width="449" height="246" alt="image" src="https://github.com/user-attachments/assets/aa038163-6e95-4983-a886-66c31bacb273" />

Because there are four joints, I wanted to create a structure that would be stable. This meant having five members. In order for a truss to be stable, the number of members (m), joints (j), and reactions (r) must satisfy the equation m + r = 2j. In my example, I have 5 members, 4 joints, and 3 reactions. Therefore, 5 + 3 = 2(4), or 8 = 8. Since both sides of the equation are equal, my design meets the stability criteria for a truss.

+ These are two triangles that generate the following, with members **BC, BD, CD, AC, AD**
    + triangle BCD
    + triangle ACD
    
<img width="453" height="253" alt="image" src="https://github.com/user-attachments/assets/658d6a35-0653-42a8-bec3-5d1e9221eca4" />

I then solved for the external forces. I chose to take the moment about point A because it has the most unknown forces, which lets the forces cancel out and makes the equation easier to solve. In my drawing, I showed whether each force creates a clockwise or counterclockwise moment. This determines whether the force is represented as positive or negative in the equation.

<img width="458" height="304" alt="Screenshot 2026-09-01 003514" src="https://github.com/user-attachments/assets/e5f75605-7a72-44b5-b8c5-718df90fe78e" />

However, at this point, I realized that at both points A and B, there are two diagonal chords that are facing the same direction, and both at the same angle downward. This made me reconsider my structure because of the potential internal forces. If I wanted to use the method of joints, I would naturally start at either A or B after solving for the external reactions. However, at either joint, I would have multiple unknown member forces, such as Fac and Fad, making the joint difficult to solve immediately.  still needed to follow the stability equation, meaning that with four joints and three reactions, I needed to have a total of five members. This led me to my final design.
+ These are two triangles that generate the following, with **<u>NEW</u>** members **BC, BD, CD, AB, AD**
    + triangle BCD
    + triangle ABD
    
<img width="382" height="192" alt="image" src="https://github.com/user-attachments/assets/31a7d989-ca49-4b15-a2cd-91cef57f0f84" />

I essentially did the same steps when solving for the external forces, except with my new and improved design. 

<img width="359" height="236" alt="image" src="https://github.com/user-attachments/assets/ee9c23c7-973a-47fa-a533-b5dd6fd0452c" />

You'll notice we got the same result, which makes sense since this is the external forces which is due to the fact that external forces depend only on the overall loading, support conditions, and geometry of the structure.

### ii. Sketch & label FBD of each joint on the truss.
Internal forces are the pushing (compression) and pulling (tension) forces carried inside the members meeting at each joint. If you'll notice that some of the directions of my external forces are not the same as my internal forces. Even though I originnally represented By as a positive force, the calculation resulted in a negative value of -8.3333. This negative result indicates that the actual direction of the force is opposite to the original. The same concept applies to the Ax since the horizontal forces equal 0.

<img width="324" height="247" alt="image" src="https://github.com/user-attachments/assets/5d9a5be9-f0f8-4f4c-963b-b5e49582b579" />
 
### iii. Symbolically solve for internal forces.

I decided to solve for the internal forces using the Method of Joints, beginning with Joint A. In the free-body diagram, it may appear that there are three unknown forces at Joint A, but there are actually only two because we already solved for Ay

Solving the equations symbolically first helps me visualize which joint I should start with and which joint I should proceed to next before inserting the numerical values. This makes the overall process more organized and easier to follow.

<img width="512" height="265" alt="image" src="https://github.com/user-attachments/assets/d924a9a1-dcf6-4488-852c-8f32c486d94f" />

### iv. Numerically solve for internal forces.
The process I followed when solving the truss was to first work on Joint A and then proceed to Joint C. I chose Joint C because it was similar in structure to Joint A, with only two chords and only one unknown force remaining. This made it a straightforward joint to solve using the equilibrium equations.

<img width="419" height="285" alt="image" src="https://github.com/user-attachments/assets/87758fbc-4b32-41e8-bb27-e21aee86fed2" />

Although when symbolically solving I had labeled my joints in A, B, C, D,  I ended up solving them somewhat out of sequence. By the time I reached the  equation for Joint C, I realized that I had already solved for a total of five members. Since my truss only has five members, this meant that all of the unknowns had been found. At this point, there was no need to continue solving the remaining joints because all of the member forces in the truss had been accounted for.

## b. Cross-sectional Area

We are then tasked with finding the largest internal force in order to calculate the required cross-sectional area of the members using a safety factor of 3.5 and the yield strength of the material. From my previous calculations, the largest internal force is 47.4 kN. However, the yield strength was not directly provided in the assignment. The material specified for the members is A500 structural steel. After further [research](https://www.tottentubes.com/astm-a500-specification-information), I disocvered that the strength of A500 steel varies depending on its grade and shape, with yield strengths ranging from approximately 228 MPa to 345 MPa. Because of this range, I decided to use a yield strength of 250 MPa for my calculations.

### i. List all the knowns and unknowns.
We know that... 
+ The largest internal force is Fbd which is equal to 47.46 kN. 
+ Safety factor is N = 3.5
+ The chosen Yield Strength is 250 MPa

Some Unknowns include...
+  minimum cross sectional area 

### ii. Symbolically solve for min cross-sectional area

To determine the required cross-sectional area (in this case the minimum), I symbolically solved for the basic relationship between stress, force, and area. Then used that to cross multiply with the allowable stress. 

<img width="242" height="250" alt="image" src="https://github.com/user-attachments/assets/b8eea650-adf1-42d0-bca8-b295c1ad3c80" />

### iii.Numerically solve for the cross-sectional area
Following the same process as when I symbolically solved for the minimum cross-sectional area, I then substituted the values I had already found into the equation. Using the largest internal force of 47.4 kN, a safety factor of 3.5, and a yield strength of 250 MPa, I calculated the required area.

<img width="457" height="221" alt="image" src="https://github.com/user-attachments/assets/002567bc-b058-4f73-bf34-00581c07250f" />

### iv. Determine the approximate weight of the truss

The standard density of steel is approximately 7.85 g/cm³. Since the final weight of the truss needs to be expressed in kilograms, I converted the density into units of kg/m³. 

<img width="261" height="328" alt="image" src="https://github.com/user-attachments/assets/a70ea873-7340-4d8c-b453-1d9475646ddc" />

## 3. Cross-section (pins)
Next, we are tasked to determine the cross-sectional area of the connecting pins which are made of hardened tool steel with a yield shear strength of 170 ksi and a density of 0.278 lb/in^3. Since we have already solved for the forces in every member of the truss, we can now use those forces to determine the required cross-sectional area of the pins.

### i. List all the knowns and unknowns.
We know that... 
+ The largest shear force in a connecting pin is 25 kN. 
+ Safety factor is N = 4
+ The provided Yield Strength is 170 ksi
+ Density of 0.278 lb/in^3

Some Unknowns include...
+  minimum cross sectional area of each pin

### ii. Generate a FBD of the pin with the largest reaction load.
 Since this is asking for the largest reaction load, that would mean the largest of the external supports, not the same internal member Fbd that we used to solve part b. This turns out to be both our P loads at pin C & D, so this diagram could be applied to either pin. 

<img width="296" height="328" alt="image" src="https://github.com/user-attachments/assets/4494c8a5-cbd7-4bea-9c16-15f2c6492c94" />

### iii. Symbolically solve for min cross-sectional area.
Since we are meant to design a **single shear connection** I decided to use the shear equation τ = V / A as opposed to its double shear counterpart τ = V / 2A. Since we are supposed to consider the safety factor of 4, we now have to consider the allowable shear stress in order for the pin to be safe. 

<img width="176" height="271" alt="image" src="https://github.com/user-attachments/assets/9fb83d7b-9fd5-4136-901b-f2564803b19f" />

### iv. Numerically solve for the cross-sectional area   
Despite the provided values, the units are not directly compatible for the shear stress calculation. The shear force is given in kilonewtons (kN), while the yield shear strength of the hardened tool steel is given in ksi. Since the density is also provided in lb/in³, it is more convenient to convert the force into pounds-force lbf and the yield strength into psi before solving for the cross-sectional area.

<img width="472" height="220" alt="image" src="https://github.com/user-attachments/assets/aa9cfae0-2e19-4dc7-ba43-a6af63fdf094" />

### v. Approximate combined weight of the pins.
The weight of an individual member could be determined using the volume-density formula Weight = A * L * ρ. However, we are dealing with a truss which carries four identical pins, therefore we can change the equation to be W = A * L * 4ρ. I figured I'd use the cross sectional area found in part three, which I estimated to be 26 x 26 mm.  

<img width="449" height="277" alt="image" src="https://github.com/user-attachments/assets/3a46e6dc-9595-41cc-b333-f73e5ac43a97" />

There was some confusion when trying to determine the length of the connecting pins. I initially started calculating the diameter and cross-sectional area of the pin, but I realized that this did not fully fit the formula being used because the formula required the length of the pin as well. I eventually connected this back to Part B, where I had already determined the cross-sectional dimensions of the truss. Since the cross section is 26 mm × 26 mm, I could use this dimension to determine the approximate length of the connecting pins. Therefore, the pin length is 26 mm, or 0.026 m.

## CAD fun
Utilize CAD software to generate a 3D model of the truss. Model the pins as cylinders with the appropriate cross-sectional areas and lengths.
 
For the CAD portion of the assignment, I initially decided to use Creo because it was the program I had the most recent experience with. When representing the truss, I used the top plane as my workspace and began by measuring from the center and extending toward the right. I then followed the dimensions and calculations from my hand calculations to construct the truss.

One of the challenges I encountered was keeping my units consistent. For example, I would sometimes have one calculation represented in meters while another was represented in inches. Although the numerical values could be converted, switching between units made it easier to make errors. Another issue was that Creo would round the values for dimensions. 

<img width="634" height="260" alt="image" src="https://github.com/user-attachments/assets/5d326b6c-1b8d-4414-862d-f63873d4941b" />

I then used the line chain tool to create the diagonal chords of the truss. This was considerably difficult because I was completing the CAD work without a mouse on my laptop. Despite this, the dimensions I was obtaining were remaining consistent with my calculations.

<img width="655" height="280" alt="image" src="https://github.com/user-attachments/assets/6136d903-508e-42a9-b7b4-dc63638098b8" />

... only to realize that Creo is impossible to use without a mouse because the scroll wheel is used for pretty much everything. Because of this limitation, I switched to SolidWorks, a program I have no experience in, and recreated the truss using essentially the same process.

<img width="549" height="349" alt="image" src="https://github.com/user-attachments/assets/604afbba-3234-4dce-9bb7-458d1fb48c1f" />

<img width="591" height="293" alt="Screenshot 2026-09-03 022449" src="https://github.com/user-attachments/assets/55ee3718-2882-497c-9fdc-398de5113d39" />

Once I was satisfied with the sketch, I extruded the truss to the 26 mm thickness that I had calculated (in meters, .026m). As for my pin diameter, I have it calculated as .5 inches which converts to 0.0127 m. Luckily diameter fit within the dimensions of my design without requiring any changes to my previous calculations. 

<img width="535" height="240" alt="image" src="https://github.com/user-attachments/assets/f7445d91-f509-4f15-bd22-bc9b05f10799" />

<img width="695" height="239" alt="Screenshot 2026-09-03 033823" src="https://github.com/user-attachments/assets/893bfadd-9d6c-4eff-ab59-8b661e8d7cde" />


<img width="625" height="189" alt="image" src="https://github.com/user-attachments/assets/cac7d67b-7a72-4739-a425-c92c62d80384" />

When assigning the material in SolidWorks, I noticed that A500 structural steel was not available in the material library. Since the purpose of this portion of the assignment is to compare the CAD results with my hand calculations, I needed to find a material with similar density and mass properties. After searching for an alternative, I decided to use AISI 1020 steel as an approximation because its density is close enough to A500 steel for the purpose of estimating the mass of the truss.

Another issue I encountered was that my SolidWorks document was initially set to the wrong unit system. When I attempted to convert the units to the correct system, SolidWorks would scale the drawing rather than simply changing the displayed units. I addressed this by overriding the conversion in the settings

<img width="744" height="425" alt="image" src="https://github.com/user-attachments/assets/7dee79b8-fc72-4b8d-a941-404ceac0a259" />

After completing the model and assigning the material, I used the Mass Properties feature in SolidWorks to simulate the calculations I had previously completed by hand. The CAD model produced the following results... 

+ Density = 7900.00 kilograms per cubic meter
+ Mass = 13.51 kilograms
+ Volume = 0.00 cubic meters
+ Surface area = 0.30 square meters

The CAD result was noticeably different from my hand calculation. My calculated weight for the truss was approximately 176.636 N, which is 18.01 kg when converted. This means there is a difference of approximately 4.50 kg between my hand calculation and the SolidWorks result. While this difference is larger than I initially expected, it can be a contribution of many factors to several factors, including the different material densities used, rounding during the CAD modeling process, and the different conversions.

## Communicate
### Engineering lesson learned
During the course of completing this project, there was not just a singular lesson that I learned. It taught me several 

+ Keeping units consistent: I learned how important it is to keep my units consistent throughout the entire calculation. I switched between meters, millimeters, inches, kN, N, and psi during the project, which caused some confusion. In the future, I will choose one unit system at the beginning and convert everything before starting my calculations.

+ Rounding numbers: One thing that caused problems was rounding my numbers too early when solving for the internal forces. I kept using slightly different values as I moved from one joint to another, which caused the final answers to become less consistent. I learned that it is better to keep more decimal places during the calculations and only round at the end.

+ Pay attention to CAD settings!!!!!: I also learned (the very hard way) that I need to pay closer attention to the CAD program I am using. Switching between Creo and SolidWorks and dealing with different unit settings caused some issues with my model. I learned that i should check that BEFORE starting the model or I'd be forced to either remake or convert everything.
 
+ Checking my work with CAD: Finally, I learned that CAD is useful for checking hand calculations. Comparing my SolidWorks mass to my calculated mass showed me that there were differences in my results and gave me a reason to go back and look at my units, dimensions, and the material properties.

... the time it took me to complete these assignment was 2 days. However my progress has been inconsistent, I did dedicate a lot of time into working on this. 
