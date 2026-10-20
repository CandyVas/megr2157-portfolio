# A7 – [Topic]

## Objective

+ Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.
+ Ensure high stiffness, strength, and lightweight optimization through iterative design.
+ Conduct multiple FEA simulations, refining geometry based on results.
+ Perform static stress analysis, including constraints, loading, and meshing selection.
+ Interpret data by identifying max stress, displacement, and safety factors.
+ Optimize the design by modifying geometry to enhance performance.
+ Document the entire process with images, calculations, and insights.
+ Reflect on key engineering lessons learned and time spent.

## Tabulate each outer loop iteration after convergence using the table below

|  | Design I | Design II | Design III |
| --- | --- | --- | --- |
| Max Stress and location | Row 1, Col 2 | Row 1, Col 3 | Row 1, Col 4 |
| Max deflection and location | Row 2, Col 2 | Row 2, Col 3 | Row 2, Col 4 |
| mass | Row 3, Col 2 | Row 3, Col 3 | Row 3, Col 4 |
| Safety Factor | Row 4, Col 2 | Row 4, Col 3 | Row 4, Col 4 |
| Number of elements | Row 5, Col 2 | Row 5, Col 3 | Row 5, Col 4 |

### Instructions

Your task is simply to create a high stiff, high strength, and lightweight component. Use Finite Element analysis to drive your decision making process throughout your design. Each step of the analysis and before you make geometric changes make sure the component’s results (stress/displacement/Safety Factor) converge on a 7% difference. Achieve this by modifying the number of elements. If after three attempts to converge use the stiffness and stress from the finer mesh size use the finest mesh size and proceed through the process.

Outline:
Assuming the bracket already has a material assigned to it. (Do not change the material.) The workflow for the component design has an outer loop and an inner loop. The inner loop’s function  is to validate the results. The outer loop’s function is for the geometry design optimization.

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
