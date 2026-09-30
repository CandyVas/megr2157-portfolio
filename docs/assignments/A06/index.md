# A6 – [Topic]

## Parametric Design
_For each feature, determine the appropriate dimension from the last assignment. Generate a parametrically designed solid model based on either the stiffness or strength analysis from the previous assignment. Show images of each designed dimension as a parameter in CAD._

Sin w wr givn th option to design a solid modelbased on either the stiffness or strength analysis from thr previous assignmeny, i decided to go with stress. I decided on stress because of the large discrepencies i  had on my stiffness analysis. i had my range went from .0028 to .490 which was not ideal if the purpose fo this assignment is to design. The features would come out too thin compared to another. When inputting these values into solidowrks, i ensured that the setting was set to IPS so there would be no discrepencies in conveting since all my solved answers r in inches


since this assignment asls for a parametrically designed solid model,  instead of straight sketching with my determined numbers, ik decided to go into solidworks global variables and analytical equations to control the bracket dimensions in SolidWorks. This allowed the dimensions of the model to reference **equations** instead of only using manually entered values. This can also help reconfirm my work and whether or nto it was done correctly. Vice versa, if i i get an incorrect result will help me know if i input an incorrect value/equation. 

<img width="640" height="359" alt="Screenshot 2026-09-29 213906" src="https://github.com/user-attachments/assets/fc3d46c9-15bb-42c4-a937-d9a61a428a07" />

for features a and b i was able to make pretty consice equations, however features c d and e became very lengthy and included muliple parts in order to solve the next. As inconvenient as it was i didnt see it a big enugh issue to need to shorten it down so i continued on. 


### Feature A
From here i was finally able to model it in CAD! I deicded i might as well work in chronological order, so i started off with Feature A and used its calculated diameter and length as parametric dimension, along with the extruded length which i assigned to be 2 in

<img width="445" height="264" alt="image" src="https://github.com/user-attachments/assets/30255dcc-2c2f-4fab-9be6-941d506989a4" />
<img width="706" height="365" alt="image" src="https://github.com/user-attachments/assets/50a445b5-2f38-46c5-9f85-4185e43d9fa7" />

### Feature B
The connecting geometry was positioned using a dimension related to the surrounding calculated features, which in my A5 i mentioned how the width from feature a transferred to B since they are attached 

<img width="374" height="340" alt="Screenshot 2026-09-29 213925" src="https://github.com/user-attachments/assets/ed1f7f6d-fef0-4b21-8192-d087c7fd4cd3" />
<img width="692" height="350" alt="image" src="https://github.com/user-attachments/assets/7583143f-418d-4d39-b229-55463f84161d" />


<img width="150" height="150" alt="Screenshot 2026-09-29 214325" src="https://github.com/user-attachments/assets/23cce1ea-88a3-45ee-b93a-13f4d6ca1daa" />
<img width="150" height="150" alt="image" src="https://github.com/user-attachments/assets/5f257ac0-b40f-4c3a-90e6-7da26dca2354" />

### Feature C 


i used w =2 and lC for a length of 1.5 and extruded hc

<img width="347" height="296" alt="image" src="https://github.com/user-attachments/assets/5d741461-da14-4f1c-8680-57c238353b23" />
<img width="702" height="350" alt="image" src="https://github.com/user-attachments/assets/6450c7ce-f48c-4efb-9ca5-b8aba60ee4af" />

### Feature D 
<img width="632" height="401" alt="image" src="https://github.com/user-attachments/assets/f2cac053-a1aa-4ff4-8d46-305d76f368fb" />

When getting to featue D i had a hard time identifying whether or not feature D was on top of feature C, oe off to the side. In appendix c provided in the A5 assign,ent, youll see that the C bracket is cut off to only be the inside base. But then bracket D does not include the cut underneath. I attempted both manners, neither coming out with desirable outcomes. Suide by side the height i got was too short, whereas on top the width was too thick, meaning there would be no room for part B which extends inwards. Therefore i found a workout 

<img width="461" height="340" alt="Screenshot 2026-09-30 003043" src="https://github.com/user-attachments/assets/d3f7143f-5b1f-491c-8b80-8af3f0621961" />
<img width="272" height="332" alt="image" src="https://github.com/user-attachments/assets/91173626-ccad-44e8-be4d-5421a34b8d76" />

> on top

<img width="341" height="314" alt="image" src="https://github.com/user-attachments/assets/6a10c41e-826b-4a7b-9281-decf2def09cf" />

> on the side

<img width="124" height="226" alt="image" src="https://github.com/user-attachments/assets/da420f27-e7a8-4ef8-8883-4457f8210e46" />
<img width="751" height="340" alt="image" src="https://github.com/user-attachments/assets/0cc2fc2d-543e-4773-80ac-af88ee9edcd5" />

> my solution


### Feature E

Onto the last feature, i once again followed appendix C and built feature E on top of feature D. 
<img width="547" height="269" alt="image" src="https://github.com/user-attachments/assets/cf21596f-1344-4488-a4e3-1dcd5a56b463" />
<img width="377" height="323" alt="image" src="https://github.com/user-attachments/assets/e59506fb-5c8c-472b-9a6a-92dc59cc4ce9" />

### Final CAD
<img width="245" height="221" alt="Screenshot 2026-09-30 005107" src="https://github.com/user-attachments/assets/f2d5f9d8-7992-4c83-9318-49a03ac94d8c" />
<img width="257" height="228" alt="image" src="https://github.com/user-attachments/assets/466ee620-0eca-408e-9eb1-86a3e6843ad7" />

### Drawinf

Here i have generated a fully dimensioned multiview drawing in CAD with engineered tolerances. 


(10%) Make sure drawing is laid out in third angle projection (symbol recommended but not required).
(20%) The tolerances for the gap need to be observed in your drawing and should match your fit tolerances.
(5%) Include a tolerance block.
X.X ± .02
X.XX ± .01
X.XXX ± .005
Reflections
(10%) Detail engineering lessons learned from both parts of the assignment and be specific. Eliminate words like good and bad from this section. Be more articulate. Document time spent.
(5pt) Identify the analytical equation (stiffness or strength) you used to drive at least one dimension in your parametric model, and name which specific dimension it controlled. Describe how you expressed that equation directly in the CAD software (e.g., as an equation/expression tied to the parameter) rather than typing in a value you calculated by hand elsewhere. If your calculation changed later in the assignment, describe exactly what happened to that dimension and whether the rest of the model responded on its own or required manual rework.
Pick one dimension on your drawing where you applied a tighter tolerance class (e.g., X.XXX ± .005) and one where you applied a looser class (e.g., X.X ± .02). For each, identify whether that feature is a mating/functional surface (like a sliding fit interface) or a non-critical feature, and explain why that functional role justified the tolerance class you chose. If you applied the tightest tolerance across your drawing by default, describe what happens to manufacturing cost or feasibility when a non-critical feature is held to an unnecessarily tight tolerance.



## Communicate

