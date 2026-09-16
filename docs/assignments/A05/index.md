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
  + Length: L = 80 mm
  
+ Some Unknowns...
  + σmax = max bending stress
  + δmax = max tip deflection


 
### b. Sketch a FBD of the feature.

Since we are meant to design this beam, i figured I'd use the existing features of the gear to make up my dimensions. So far i know that the size of the motor is motor 38 mm, and the length of the gearbox is 36.6. 

38 + 36.5 = 74.6 mm

hence, i decided I'd make the length of my beam to be 80 mm to provide some extra room when adding the mount. As for where my load will be applied, i calculated my moment around the length of the shaft which is 18 mm. Despite the ambiguity of the motor's specifications, the shaft is the only size included that mentions length, so i decided to use that as my distance. Adding it into my diagram, it gave me my calculated moment of 5400 N * mm 

*pic*

### c. Model the equations and symbolically solve.
Since the appendix b feature of the beam includes a moment, the equation i decided to go with was a moment acting upon the cantilver beam, which allows me to use the same equation we did an example on in class. 

When it came to the step of solving symbolically, i realized that i had more unknowns than what i have previously predicted. In order to solve for both the bending stress and deflection, i would need to find out not only the length (which i calculated above) but also the base *and* height of my cross section. After consolidating with the lecture notes, it appears i did the steps correct. SInce we are technically meant to design the beam i gave myself the liberty of assigning whatever height and base since in the class example height was provided. therfore I selected a height of base = 35 mm and a height of 10 mm. Since the base is meant to be wide enough to carry the motor, i noticed that it has a diameter of 28 mm. The 35 mm size allows some leeway where it rests. The height didnt take up much thought, i assigned it a simple 10 mm

so now we have 
+ Base: b = 35 mm
+ Height: h = 10 mm


I then used my new information to solve for the minimum required beam width b. 

*pic*

However my chosen height proved to exceed the max deflection. i decided to double it nd make it 20 mm instead. 
Youll also see that i tried numerically solving for ase instead of assigning it a number, however, those numbers also exceeded my max so i decided to stick with my original method. 

+ NEW Height: h = 20 mm

### **UPDATE**

this will make sense after reading feature 2, but i applied my new knowlegde of having to discover the height. So i stuck with a base of __ and kept my length 80. I discovered this was because i tried solving for base instead of height and has my equation all wrong which messed with my calculations. Using the symbolically solved equations in part b of feature 2, the NEw height i got was ___. However when i solved using 80 mm lentgh, i got a abundanley large number of a height of 58 which is unrealistic. And this is where the project confuses me because i keep going back and forth. When thinking about it realistically, a short length mount wont be able to carry something larger. However for the sake of my cslculations, i decided to proceed but with another length. When deciding this length, i simply just played with numbers on my calculator until i settled with a acceptable number, and it ended up being 20. 

*NEW picture*

### d. Numerically solve for the cross-sectional geometry.   

After calculating the allowable stress, i got an allowable stress of 19.33 MPa. 


*pic*

after numerically solving, i finally was able to compare my allowed stress to my max, and luckily with my first attempt the design passed the stress requirement which allowed me to continue on my design. 

##  Feature 2

<img width="182" height="137" alt="Screenshot 2026-09-15 231155" src="https://github.com/user-attachments/assets/b2ee1368-e07a-4b11-a70b-3e28d8800819" />

### a. List all the knowns and unknowns.
Similarly to the steps taken in fature one, i repeated the process of finding the knowns and unknowns necessary to solving the wall attached portion of this design. SO once again i took the liberty of asigning it anotherlength, this time 50 mm. I learned that from the last example, you need to specify one cross-sectional dimension before you can solve for the other. Therefore i went for a practical width b = 10 mm for the sake of finding required height

we know...
  + Applied load: P = 300 N
  + Safety Factor: N = 3
  + Max Allowed deflection: δmax = .30 mm
  + PLA young modulus: E = 3.5 GPa
  + PLA tensile strength: σy = 58 MPa
  + Length: L = 50 mm
  + Base: h = 10 mm

+ Some Unknowns...
  + σmax = max bending stress
  + δmax = max tip deflection
  + Inertia: I = ?

### b. Sketch a FBD of the feature.
As shown in the diagram above, i ureferenced that when designing my cantilever. I treated the wall above it as the rigid support and  the lower section of Feature 2 as the cantilever. In this design i am including my predetermined 


### c. Model the equations and solve them symbolically.

### d. Numerically solve for the cross-sectional geometry.
this section asks for the cross sectional geometry, so i decided to take another approach when solving. 

From here i got a maximum length of 25 mm that passed both stress and deflection requirements. SO therefore my cross section is offically 25 x 10 mm. 

Now that i learned from this mistake, i went back to my figure one and plugged my discovery into these new equation 

## Sketch

 I am very aware that my hand calculations lengths do not translate well, especially since they are meant to carry this gear.If i were to solve it the way i initially did with feature one, using my predetermined lengths, maybe i wouldve gotten something out of it. However, im only really upset about feature 2 having a shorter base then its height. Im hoping that swapping the numbers will essentially be fine. 

The criteria for this sketch portion was that we had to determine the dimensions from the previous problems. However in my CAD design i will definitley make the wall plate wider than the 10-mm width because we need room for the four bolts.

## 3D CAD mode
I then created the model in solidowkrs.  I started off by going into the equations tab and addig all my calculated numbers as parameters so that everything was fixed. this is the graph i ended up with. Only until it came to designing my cad did i realize that i dumbly chose two different bases, knowing that this was an attached piece. However i was too dar into this project to want to go back and calculate for a difference so i simply just increased what i had. If i continue with this my design will fold in on itself. so i decided to double down on the initial length i had when veryfirst designing, which was 80 mm. 

<img width="341" height="295" alt="image" src="https://github.com/user-attachments/assets/ad0134a6-f657-4517-95df-be0e7797cf37" />

i sketched the first part in th front plane then went onward to the top plan to draw feature 2 .

and as you can see, with the new implemented length of feature one, i can keep feature 2's height. which lesves me with this design 

<img width="390" height="305" alt="image" src="https://github.com/user-attachments/assets/52e86cfd-4f17-405d-983c-907b81aed9e4" />



+ a. Design features on the motor mount to minimize deflection.
+ b. Where appropriate, use parametric modeling techniques to design.
+ c. Create clearance holes for the shaft and bolts (3.4 mm clearance holes for bolts).

## Appendix

