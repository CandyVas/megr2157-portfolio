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


Since we are modifying our previously designed bracket from Assignments #5 and #6, we are supposed to keep the same material that we originally chose. We were given three options: aluminum, steel, or titanium. I initially decided to use steel, so I will continue using steel for this simulation and the rest of my design changes.

### First Test 
Since I wanted to start with something familiar, I decided to use the same 650 lbf load that I used in my previous hand calculations and FEA work. This gave me a starting point to see how the original bracket would perform before making any changes. I applied the force to the cylindrical section of the bracket where the polyester strap will be placed. I chose this area because it represents where the force will be applied to the bracket during use.


To set up the simulation, I followed essentially the same steps from Assignment #3 when we performed an FEA on a beam. I opened the Simulation tab in SolidWorks and created a new static study.

<img width="390" height="329" alt="image" src="https://github.com/user-attachments/assets/bbd6aaeb-81e8-4f27-b0a8-a25dcb713bdd" />

> New static study

<img width="434" height="343" alt="image" src="https://github.com/user-attachments/assets/dfdb54d6-7cfe-4115-ae9d-083c44e0c67e" />

> Selected fixed geometry for the fixtures and applied them to the inside surfaces of the bracket where it would be held in place

<img width="414" height="328" alt="image" src="https://github.com/user-attachments/assets/3bb49d1a-c5d9-4c72-a472-80f6edf88369" />

> Chose external loads, force, and applied it to the cylinder.

## Inner Loop #1

For my first test, I tried three different mesh sizes, coarse, medium, and fine. I wanted to see how much the results changed when I increased the number of elements.

<img width="304" height="260" alt="image" src="https://github.com/user-attachments/assets/081f47af-dbdc-4e02-a0c6-fb92825e4a60" />
<img width="290" height="260" alt="image" src="https://github.com/user-attachments/assets/34bb96de-818c-4635-b7f3-62e337a2676e" />

> FEA Test I (course)

<img width="304" height="260" alt="image" src="https://github.com/user-attachments/assets/70df71e8-12e5-4687-ad14-5fb0ddd8a94a" />
<img width="250" height="260" alt="image" src="https://github.com/user-attachments/assets/f248c78d-c202-4b21-9620-8e0174af7b8b" />

> FEA Test II (medium)

<img width="304" height="260" alt="image" src="https://github.com/user-attachments/assets/a507122b-9e22-4dd8-be37-75740931494c" />
<img width="304" height="260" alt="image" src="https://github.com/user-attachments/assets/d565ed17-c837-41b9-92cb-72d668925a92" />

> FEA Test III (fine)

### Testing

|  | FEA TEST I (coursest) | FEA TEST II (medium) | FEA TEST III (finest) | 
| --- | --- | --- | --- |
| Max Stress (psi) | [8432.03 ](https://drive.google.com/file/d/1LmoA18RBS0y-WfzUCphlt8YkyB1MwGF-/view?usp=drive_link)  | [10351.64](https://drive.google.com/file/d/1sx3DWyFvPLpq3ygLxlOQVUxShEE6iWvI/view?usp=drive_link) | [13039.83](https://drive.google.com/file/d/1-ZmRt7BGcYg2v_fihzhOCRqZBACOtOV4/view?usp=drive_link) |
| Max deflection (in) | [0.003176](https://drive.google.com/file/d/1qqbKx0bDmgthT4KH65L3eSJQ36-L8P4y/view?usp=drive_link) | [0.003236](https://drive.google.com/file/d/1b0eXsh6fwuehORkabmpAiPix238T88Sg/view?usp=drive_link) | [0.003261](https://drive.google.com/file/d/1h88byk-4Fjp9dEaLACUSn3epMsGkUT82/view?usp=drive_link) | 
| mass (lb) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | 
| Min Safety Factor | [4.3](https://drive.google.com/file/d/1rIlzJ5jylqaa2AHQpRtdf6rnpYS43JHF/view?usp=drive_link) | [3.5](https://drive.google.com/file/d/1qDnxA7d-pIfPDjlx0o__ciH2jlDy9Gw-/view?usp=drive_link) | [2.8](https://drive.google.com/file/d/1DQxkk-69Jwnkx02tcLOZ9H1o-NJjp2bW/view?usp=drive_link) | 
| Mesh elements | [1166](https://drive.google.com/file/d/1ZSm8HjPi9pv1s8OypYy0S5V9oICioKHf/view?usp=drive_link) | [8442](https://drive.google.com/file/d/1sMF6kFER_4_QVDnT89wkHPI-IdpMtVnS/view?usp=drive_link) | [62568](https://drive.google.com/file/d/1s0uQqB2zTZbSzdjKj46UIfusShTZ44OY/view?usp=drive_link) | 

When looking at the results, I noticed that the maximum stress increased quite a bit as the mesh became finer. The coarse mesh gave me a stress of 8,432.03 psi, while the fine mesh gave me 13,039.83 psi. This showed me that the coarse mesh was not capturing the maximum stress as accurately as the finer mesh.

*add pic of calculations* 

Both differences were greater than the required 7%, meaning the stress results had not converged yet. 

Going forward, I decided that Test I was too coarse to use as my main reference because its stress result was much lower than the results from the finer meshes.  I kept Test III as my fine-mesh reference because it had the highest number of elements at 62,568.


## INNER LOOP #2

<img width="428" height="299" alt="Screenshot 2026-10-22 011229" src="https://github.com/user-attachments/assets/4da04dd1-f8bc-430f-a716-2a8870431e5e" />
<img width="352" height="298" alt="image" src="https://github.com/user-attachments/assets/e89f9cf9-1f2b-42e5-8e85-4f9a4272b5db" />

> Test IV

<img width="431" height="299" alt="image" src="https://github.com/user-attachments/assets/38af265e-77ea-4133-b48d-c0665626a647" />
<img width="338" height="271" alt="image" src="https://github.com/user-attachments/assets/73e0093a-2ebb-48e2-95fe-4352bfa9317b" />

> Test V

|  | FEA TEST IV | FEA TEST V | FEA TEST III (ref) | 
| --- | --- | --- | --- |
| Max Stress (psi) | [10691.54](https://drive.google.com/file/d/1MJ7gGu1tqx9gj4DPVeWiUv3buM2gfWa0/view?usp=drive_link) | [11475.80](https://drive.google.com/file/d/1uf39Zxmo70pj-xr1qI6cMnohy28NTYTS/view?usp=drive_link) | [13039.83](https://drive.google.com/file/d/1-ZmRt7BGcYg2v_fihzhOCRqZBACOtOV4/view?usp=drive_link) |
| Max deflection (in) | [0.003238](https://drive.google.com/file/d/1dPtVXxx03N8nPZgLZO4dmoQMzIdoZC-C/view?usp=drive_link) | [0.003249](https://drive.google.com/file/d/1i1E7-cMqJz-DT2yH8WoP8oinfBm4Wjrp/view?usp=drive_link) | [0.003261](https://drive.google.com/file/d/1h88byk-4Fjp9dEaLACUSn3epMsGkUT82/view?usp=drive_link) | 
| mass (lb) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link)  | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | 
| Min Safety Factor | [3.4](https://drive.google.com/file/d/1AsDNtX6vw21OG3OOxiBKqWM08zSHdHEe/view?usp=drive_link) | [3.2](https://drive.google.com/file/d/1pZZk6Y6gLLaCFWQMmEJis6R2lIi7sRCv/view?usp=drive_link) | [2.8](https://drive.google.com/file/d/1DQxkk-69Jwnkx02tcLOZ9H1o-NJjp2bW/view?usp=drive_link) | 
| Mesh elements | [10944](https://drive.google.com/file/d/1e23cpEhdzElK1MktT5rvVsUP70MVf5nq/view?usp=drive_link) | [19431](https://drive.google.com/file/d/1pZZk6Y6gLLaCFWQMmEJis6R2lIi7sRCv/view?usp=drive_link) | [62568](https://drive.google.com/file/d/1s0uQqB2zTZbSzdjKj46UIfusShTZ44OY/view?usp=drive_link) | 

In this round, I noticed that the displacement results were staying very close to each other. The maximum displacement only increased from 0.003238 in to 0.003249 in between Test IV and Test V.

However, the stress results were still changing. Test IV had a maximum stress of 10,691.54 psi, while Test V had a maximum stress of 11,475.80 psi.

*calc*

## INNER LOOP #3

<img width="461" height="332" alt="Screenshot 2026-10-20 192205" src="https://github.com/user-attachments/assets/ad738b66-6b28-4564-b4ae-5d66aa47670b" />
<img width="341" height="308" alt="Screenshot 2026-10-20 192231" src="https://github.com/user-attachments/assets/6dba00a4-a440-42db-a28b-9d71503678b9" />

> Test VI

<img width="481" height="344" alt="image" src="https://github.com/user-attachments/assets/d1c25216-32dc-4aff-92bf-bf4e7fed1121" />
<img width="393" height="332" alt="image" src="https://github.com/user-attachments/assets/6a5a5a2c-a7dd-4743-9e83-be0ee0e38bed" />

> Test VII


|  |FEA TEST VI | FEA TEST VII | FEA TEST III (ref) | 
| --- | --- | --- | --- |
| Max Stress (psi) | [12800.14 ](https://drive.google.com/file/d/1Mb_RpzCKlbmUZSs4rUbw9T09wy8wptMs/view?usp=drive_link)|[12468.35](https://drive.google.com/file/d/1e23cpEhdzElK1MktT5rvVsUP70MVf5nq/view?usp=drive_link) | [13039.83](https://drive.google.com/file/d/1-ZmRt7BGcYg2v_fihzhOCRqZBACOtOV4/view?usp=drive_link) |
| Max deflection (in) | [0.003256](https://drive.google.com/file/d/1But4_6RX-oerGQLNMoek-1LGg15jETto/view?usp=drive_link) | [0.003257](https://drive.google.com/file/d/1qqbKx0bDmgthT4KH65L3eSJQ36-L8P4y/view?usp=drive_link) | [0.003261](https://drive.google.com/file/d/1h88byk-4Fjp9dEaLACUSn3epMsGkUT82/view?usp=drive_link) | 
| mass (lb) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | [1.80](https://drive.google.com/file/d/1HaQvMry4wOUBWCf5TgsEzOzqOQDRxNlk/view?usp=drive_link) | 
| Min Safety Factor | [2.8](https://drive.google.com/file/d/1BniY2cQJyzA0uOpW_JSn7IzdD13bFvut/view?usp=drive_link) | [2.9](https://drive.google.com/file/d/1rIlzJ5jylqaa2AHQpRtdf6rnpYS43JHF/view?usp=drive_link) | [2.8](https://drive.google.com/file/d/1DQxkk-69Jwnkx02tcLOZ9H1o-NJjp2bW/view?usp=drive_link) | 
| Mesh elements | [36654](https://drive.google.com/file/d/1BniY2cQJyzA0uOpW_JSn7IzdD13bFvut/view?usp=drive_link) | [49319](https://drive.google.com/file/d/1ZSm8HjPi9pv1s8OypYy0S5V9oICioKHf/view?usp=drive_link) | [62568](https://drive.google.com/file/d/1s0uQqB2zTZbSzdjKj46UIfusShTZ44OY/view?usp=drive_link) | 

*calc*

Both differences were within the required 7% limit. This showed that the stress results were now much closer together and that the mesh was giving more consistent results.

After completing the third round of testing, I was more confident in the results because the stress and displacement differences were now within the required 7% limit for the comparisons I made.

I decided to keep Test III as my final reference because it had the highest number of elements, at 62,568. Its maximum stress was 13,039.83 psi, its maximum displacement was 0.003261 in, and its minimum factor of safety was 2.8.


Design Optimization
Review results to make geometric changes, adding and removing material where needed in an attempt to modify the component to be stronger, stiffer, and more lightweight than the prior solutions.
Repeat #1 through #x  a minimum of three times.
End Outer Loop

Reflections
(10%) Detail engineering lessons learned from the assignment and be specific. Eliminate words like good and bad from this section. Be more articulate. Document time spent.
For example, I learned how different size and shape meshes affect the results and the time to solve. The greater the number of meshes increases the computational time to solve.
