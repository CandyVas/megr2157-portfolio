# A7 – [FEA]
Download my bracket file [HERE :)](https://drive.google.com/file/d/1nfd78894EtzllECF0gip0nWmreISuWJr/view?usp=sharing)
## Objective

Your task is simply to create a high stiff, high strength, and lightweight component. Use Finite Element analysis to drive your decision making process throughout your design. Each step of the analysis and before you make geometric changes make sure the component’s results (stress/displacement/Safety Factor) converge on a 7% difference. Achieve this by modifying the number of elements. If after three attempts to converge use the stiffness and stress from the finer mesh size use the finest mesh size and proceed through the process.

Since we are modifying our previously designed bracket from Assignments #5 and #6, we are supposed to keep the same material that we originally chose. We were given three options: aluminum, steel, or titanium. I initially decided to use steel, so I will continue using steel for this simulation and the rest of my design changes.

### First Test 
I wanted to start with something familiar, I decided to use the same 650 lbf load that I used in my previous hand calculations and FEA work. This gave me a starting point to see how the original bracket would perform before making any changes. I applied the force to the cylindrical section of the bracket where the polyester strap will be placed. I chose this area because it represents where the force will be applied to the bracket during use.

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

When looking at the results, I noticed that the maximum stress increased quite a bit as the mesh became finer. The coarse mesh gave me a stress of 8,432.03 psi, while the fine mesh gave me 13,039.83 psi. This showed me that the coarse mesh was not getting the maximum stress as accurately as the finer mesh.

For maximum stress:

+ Test I to Test II: |(10,351.64 − 8,432.03) / 8,432.03| × 100% = 22.77%.

+ Test II to Test III: |(13,039.83 − 10,351.64) / 10,351.64| × 100% = 25.97%.

For maximum displacement:

+ Test I to Test II: |(0.003236 − 0.003176) / 0.003176| × 100% = 1.89%.
  
+ Test II to Test III: |(0.003261 − 0.003236) / 0.003236| × 100% = 0.77%.

Both differences were greater than the required 7%, meaning the stress results had not converged yet. Therefore I decided that Test I was too coarse to use as my main reference because its stress result was much lower than the results from the finer meshes. I kept Test III as my fine-mesh reference because it had the highest number of elements at 62,568.


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

Maximum stress

+ Test IV to Test V: |(11,475.80 − 10,691.54) / 10,691.54| × 100% = 7.33%.

+ Test V to Test III: |(13,039.83 − 11,475.80) / 11,475.80| × 100% = 13.62%.

Maximum displacement

+ Test IV to Test V: |(0.003249 − 0.003238) / 0.003238| × 100% = 0.34%.

+ Test V to Test III: |(0.003261 − 0.003249) / 0.003249| × 100% = 0.37%.

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

Maximum stress

+ Test VI to Test VII: |(12,468.35 − 12,800.14) / 12,800.14| × 100% = 2.59%.

+ Test VII to Test III: |(13,039.83 − 12,468.35) / 12,468.35| × 100% = 4.58%.

Maximum displacement

+ Test VI to Test VII: |(0.003257 − 0.003256) / 0.003256| × 100% = 0.031%.

+ Test VII to Test III: |(0.003261 − 0.003257) / 0.003257| × 100% = 0.123%.

Both differences were within the required 7% limit, however I decided to keep Test III as my final reference because it had the highest number of elements, at 62,568. Its maximum stress was 13,039.83 psi, its maximum displacement was 0.003261 in, and its minimum factor of safety was 2.8.

## Design Optimization

### Design 1: 

For my first design change, I added a fillet radius of .15 inches around the curved connection of the cylinder. I chose this area because the original stress plot showed a lot of stress concentration near the bend,, which could be from the sharp corner. My reasoning was that making the transition smoother could help spread the stress over a larger area instead of concentrating it in one small region.

After making this change, I ran the FEA again using the same steel material, 650 lbf load, and fixed fixtures. I then checked the maximum stress, maximum displacement, minimum factor of safety, and mass to see how the new design compared to the original bracket.

Design 1: Increased Fillet Radius

<img width="478" height="352" alt="image" src="https://github.com/user-attachments/assets/39a02f5e-9aba-4a4c-9cff-19caba32722f" />

|  | FEA TEST I (course) | FEA TEST II (medium) | FEA TEST III (fine) | 
| --- | --- | --- | --- |
| Max Stress (psi) | 11845.74 | 12012.02 | 13003.94 |
| Max deflection (in) | 0.003189 | 0.003230 | 0.003246 |
| mass (lb) | 1.80 | 1.80 | 1.80 |
| Min Safety Factor | 3.1 | 3 | 2.8 |
| Mesh elements | 1571 | 8527 | 63129 |

For maximum stress:

+ Test I to Test II: |(12,012.02 − 11,845.74) / 11,845.74| × 100% = 1.40%.

+ Test II to Test III: |(13,003.94 − 12,012.02) / 12,012.02| × 100% = 8.26%.

For maximum displacement:

+ Test I to Test II: |(0.003230 − 0.003189) / 0.003189| × 100% = 1.29%.

+ Test II to Test III: |(0.003246 − 0.003230) / 0.003230| × 100% = 0.50%.


I noticed that the maximum stress from the finest mesh decreased slightly from 13,039.83 psi to 13,003.94 psi after adding the fillet which shows that the fillet had a slight effect on the maximum stress. 

### Design 2: 

Another thing I noticed is that the displacement plot showed a lot of red around the lower cylindrical section. This shows that this region experiences high displacement sure to the load. Since my goal is to make the bracket stiffer and lighter, I decided that my next design change will be to hollow out the cylindrical section.

<img width="385" height="281" alt="image" src="https://github.com/user-attachments/assets/19eb78bb-54b0-484e-9c07-509253077c40" />
<img width="288" height="280" alt="image" src="https://github.com/user-attachments/assets/574da93c-372b-498d-baf2-abc14569989c" />

|  | FEA TEST I (course) | FEA TEST II (medium) | FEA TEST III (fine) | 
| --- | --- | --- | --- |
| Max Stress (psi) | 12579.11| 12769.22 | 14450.00 |
| Max deflection (in) | 0.003768 | 0.003821 | 0.003850 |
| mass (lb) | 1.52 | 1.52 | 1.52 |
| Min Safety Factor | 2.9 | 2.8 | 2.5 |
| Mesh elements | 2752 | 7112 | 54713 |

For maximum displacement:

+ Test I to Test II: |(12,769.22 − 12,579.11) / 12,579.11| × 100% = 1.51%.

+ Test II to Test III: |(14,450.00 − 12,769.22) / 12,769.22| × 100% = 13.16%.

For maximum displacement:

+ Test I to Test II: |(0.003821 − 0.003768) / 0.003768| × 100% = 1.41%.

+ Test II to Test III: |(0.003850 − 0.003821) / 0.003821| × 100% = 0.76%.

The main improvement from this design was the reduction in mass. The original bracket had a mass of 1.80 lb, while the hollowed-out design had a mass of 1.52 lb. However, I also noticed that the maximum stress increased to 14,450 psi in the fine-mesh test, compared with 13,003.94 psi for the previous fillet design. The minimum factor of safety also decreased from 2.8 to 2.5, showing that removing material had a negative effect on the bracket's strength.

### Design 3: 

For my next design, I decided to increase the thickness of the vertical bar that supports the cylindrical section. I chose this area because it connects the cylinder to the rest of the bracket and helps transfer the applied load through the structure. Since the previous design showed an increase in stress and displacement after removing material, I wanted to add material back to this supporting section rather than make the entire bracket thicker. The current extrusion is 0.66 in but i increased it to 1.00 in.

|  | FEA TEST I (course) | FEA TEST II (medium) | FEA TEST III (fine) | 
| --- | --- | --- | --- |
| Max Stress (psi) | 6427.94 | 6686.14  | 7580.85  |
| Max deflection (in) | 0.001046 | 0.001059 | 0.001067 |
| mass (lb) | 1.69 | 1.69 | 1.69 |
| Min Safety Factor | 5.6 | 5.4 | 4.8 |
| Mesh elements | 1485 | 7935 | 59696 |

For maximum stress:

+ Test I to Test II: |(6,686.14 − 6,427.94) / 6,427.94| × 100% = 4.02%.

+ Test II to Test III: |(7,580.85 − 6,686.14) / 6,686.14| × 100% = 13.38%.

For maximum displacement:

+ Test I to Test II: |(0.001059 − 0.001046) / 0.001046| × 100% = 1.24%.

+ Test II to Test III: |(0.001067 − 0.001059) / 0.001059| × 100% = 0.76%.

Based on these results, increasing the thickness of the supporting bar was the most effective change I have tested so far. The maximum stress and displacement both decreased significantly, while the minimum factor of safety increased. Even though the mass increased compared with the hollowed-out design, it remained lower than the original bracket's mass.

## Tabulate...
each outer loop iteration after convergence using the table below

|  | Design I (fillet) | Design II (hallowed cylinder)| Design III (ticker bar) |
| --- | --- | --- | --- |
| Max Stress (psi) | 13003.94 | 14450.00 | 7580.85 |
| Max deflection (in) | 0.003246 | 0.003850 | 0.001067 |
| Safety Factor | 2.8 | 2.5 | 4.8 |
| Number of elements | 63129 | 54713 | 59696 |


## Reflections

Throughout this assignment, I learned how important mesh refinement is when using Finite Element Analysis to make design decisions. At first, I thought using a fine mesh would automatically give me the correct results, but after comparing the different tests, I noticed that the maximum stress could change quite a bit as the number of elements increased. The displacement results were generally more consistent, while stress and factor of safety were more sensitive to the mesh size. This showed me why I needed to check convergence before using the results to make changes to the bracket.

Another lesson I learned was that changing the design can affect stress, displacement, and weight differently. When I added the 0.15 in fillet, the maximum stress decreased slightly compared with the original bracket, but the improvement was small. This showed me that smoothing a corner can help with a stress concentration, but the size and location of the change matter. Similarly, when I hollowed out the cylinder section, i reduced the mass from 1.80 lb to 1.52 lb. However, the maximum stress and displacement increased, and the minimum factor of safety decreased. This taught me that removing material can reduce weight but can also make a component less stiff and increase the stress in the remaining material. 

I also learned that i cannot judge a design based on only one result. For example, the hollowed-out design was the lightest, but it also had the highest maximum stress and displacement of the three modified designs. The thicker supporting bar had a higher mass than the hollowed-out version, but it performed better in terms of stress, displacement, and factor of safety. 

## Time Spent
I spent 6 hours completing this assignment. This included setting up the simulations, testing different mesh sizes, checking the convergence calculations, and writing my report.
