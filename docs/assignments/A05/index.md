# A5 – [Topic]

## Objective
24V DC planetary gear motor to a rigid vertical wall under a 300 N

We are tasked with designing a motor mount using a [*24V DC Gear Motor](https://www.omc-stepperonline.com/brushed-24v-dc-gear-motor-3-6kg-cm-46rpm-w-99-5-1-planetary-gearbox-pa28-28245800-g100) that is meant to attach to a rigid wall under 300 N.

<img width="448" height="132" alt="image" src="https://github.com/user-attachments/assets/2a4df698-0af7-4709-8320-374c683521bc" />

> Motor against Wall

<img width="122" height="117" alt="image" src="https://github.com/user-attachments/assets/53fa329f-3d36-4322-881b-2dd686c46e2d" />

> 24V DC Gear Motor

We are suppose to consider both features when designing for the yield strength and then designing for a maximum deflection of .30 mm at the free end. We were given the opition of selecting a material between ABS, PETG,  or PLA as a motor mount material. When making this decision, i deicded to go with PLA because not only is it the material i am most familiar with, after further research i discovered it is also the most optimal from the list of options. Compared to the others, it has a considerably higher Elastic Modulus which gives it a better ability to stay stiff. 

<img width="338" height="17" alt="Screenshot 2026-09-15 151220" src="https://github.com/user-attachments/assets/9cfef95a-8d23-4ba6-9599-1d1e464a8278" />

>[ABS](https://www.specialchem.com/plastics/guide/acrylonitrile-butadiene-styrene-abs-plastic)

<img width="372" height="70" alt="image" src="https://github.com/user-attachments/assets/728c2a42-619b-4037-a7e4-44b95a0de906" />

> [PLA vs. PETG](https://store.sunlu.com/blogs/products-knowledge/a-comprehensive-comparison-pla-vs-petg-in-3d-printing)


When designing, there is a safety factor of 3 to take into account, and we were instructed to neglect the weight of the motor.

___Research the design of different motor mounts and place the links in an appendix on your page. Make justifiable aproximations in your design to simplify your analysis. (ie. use the beam calculations) .____nnnmmn

Finally, we are meant to follow Appendix B for the initial approach when setting up the design analysis

<img width="263" height="314" alt="Screenshot 2026-09-15 231143" src="https://github.com/user-attachments/assets/f0ee0cf6-8fea-4d94-a894-55b747c27180" />


> Appendix B

## Feature 1

<img width="230" height="86" alt="Screenshot 2026-09-15 231150" src="https://github.com/user-attachments/assets/13558271-18d7-4199-93fe-4eff33092082" />

### a. List all the knowns and unknowns.
When acessing the link  for the gear motor, luckily there are already specifications such as the diameters and sizes of the gearbox. we will add those to our knowns 

<img width="211" height="140" alt="image" src="https://github.com/user-attachments/assets/02d84be6-e697-4aab-897f-6e0abd282776" />

+ On top of that we know...
  + Applied load: P = 300 N
  + Safety Factor: N = 3
  + Max Allowed deflection: δmax = .30 mm
  + PLA young modulus: E = 3.5 GPa
  + PLA tensile strength: σy = 58 MPa

+ Some Unknowns...
  + σmax = max bending stress
  + δmax = max tip deflection

Since we are meant to design this beam, i figured I'd use the existing features of the gear to make up my dimensions. So far i know that the size of the motor is motor 38 mm, and the length of the gearbox is 36.6. 

38 + 36.5 = 74.6 mm

hence, i decided I'd make the length of my beam to be 80 mm to provide some extra room when adding the mount.
 
### b. Sketch a FBD of the feature.

*pic*

### c. Model the equations and symbolically solve.
Based off my free body diagram, the example we did in class does not resemble this project. after consulting the lecture slides, the proper deflection equation would actually be 
<img width="545" height="293" alt="image" src="https://github.com/user-attachments/assets/a2098e67-9ac4-4fa9-a853-8f4b51603022" />

Using this information i used it to calculate symbolically 

*pic*

### d. Numerically solve for the cross-sectional geometry.   

After calculating the allowable stress, i got an allowable stress of 19.33 MPa. 

By this step i realized that i had more unknowns than what i have previously predicted. In order to solve for both the bending stress and deflection, i would need to find out both the base and height of my cross section. After consolidating with the lecture notes, it appears i did the steps correct however the unknown of b was th eonly thing we were meant to look for. SInce we are technically meant to design the beam i gave myself the liberty of assigning whatever height since in the class example height was provided. therfore I selected a beam height of h = 35 mm. I then used my new information to solve for the minimum required beam width b. 

*pic*

after numerically solving, i finally was able to compare my allowed stress to my max, and luckily with my first attempt the design passed the stress requirement which allowed me to continue on my design. 

##  Feature 2

<img width="182" height="137" alt="Screenshot 2026-09-15 231155" src="https://github.com/user-attachments/assets/b2ee1368-e07a-4b11-a70b-3e28d8800819" />

### a. List all the knowns and unknowns.
Similarly to the steps taken in fature one, i repeated the process of finding the knowns and unknowns necessary to solving the wall attached portion of this design. SO far 

we know...
  + Applied load: P = 300 N
  + Safety Factor: N = 3
  + Max Allowed deflection: δmax = .30 mm
  + PLA young modulus: E = 3.5 GPa
  + PLA tensile strength: σy = 58 MPa
assuming we will be using the same length as before
  + Length: L = 80 mm

+ Some Unknowns...
  + σmax = max bending stress
  + δmax = max tip deflection
  + b =
  + I = 

### b. Sketch a FBD of the feature.
### c. Model the equations and solve them symbolically.
### d. Numerically solve for the cross-sectional geometry.

## Sketch


## 3D CAD mode
+ a. Design features on the motor mount to minimize deflection.
+ b. Where appropriate, use parametric modeling techniques to design.
+ c. Create clearance holes for the shaft and bolts (3.4 mm clearance holes for bolts).

## Appendix

