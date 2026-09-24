# A5 – [Topic]

## Objective

Detail design a bracket, using the concept design in Appendix B, to hold a horizontal force applied symmetrically by a strap outline in resource #1. The bracket’s dimensions are designed with different fit classes. Each dimension of the T beam is part of the fit:

“a” intention for use where accuracy is not essential
“b” is about the closest fits that can be expected to run freely
“c” is where accurate location and minimum play is desired

<img width="398" height="305" alt="Screenshot 2026-09-22 205002" src="https://github.com/user-attachments/assets/3a990a89-adae-4d6f-9bb4-8b8a3df7f058" />

> appendix b



Design using a safety factor of 4 and applied load in between 500 lbf < F < 800 lbf. Choose one of three metals, aluminum 6061 T6, Steel (ASTM A36), or Titanium (Ti-6Al-V4). Furthermore, state assumptions and approximations about the design in order to use fundamental strength of materials analysis. For example, use the proper stress analysis and deflection analysis where appropriate. Assume no failure due to direct shear stress. 

<img width="1338" height="611" alt="image" src="https://github.com/user-attachments/assets/2a063384-5979-40a3-b3f2-b59eea513e41" />


## 1. Stress Analysis

The material I decided to go with was steel as i The yield stress of ASTM A36 steel is 36,000 psi, 250 MPa. Since the force was given in lbf we will stick wwith the psi units so it will convert correctly. Since we are meant to design applied load in between 500 lbf < F < 800 lbf, i decided to choose the medium allowable strength of 650 lbf. Using the available information, i make sure to list my knowns and unknowns in order to solve for a stress analysis. SInce the Design consist of 5 parts, i will be generating Free Body DIagrams for each dimension accordibgly to the stress analysis being done. Since we easily have the yeild strength and safety factor, we can easily calculate the allowed stress by dividg 36000 by 4m which gives us 9,000 psi. 

One thing i made sure to do was that is a stumled along something with inconsistent units, i made sure to convert it before it got into my mathematical solving. 

In the process of solving these i recognized that we arepretty much solving this with no dimensions. Therefore i took the liberty of making up numbers and start with unknown dimensions to eventually solve for the minimum dimensions needed to survive the load. 

### Feature A
<img width="464" height="262" alt="Screenshot 2026-09-24 050722" src="https://github.com/user-attachments/assets/09cdf869-f499-4dd3-b5ce-295383e18c10" />

### Feature B
<img width="446" height="258" alt="Screenshot 2026-09-24 050736" src="https://github.com/user-attachments/assets/51b86982-a029-45a2-b252-124161cd00c5" />

### Feature C
For feaure C, in the appendix A it appears that the cylinder is potruding/ appears to be loger than the rest f the design.SO i reduced the assumed length of 2 inches down to 1.5 in. I also wasnt condient with my previous attempt at solving because i ended up with a potential of two areas ad i didnt know which one to decide more valid than the other. i figured it would be the first calculation because it doesnt use the hypothetical width i assigned it, but that wouldnt explain why the area is less than the thickness we solved numerically. 

<img width="467" height="252" alt="Screenshot 2026-09-24 050748" src="https://github.com/user-attachments/assets/368d610f-0eb2-4d74-a921-edbe2b484e45" />

### Feature D
Same goes here for feature D, i figured id keep shrinking it by incriments so i have settled on a lenth of 1 inch. I essemtiay followed th same steps as C on E and D. the mist idficuly part was parts a b and c because of the many unknowns. they essentially act as setting stone for the future problems

I'm the previous Fbd i had 2 forces visible, but since both features D and E appear on two sides of the design, i decided to half the load which ca be justified by the symmetrical fixes. 

<img width="467" height="257" alt="Screenshot 2026-09-24 050800" src="https://github.com/user-attachments/assets/66a6d7a2-f6aa-4643-84b2-93316a22e9f7" />

### Feature E
<img width="462" height="257" alt="Screenshot 2026-09-24 050809" src="https://github.com/user-attachments/assets/8255504b-b415-48c9-84db-63092bfd4a5a" />

 
## 2. Stiffness Analysis

### Feature A
<img width="326" height="180" alt="image" src="https://github.com/user-attachments/assets/3eaccd74-19f8-4222-a761-17d9f96597a0" />

### Feature B
<img width="323" height="164" alt="image" src="https://github.com/user-attachments/assets/9360153c-8299-4bf8-a136-d750c10969e6" />

### Feature C
<img width="327" height="168" alt="image" src="https://github.com/user-attachments/assets/ae93d21b-f326-46f7-8f9b-a8a280c6db85" />

### Feature D
<img width="326" height="179" alt="image" src="https://github.com/user-attachments/assets/53f1b40b-bacc-4cf2-abfa-6d0e16c88b33" />

### Feature E
<img width="326" height="170" alt="image" src="https://github.com/user-attachments/assets/2fee5a58-8e7d-4cd6-9802-da384ed6a6e4" />


## 3. Multiview Sketches 


## 4. Lessons Learned 

### a. Governing failure mode

### b. Error propagation 

### c. Assumption sensitivity



## Appendix

