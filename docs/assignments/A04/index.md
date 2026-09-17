# A4 – Motor Mount
## Objective

If you'd like to download my CAD file, you can using [this link](https://drive.google.com/file/d/11BwIIBuTp2zlIRskjAGCmuQI-3zcJ8Bv/view?usp=drive_link)

For this project, we are tasked with designing a motor mount using a [*24V DC Gear Motor](https://www.omc-stepperonline.com/brushed-24v-dc-gear-motor-3-6kg-cm-46rpm-w-99-5-1-planetary-gearbox-pa28-28245800-g100) that is meant to attach to a rigid wall under a 300 N force.

<img width="448" height="132" alt="image" src="https://github.com/user-attachments/assets/2a4df698-0af7-4709-8320-374c683521bc" />

> Motor against Wall

<img width="122" height="117" alt="image" src="https://github.com/user-attachments/assets/53fa329f-3d36-4322-881b-2dd686c46e2d" />

> 24V DC Gear Motor

We are supposed to consider both features when designing for the yield strength and then designing for a maximum deflection of 0.30 mm at the free end. We were given the option of selecting a material between ABS, PETG, or PLA as a motor mount material. When making this decision, I decided to go with PLA because not only is it the material I am most familiar with, but after further research, I discovered it is also the most optimal from the list of options. Compared to the others, it has a considerably higher Elastic Modulus, which gives it a better ability to stay stiff and resist deflection.

<img width="338" height="17" alt="Screenshot 2026-09-15 151220" src="https://github.com/user-attachments/assets/9cfef95a-8d23-4ba6-9599-1d1e464a8278" />

>[ABS](https://www.specialchem.com/plastics/guide/acrylonitrile-butadiene-styrene-abs-plastic)

<img width="372" height="70" alt="image" src="https://github.com/user-attachments/assets/728c2a42-619b-4037-a7e4-44b95a0de906" />

> [PLA vs. PETG](https://store.sunlu.com/blogs/products-knowledge/a-comprehensive-comparison-pla-vs-petg-in-3d-printing)

When designing, there is a safety factor of 3 to take into account, and we were instructed to neglect the weight of the motor.

Finally, the last thing we are meant to consider is Appendix B for the initial approach when setting up the design analysis.

<img width="263" height="314" alt="Screenshot 2026-09-15 231143" src="https://github.com/user-attachments/assets/f0ee0cf6-8fea-4d94-a894-55b747c27180" />


> Appendix B

## Feature 1

<img width="230" height="86" alt="Screenshot 2026-09-15 231150" src="https://github.com/user-attachments/assets/13558271-18d7-4199-93fe-4eff33092082" />

### a. List all the knowns and unknowns.

When accessing the link for the gear motor, luckily there are already specifications such as the diameters and sizes of the gearbox. We will add those to our knowns.

<img width="211" height="140" alt="image" src="https://github.com/user-attachments/assets/02d84be6-e697-4aab-897f-6e0abd282776" />

On top of that we know...

  + Applied load: P = 300 N

  + Safety Factor: N = 3
  
  + Max Allowed deflection: δmax = .30 mm
    
  + PLA young modulus: E = 3.5 GPa
    
  + PLA tensile strength: σy = 58 MPa
  
Some Unknowns include...

  + σmax = max bending stress
    
  + δmax = max tip deflection

### b. Sketch a FBD of the feature.

Since we are meant to design this beam, I figured I'd use the existing features of the gear to make up my dimensions. So far, I know that the size of the motor is 38 mm, and the length of the gearbox is 36.6 mm.

38 + 36.5 = 74.6 mm

Hence, I decided I'd make the length of my beam 80 mm to provide some extra room when adding the mount. As for where my load will be applied, I calculated my moment around the length of the shaft, which is 18 mm. Despite the ambiguity of the motor's specifications, the shaft is the only size included that mentions length, so I decided to use that as my distance.

<img width="539" height="143" alt="image" src="https://github.com/user-attachments/assets/43c6dbc9-61b3-401a-ad8b-a509fcfb749a" />


### c. Model the equations and symbolically solve.
Since the Appendix B feature of the beam includes a moment, the equation I decided to go with was a moment acting upon the cantilever beam. This allows me to use the same equation we did an example on in class.

When it came to the step of solving symbolically, I realized that I had more unknowns than what I had previously predicted. In order to solve for both the bending stress and deflection, I would need to find out not only the length, which I calculated above, but also the base and height of my cross section.

After consolidating with the lecture notes and the projects rubric, it appears I did the steps correctly. Since we are technically meant to design the beam, I gave myself the liberty of assigning whatever height and base I wanted, since in the class example, the height was provided. Therefore, I selected a base of 35 mm and a height of 10 mm. Since the base is meant to be wide enough to carry the motor, I noticed that it has a diameter of 28 mm. The 35 mm size allows some leeway where the motor rests. The height didn't take up much thought, so I assigned it a simple 10 mm.

Some **new** knowns are...

+ Length: L = 80 mm
  
+ Base: b = 35 mm
  
+ Height: h = 10 mm

I then used my new information to solve for the minimum required beam width b. 

<img width="527" height="201" alt="image" src="https://github.com/user-attachments/assets/a56b817d-2ace-4b22-a331-cc8288b2c530" />

> You'll notice that in my symbolic solving versus numerical one, I have the equation for height here, but I tried solving for base later. Further into the document you'll find that I was doing the wrong math, so I erased my equation for base and replaced it with an attempt to find height.


### d. Numerically solve for the cross-sectional geometry.   

After calculating for the allowable stress, I got 19.33 MPa.

<img width="668" height="339" alt="image" src="https://github.com/user-attachments/assets/8b75edba-a612-4a82-b189-5dc7f7ac1825" />

This helped me to finally able to compare my allowable stress to my maximum stress. Luckily, with my first attempt, the design passed the stress requirement, which let me continue on with my design.

However, my chosen height proved to exceed the maximum allowed deflection. I decided to double it and make it 20 mm instead.

You'll also see that I tried numerically solving for the base instead of assigning it a number. However, those numbers also exceeded my maximum allowed deflection, so I decided to stick with my original method.

+ **NEW** Height: h = 20 mm

### **UPDATE**

> This will make more sense after reading Feature 2, but I applied my new knowledge of having to discover the height. I stuck with a base of 35 mm and kept my length at 80 mm. I discovered that this was because I tried solving for the base instead of the height, and I had my equation all wrong, which messed with my calculations.

> Using the symbolically solved equations in Part B of Feature 2, the new height I got was 24 mm. However, when I solved using an 80 mm length, I got an abundantly large required height of 58 mm, which seemed unrealistic.

> This is where the project started to confuse me because I kept going back and forth between the different dimensions. When thinking about it realistically, a short-length mount wouldn't necessarily be able to carry something larger because of how the load and moment would act on the beam. However, for the sake of my calculations, I decided to proceed but with another length. When deciding this length, I simply played with different numbers on my calculator until I settled with an acceptable number, and it ended up being 20 mm.

<img width="668" height="350" alt="image" src="https://github.com/user-attachments/assets/2e50806d-a761-4d4f-8cd4-f79d8a3af9f9" />

##  Feature 2

<img width="182" height="137" alt="Screenshot 2026-09-15 231155" src="https://github.com/user-attachments/assets/b2ee1368-e07a-4b11-a70b-3e28d8800819" />

### a. List all the knowns and unknowns.
Similarly to the steps taken in Feature 1, I repeated the process of finding the knowns and unknowns necessary to solve for the wall-attached portion of this design.

So, once again, I took the liberty of assigning it another length, this time 50 mm. I learned from the last example that you need to specify one cross-sectional dimension before you can solve for the other. Therefore, I went with a practical width of b = 10 mm for the sake of finding the required height.

> **EDIT** As I'm tidying up my document, I realize that here is another place I made a mistake by choosing another base length, knowing that mount features 1 and 2 are meant to attach.

We know...

+ Applied load: P = 300 N
  
+ Safety Factor: N = 3
  
+ Max Allowed deflection: δmax = .30 mm
  
+ PLA young modulus: E = 3.5 GPa
  
+ PLA tensile strength: σy = 58 MPa
  
+ Length: L = 50 mm

+ Base: h = 10 mm

Some Unknowns...

+ σmax = max bending stress
  
+ δmax = max tip deflection

+ Inertia: I = ?

### b. Sketch a FBD of the feature.

<img width="605" height="331" alt="image" src="https://github.com/user-attachments/assets/9c0d730d-6510-465a-9f92-0efd4015b90e" />

As shown in the diagram above, I treated the wall asmy rigid support and the lower section of Feature 2 as the cantilever.

### c. Model the equations and solve them symbolically.

<img width="671" height="347" alt="image" src="https://github.com/user-attachments/assets/1a8e705e-0a61-43db-aef8-38ffb53d14b2" />

### d. Numerically solve for the cross-sectional geometry.
I was not satisfied with my attempt in feature 1, so after looking at the rubric again did i see that we are meant to solve for the cross sectional geometry, so I decided to take another approach when solving.

<img width="746" height="347" alt="image" src="https://github.com/user-attachments/assets/81b47de4-066c-4148-820b-b5d8eef8ba41" />

From here, I got a maximum length of 25 mm that passed both the stress and deflection requirements. Therefore, my cross section is officially 25 × 10 mm.

Now that I learned from this mistake, I went back to Figure 1 and plugged my discovery into these new equations.

## Sketch

I am very aware that my hand-calculated results do not translate well, especially since they are meant to carry this gear. If I were to solve it the way I initially did with Feature 1, using my predetermined lengths, maybe I would have gotten something out of it. However, I'm only really upset about them not having consistent bases.

<img width="468" height="355" alt="image" src="https://github.com/user-attachments/assets/fae99b59-bf97-4bd6-ba41-e9a6b60af8a7" />

The criteria for this sketch portion was that we had to determine the dimensions from the previous problems. However, in my CAD design, I will definitely make the length in feature one to be longer to accommodate feature 2's size. As well as fix both bases to be a consistent 35 mm. 

## 3D CAD mode
I then created the model in SolidWorks. I started off by going into the equations tab and adding all my calculated numbers as parameters so that everything was fixed. This is the graph I ended up with.

<img width="503" height="157" alt="Screenshot 2026-09-16 165503" src="https://github.com/user-attachments/assets/f5f769b8-29f7-4b82-97db-1845f28f0668" />

Only when it came to designing my CAD did I realize that I had dumbly chosen two different bases, knowing that this was supposed to be an attached piece. However, I was too far into this project to want to go back and calculate for a different dimension, so I simply just increased what I had. If I continued with this, my design would fold in on itself. So, I decided to double down on the initial length I had when first designing, which was 80 mm.

<img width="406" height="266" alt="Screenshot 2026-09-16 165901" src="https://github.com/user-attachments/assets/0a44c03f-1530-492a-b118-0b6c14fbc265" />
<img width="433" height="269" alt="Screenshot 2026-09-16 170045" src="https://github.com/user-attachments/assets/8191619a-58cb-49f1-8685-401e66e8a1bd" />

<img width="341" height="295" alt="Screenshot 2026-09-16 171510" src="https://github.com/user-attachments/assets/ee45e4fd-0549-487e-8d06-cda79784f9ab" />

> In this last image, you can see my attempt to draw feature 2's height of 25mm, which exceeds the 20mm length of feature 1

<img width="279" height="313" alt="Screenshot 2026-09-16 172249" src="https://github.com/user-attachments/assets/deecc7bf-ff92-415b-8c52-e1380a0b3ad7" />

> However, with the "new" implemented length of Feature 1, I can keep Feature 2's height, which lead me to this design

<img width="390" height="305" alt="image" src="https://github.com/user-attachments/assets/52e86cfd-4f17-405d-983c-907b81aed9e4" />

<img width="343" height="332" alt="Screenshot 2026-09-16 172621" src="https://github.com/user-attachments/assets/ec9c9469-1de4-4f8e-818a-d62208ce80eb" />


<img width="562" height="340" alt="Screenshot 2026-09-17 031538" src="https://github.com/user-attachments/assets/f19aec96-3efd-4531-acc2-82398858315a" />


<img width="269" height="300" alt="Screenshot 2026-09-17 031831" src="https://github.com/user-attachments/assets/4b2689c8-ff45-4332-957c-25ff60f1f800" />


<img width="248" height="300" alt="Screenshot 2026-09-17 031846" src="https://github.com/user-attachments/assets/18f72650-deec-48e8-9f5a-f91270fed67b" />


<img width="495" height="124" alt="Screenshot 2026-09-17 032007" src="https://github.com/user-attachments/assets/df232ab5-e27b-440e-8db9-15f8b040300c" />

Despite initially starting with different numbers, I still made sure to implement parametric modeling techniques when designing this mount. By the end of this design, this was what my equations tab looked like.

This project took me approximately nine hours, simply because I kept going back and forth on whether or not I was doing this appropriately. By the time I realized the proper technique, I was too far into the project to want to go back.

I'm aware my design is very thick compared to the example provided in class, but based on my hand calculations, this is meant to minimize deflection. If I were to simply design this base and freely choose the length, height, and base, then maybe it wouldn't have been such a struggle. But the assignment did say to find the cross-sectional geometry, and that wasn't something I could simply gloss over.

However, in the rubric, it technically does not mention using the specifications of the provided gearbox, simply to consider the four clearance holes. I acknowledge that perhaps that's where I began to mess myself up and started concluding things I shouldn't have. And further into my [research](https://www.omc-stepperonline.com/nema-23-bracket-for-stepper-motor-and-geared-stepper-motor-alloy-steel-bracket-st-m2), did I discover that motor mounts are indeed not meant to be this thick.

In the future, before I blindly decide to go straight into the math, I should really consider what exactly I'm designing first. This should be pretty obvious for engineers, however, I get pretty blindsided when it comes to class assignments.

## Appendix

[ABS](https://www.specialchem.com/plastics/guide/acrylonitrile-butadiene-styrene-abs-plastic)
> Used to find the elasticity module for the material ABS

[PLA vs. PETG](https://store.sunlu.com/blogs/products-knowledge/a-comprehensive-comparison-pla-vs-petg-in-3d-printing)
> Used to compare which would be the most optimal material to use

[*24V DC Gear Motor](https://www.omc-stepperonline.com/brushed-24v-dc-gear-motor-3-6kg-cm-46rpm-w-99-5-1-planetary-gearbox-pa28-28245800-g100)
> Used to find the specifications of my designed mount

[Example Motor Mount](https://www.omc-stepperonline.com/nema-23-bracket-for-stepper-motor-and-geared-stepper-motor-alloy-steel-bracket-st-m2) 
> Used for cross referencing motor mount design and its purpose 
