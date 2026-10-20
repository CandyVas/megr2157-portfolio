# A7 – [Topic]

## Objective

Your task is simply to create a high stiff, high strength, and lightweight component. Use Finite Element analysis to drive your decision making process throughout your design. Each step of the analysis and before you make geometric changes make sure the component’s results (stress/displacement/Safety Factor) converge on a 7% difference. Achieve this by modifying the number of elements. If after three attempts to converge use the stiffness and stress from the finer mesh size use the finest mesh size and proceed through the process.

## Tabulate each outer loop iteration after convergence using the table below

|  | Design I | Design II | Design III |
| --- | --- | --- | --- |
| Max Stress and location | Row 1, Col 2 | Row 1, Col 3 | Row 1, Col 4 |
| Max deflection and location | Row 2, Col 2 | Row 2, Col 3 | Row 2, Col 4 |
| mass | Row 3, Col 2 | Row 3, Col 3 | Row 3, Col 4 |
| Safety Factor | Row 4, Col 2 | Row 4, Col 3 | Row 4, Col 4 |
| Number of elements | Row 5, Col 2 | Row 5, Col 3 | Row 5, Col 4 |

### Instructions

Outline:

Since we are modifying our previous designed bracket from Assignment #5 and #6, we are meant to keep the assigned material on the bracket that we initially started with. We were originally given the option to choose between the three metals, Aluminum, Steel, or Titanium. I intially settled on Steel which is what we will use for this stimulation. 

### First Test 
Since we are to find a high stiff, high strength, and lightweight component, i decided that my initial attempt will be using what i used when doing my hand calculations in previous FEA's. For my stimulation i will use a load of 650 lbf and work from there. 

i followed procedure similar to assignment three where we conducted an FEA on a beam. Following solidworks feature tree, i g down the menu when performing this FEA

<img width="390" height="329" alt="image" src="https://github.com/user-attachments/assets/bbd6aaeb-81e8-4f27-b0a8-a25dcb713bdd" />
> clicked on stimulation tab and created a new study

<img width="434" height="343" alt="image" src="https://github.com/user-attachments/assets/dfdb54d6-7cfe-4115-ae9d-083c44e0c67e" />

> selected on fixed geometry for thr ficture and placed them inside the bracket since it is being slotting

<img width="414" height="328" alt="image" src="https://github.com/user-attachments/assets/3bb49d1a-c5d9-4c72-a472-80f6edf88369" />

> chose external loads, force, and applied it to the cylinder which will be held by polyester strap. I made sure to convert the units to my original lbf and used my determined 650

<img width="428" height="335" alt="image" src="https://github.com/user-attachments/assets/081f47af-dbdc-4e02-a0c6-fb92825e4a60" />
<img width="398" height="344" alt="image" src="https://github.com/user-attachments/assets/34bb96de-818c-4635-b7f3-62e337a2676e" />

> FEA Test I

<img width="448" height="339" alt="image" src="https://github.com/user-attachments/assets/a507122b-9e22-4dd8-be37-75740931494c" />
<img width="471" height="335" alt="image" src="https://github.com/user-attachments/assets/d565ed17-c837-41b9-92cb-72d668925a92" />


> FEA Test II

I decided to try out both extremes of trying the course mesh then the fine mesh to hone in on what design would be best to base the rest of them off of. 

The inner loop’s function  is to validate the results. The outer loop’s function is for the geometry design optimization.

## INNER LOOP #1

|  | FEA TEST I | FEA TEST II | 
| --- | --- | --- |
| Max Stress (psi) | [8432.03 ](https://drive.google.com/file/d/1LmoA18RBS0y-WfzUCphlt8YkyB1MwGF-/view?usp=drive_link)  | Row 1, Col 3 |
| Max deflection (in) | [0.003176](https://drive.google.com/file/d/1qqbKx0bDmgthT4KH65L3eSJQ36-L8P4y/view?usp=drive_link) | Row 2, Col 3 | 
| mass (lb) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | Row 3, Col 3 | 
| Min Safety Factor | [4.3](https://drive.google.com/file/d/1rIlzJ5jylqaa2AHQpRtdf6rnpYS43JHF/view?usp=drive_link) | Row 4, Col 3 | 
| Mesh elements | [1166](https://drive.google.com/file/d/1ZSm8HjPi9pv1s8OypYy0S5V9oICioKHf/view?usp=drive_link) | Row 5, Col 3 | 

Outer Loop: Based on Design Optimization
(30% total: each time through the outer loop is 10%)

Inner Loop: Based on validation
(60% total: each time through the inner loop is 20%)

Preprocessing
Perform a static stress analysis
Select proper constraints
Select appropriate loading
Select a mesh
Computation
Solve
Data Interpretation
Review the results by tabulating the
safety factor
maximum stress and it’s location
maximum displacement and it’s location  
Error Estimation
Validate the model by repeating until either the results converge within 7% or it is the third attempt to converge.
End Inner Loop

Design Optimization
Review results to make geometric changes, adding and removing material where needed in an attempt to modify the component to be stronger, stiffer, and more lightweight than the prior solutions.
Repeat #1 through #x  a minimum of three times.
End Outer Loop

Reflections
(10%) Detail engineering lessons learned from the assignment and be specific. Eliminate words like good and bad from this section. Be more articulate. Document time spent.
For example, I learned how different size and shape meshes affect the results and the time to solve. The greater the number of meshes increases the computational time to solve.
