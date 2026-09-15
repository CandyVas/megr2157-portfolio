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

<img width="226" height="349" alt="image" src="https://github.com/user-attachments/assets/3f052ea1-f82d-446e-b114-a61c2ca3060f" />

> Appendix B

## Feature 1

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
 
### b. Sketch a FBD of the feature.


### c. Model the equations and symbolically solve.
### d. Numerically solve for the cross-sectional geometry.   

##  Feature 2

+ a. List all the knowns and unknowns.
+ b. Sketch a FBD of the feature.
+ c. Model the equations and solve them symbolically.
+ d. Numerically solve for the cross-sectional geometry.

## Sketch


## 3D CAD mode
+ a. Design features on the motor mount to minimize deflection.
+ b. Where appropriate, use parametric modeling techniques to design.
+ c. Create clearance holes for the shaft and bolts (3.4 mm clearance holes for bolts).

## Appendix
