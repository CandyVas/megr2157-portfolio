# A6 – [Bracket Drawing]
Download my CAD files here! 

[Bracket Solid Model](https://drive.google.com/file/d/1GgQWCIwWzx3vZQ0zwyOpJ5hfY6XAedJE/view?usp=drive_link)

[Bracket Drawing](https://drive.google.com/file/d/1DViOjW9j3nBZgAKWtZuzzuWriehEhukw/view?usp=drive_link)

## Parametric Design

For this assignment, I was given the option to design the solid model based on either the stiffness or strength analysis from the previous assignment. I chose to use the strength analysis because my stiffness analysis produced a large range of calculated feature dimensions, from approximately 0.0028 in to 0.490 in. This variation would have resulted in features with much different thicknesses and would have made the final design less practical to model as a bracket. Using the strength analysis provided a more consistent basis for determining the required feature dimensions.

When entering the calculated values into SolidWorks, I made sure that the document units were set to IPS (inch, pound, second). This ensured that the dimensions and equations were consistent with the calculations from the previous assignment, which were solved for inches and pounds.

Because this assignment required a parametrically designed solid model, I decided not to simply sketch the bracket using manually calculated dimensions. Instead, I used SolidWorks Global Variables and equations to control the dimensions of the model. This allowed the dimensions to reference analytical equations rather than relying solely on manually entered values.


<img width="640" height="359" alt="Screenshot 2026-09-29 213906" src="https://github.com/user-attachments/assets/fc3d46c9-15bb-42c4-a937-d9a61a428a07" />

For Features A and B, I was able to create relatively concise equations because each dimension could be calculated directly from the loading and allowable stress. Features C, D, and E, however, required several intermediate calculations. Although these equations were longer, I kept them in the model because they maintained the relationship between the analytical calculations and the CAD geometry.


### Feature A

I began the CAD model with Feature A and worked through the features in chronological order. For Feature A, I used the calculated diameter as a parametric dimension and assigned the feature length based on the specified 2.00 in dimension. The diameter was determined from the bending stress relationship for a circular cross section, which could be found in my picture above. 

<img width="445" height="264" alt="image" src="https://github.com/user-attachments/assets/30255dcc-2c2f-4fab-9be6-941d506989a4" />
<img width="706" height="365" alt="image" src="https://github.com/user-attachments/assets/50a445b5-2f38-46c5-9f85-4185e43d9fa7" />

### Feature B
Feature B was created as the connecting geometry between the surrounding features. Its dimensions were related to the calculated dimensions of the adjacent geometry. As discussed in my previous assignment, the width of Feature A transfers into Feature B because the two features are connected.

<img width="374" height="340" alt="Screenshot 2026-09-29 213925" src="https://github.com/user-attachments/assets/ed1f7f6d-fef0-4b21-8192-d087c7fd4cd3" />
<img width="692" height="350" alt="image" src="https://github.com/user-attachments/assets/7583143f-418d-4d39-b229-55463f84161d" />


<img width="150" height="150" alt="Screenshot 2026-09-29 214325" src="https://github.com/user-attachments/assets/23cce1ea-88a3-45ee-b93a-13f4d6ca1daa" />
<img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/5f257ac0-b40f-4c3a-90e6-7da26dca2354" />

### Feature C 
For Feature C, I used the width of 2.00 in, the specified feature length of 1.50 in to find the calculated height hC. The calculated value was then used to control the height of Feature C. 

<img width="347" height="296" alt="image" src="https://github.com/user-attachments/assets/5d741461-da14-4f1c-8680-57c238353b23" />
<img width="702" height="350" alt="image" src="https://github.com/user-attachments/assets/6450c7ce-f48c-4efb-9ca5-b8aba60ee4af" />

### Feature D 
<img width="632" height="401" alt="image" src="https://github.com/user-attachments/assets/f2cac053-a1aa-4ff4-8d46-305d76f368fb" />

I began to struggle interpreting the rest of the bracket by feature D. When reviewing Appendix C from Assignment A5, I had difficulty determining whether Feature D was to be positioned on top of Feature C or to the side of it. In the provided geometry, Feature C appeared to be cut down to the inside base, while Feature D did not appear to include the same cut underneath it. So I just modeled both interpretations to compare their effects on the overall bracket geometry.

<img width="461" height="340" alt="Screenshot 2026-09-30 003043" src="https://github.com/user-attachments/assets/d3f7143f-5b1f-491c-8b80-8af3f0621961" />
<img width="272" height="332" alt="image" src="https://github.com/user-attachments/assets/91173626-ccad-44e8-be4d-5421a34b8d76" />

> TOP - When positioned on top of Feature C, the width became too large. This got in the way of space required for Feature D, which extends inward.

<img width="341" height="314" alt="image" src="https://github.com/user-attachments/assets/6a10c41e-826b-4a7b-9281-decf2def09cf" />

> SIDE - When positioned on the side of Feature C, the resulting height was too short (same height as feature C) meaning it didn't extend up any further like in the Appendix. 

<img width="124" height="226" alt="image" src="https://github.com/user-attachments/assets/da420f27-e7a8-4ef8-8883-4457f8210e46" />
<img width="751" height="340" alt="image" src="https://github.com/user-attachments/assets/0cc2fc2d-543e-4773-80ac-af88ee9edcd5" />

> MY SOLUTION


### Feature E
<img width="547" height="269" alt="image" src="https://github.com/user-attachments/assets/cf21596f-1344-4488-a4e3-1dcd5a56b463" />
<img width="377" height="323" alt="image" src="https://github.com/user-attachments/assets/e59506fb-5c8c-472b-9a6a-92dc59cc4ce9" />

### Final CAD
After completing Features A through E, I combined the features into the final bracket model.

<img width="245" height="221" alt="Screenshot 2026-09-30 005107" src="https://github.com/user-attachments/assets/f2d5f9d8-7992-4c83-9318-49a03ac94d8c" />
<img width="257" height="228" alt="image" src="https://github.com/user-attachments/assets/466ee620-0eca-408e-9eb1-86a3e6843ad7" />

### Drawing

After completing the model, I generated a fully dimensioned multiview engineering drawing in SolidWorks. The drawing was created using third-angle projection, with the front, top, and right-side views.

<img width="491" height="378" alt="image" src="https://github.com/user-attachments/assets/0e5fe78b-407a-4899-9c7c-d5b133a4ee74" />

## Lessons Learned

One of the main lessons I learned from this assignment was the importance of connecting analytical calculations to the CAD model rather than treating the calculations and modeling as separate processes. In the last assignment, I calculated the required dimensions from the strength analysis. In this assignment, I used those calculations to create a parametric model in SolidWorks. This showed me how an analytical design can be translated into a CAD model while maintaining relationships between dimensions.

Another lesson was the importance of using appropriate tolerances and how it should be related to the function of the feature. A sliding-fit surface would require more control, while non-functional features can generally accept a larger dimensional variation.

I've spent about 4 and a half hours were spent on the assignment. 

## Analytical Equation
One of the analytical equations used to directly control my CAD model was the bending-stress equation for Feature A. For a circular cross section i used  ( ( 32 * "M" ) / ( pi * "Sallow" ) ) ^ ( 1 / 3 ) Instead of calculating the diameter separately and manually entering that value into the sketch, I entered the relationship into the SolidWorks Global Variables/Equations system. The CAD dimension for the diameter was then linked to that variable. This allowed the CAD model to respond automatically if an input such as the applied load, safety factor, yield strength, or allowable stress were changed. The relationship between the analytical calculation and the CAD dimension are then maintained within the model.

## Tolerances 
For the tighter tolerance example, I used the dimension 1.00 ± 0.0005. This dimension is connected with the sliding-fit of the bracket and the T-beam. So because this is functional surface, the dimensional variation directly affects the clearance between the two components. That would mean a tighter tolerance is therefore more appropriate because a large variation could change the intended fit. If the opening becomes too small, interference could occur or if it becomes too large, the bracket could have excessive movement relative to the T-beam.

Whereas for my looser tolerance, I used 1.50 ± 0.02. Since the dimension does not control the sliding fit or another relationship. So because this feature does not affect the function of the bracket, a larger tolerance of ±0.02 in is sufficient. Applying a tighter tolerance would provide little benefit while making the feature more difficult and more expensive to manufacture.

