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

The material I decided to go with was steel, as the yield stress of ASTM A36 steel is 36,000 psi, or 250 MPa. Since the force was given in lbf, we will stick with the psi units so everything will convert correctly. Since we are meant to design for an applied load between 500 lbf < F < 800 lbf, I decided to choose the medium allowable strength of 650 lbf.

Using the available information, I made sure to list my knowns and unknowns in order to solve for a stress analysis. Since the design consists of 5 parts, I will be generating Free Body Diagrams for each dimension according to the stress analysis being done. Since we are given the yield strength and safety factor, we can easily calculate the allowable stress by dividing 36,000 by 4, which gives us 9,000 psi. 

One thing I made sure to do was that if I stumbled along something with inconsistent units, I made sure to convert it before it got into my mathematical solving.

In the process of solving these, I recognized that there were no dimensions given. Therefore, I took the liberty of making up numbers and starting with unknown dimensions to eventually solve for the minimum dimensions needed to withstand the load.

### Feature A
<img width="464" height="262" alt="Screenshot 2026-09-24 050722" src="https://github.com/user-attachments/assets/09cdf869-f499-4dd3-b5ce-295383e18c10" />

### Feature B
<img width="446" height="258" alt="Screenshot 2026-09-24 050736" src="https://github.com/user-attachments/assets/51b86982-a029-45a2-b252-124161cd00c5" />

### Feature C
For Feature C, in Appendix A, it appears that the cylinder is protruding and appears to be longer than the rest of the design. So, I reduced the assumed length of 2 inches down to 1.5 inches.

I also wasn't confident with my previous attempt at solving because I ended up with a potential of two areas, and I didn't know which one to decide was more valid than the other. I figured it would be the first calculation because it doesn't use the hypothetical width I assigned it, but that wouldn't explain why the area is less than the thickness we solved numerically.


<img width="467" height="252" alt="Screenshot 2026-09-24 050748" src="https://github.com/user-attachments/assets/368d610f-0eb2-4d74-a921-edbe2b484e45" />

### Feature D
The same goes here for Feature D. I figured I would keep shrinking it by increments, so I have settled on a length of 1 inch. I essentially followed the same steps as C on E and D. The most difficult part was Parts A, B, and C because of the many unknowns. They essentially act as stepping stones for the future problems.

In the previous FBD, I had two forces visible, but since both Features D and E appear on two sides of the design, I decided to halve the load, which can be justified by the symmetrical features. Therefore, each side would experience half of the total 650-lbf load which gives 325 lbf, which allows me to use the appropriate applied loads. 

<img width="467" height="257" alt="Screenshot 2026-09-24 050800" src="https://github.com/user-attachments/assets/66a6d7a2-f6aa-4643-84b2-93316a22e9f7" />

### Feature E
<img width="462" height="257" alt="Screenshot 2026-09-24 050809" src="https://github.com/user-attachments/assets/8255504b-b415-48c9-84db-63092bfd4a5a" />

 
## 2. Stiffness Analysis
For the stiffness analysis, we were given a maximum allowable deflection of 0.005 in. We were also given the same assumption that shear shear deflections were negligible. Based off the load distributions i saw fit, i assigned them their equation to solve for deflection as well as moment o inertia. 

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

For the multiview sketches, I used the dimensions calculated from the stress and stiffness analyses above and applied them to my draw design. The multiview helped visualize the bracket from different directions and to ensure that the dimensions were consistent. 

<img width="487" height="292" alt="image" src="https://github.com/user-attachments/assets/146a9914-5f7e-4f8c-b507-6aea935df421" />

## 4. Lessons Learned 

### a. Governing failure mode
For Feature E, stress governed the design. The stress analysis required a minimum height of 0.329 in, while the stiffness analysis required .0024 in to keep the deflection below 0.005 in. Perhaps this was due to an error on my end of the work for it to come out so drastically different. However, if we were to work off these numbers alone, the stress requirement would control the final dimension. This is because the two requirements are nowhere near close, and since the stress requirement is larger, it governs the final dimension.

### b. Error propagation 
I struggled with this throughout the assignment, especially because the load is transferred from one feature to the next, and i had a difficult time making assumptions for each feature due to the fact that they all connected. This is particularly true with the reaction forces from the symmetric load split, which were carried throughout the features. An early mistake of using the full 650-lbf load instead of the 325-lbf load on each symmetric side would have trickled down into Features B–E, or vice versa. This would have increased their calculated loads and moments and could have made the final dimensions invalid.

### c. Assumption sensitivity
One important assumption was the equal load distribution between the two symmetric sides. If the strap load were not centered, one side could carry more than 325 lbf. Because of the equation M = PL, the increased load would increase the bending moment and required section modulus, resulting in larger required dimensions. Therefore, the symmetry assumption has a direct effect on the final bracket dimensions.
