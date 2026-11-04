# A9 – Pulleys

## Objective

Design a pulley system to transfer power between two parallel axes separated by a center distance of 4–6 inches. The system must meet the following requirements:

+ Pulley Diameter: Both pulleys shall have a diameter of 3 inches.
  
+ Rotational Speed: Select an operating speed between 1000–2000 rpm.
  
+ Belt Tension (Static): Select a belt tension between 4–6 lbf under stationary conditions.
  
+ Material: Pulleys may be made from aluminum, ABS, or steel, and may include a groove and shaft diameter of your choosing (within reasonable manufacturing limits).
  
+ Safety Factor: The design must satisfy a minimum safety factor of 3.
  
+ Assume the belt is made from polyurethane rubber, with a yield strength of 3.25 MPa (471 psi) at 20% strain, based on: Wanga, Chena, Wua, Zhangb, Suna, “Strain-induced Structural and Dynamic Changes in Segmented Polyurethane Elastomers.”


<img width="397" height="149" alt="image" src="https://github.com/user-attachments/assets/289500b0-98b8-4d3e-b78e-60f6041cb5f1" />


Figure #1 shows the force and geometric constraints of the design problem.

## Pullet System Design

For this portion of the assignment, we were tasked with selecting a suitable belt from Resource #1. This involved calculating the forces on both the tight and loose sides of the belt while assuming there was no slippage. We also had to calculate the minimum belt diameter using the normal stress equation and the material's yield strength. Finally, we needed to calculate the belt's outer circumference and use that information to select a suitable belt.

To begin, I listed all the knowns and unknowns required to complete these calculations. This helped organize the information and identify which values needed to be determined before selecting the final belt. Since we were allowed to choose between aluminum, ABS, or steel for the pulley material, I did some additional research to determine which material would work best with a polyurethane rubber belt. Based on my research, I decided that steel would be the most appropriate choice because it provides high strength and durability, especially when dealing with heavier loads. 

I also needed to determine the coefficient of friction between the belt and the pulley. After doing some research, I found that the coefficient of friction for polyurethane against steel is approximately μ = 0.5–0.7, according to this [source](https://www.puteken.com/polyurethane-timing-belt-steel-pulley-friction/). I decided to use a coefficient of friction of 0.5 for my calculations. I chose the lower end of the range to use a more conservative value when determining the forces acting on the belt.

<img width="281" height="332" alt="image" src="https://github.com/user-attachments/assets/fc76b3bd-f187-4b8a-8058-4d2be4bf7f7a" />

Since my calculated minimum belt diameter was 0.2591 inches, a 1/4-inch belt would be too small because its diameter is only 0.25 inches. I then visited the McMaster-Carr website to look at the available belt sizes. Since the calculated diameter was slightly larger than the minimum 1/4-inch size, I decided to increase the belt diameter to the next suitable size. Therefore I selected a belt with a diameter of 5/16 inches (0.3125 inches). This provides a diameter greater than the calculated minimum, allowing the belt to meet the required design conditions.

## Shaft Design 

Next, we move on to designing the shafts that support the two pulleys. The objective of this section is to determine the minimum shaft diameter using 1060 hardened steel while maintaining a minimum safety factor of 3.

Since we were required to use 1060 hardened steel, I did some additional research to understand how hardened steel differs from regular steel. After further [investigation](https://gcnov.com/sae-aisi-1060-carbon-steel-material-guide/), I learned that hardening involves heating and cooling the steel through a controlled process to increase its strength and hardness. The final strength depends on the heat treatment used, but hardened 1060 steel can have a much higher tensile yield strength than its untreated form.

Based on the information I found, the tensile yield strength can range from approximately 650 to 900 MPa (94,200 to 130,500 psi), depending on the heat treatment. The terms quenched and tempered are also commonly used when describing heat-treated steel. For my calculations, I decided to use the lower end of this range and assign the material a tensile yield strength of 95,000 psi. I chose this value to avoid assuming the material would perform at the highest possible strength.

<img width="281" height="331" alt="image" src="https://github.com/user-attachments/assets/ed6063cb-c2d1-4fac-b856-474eeec29878" />

Since we are dealing with torsional loading, I needed to convert the tensile yield strength into shear yield strength. To do this, I used the [Von Mises yield criterion](https://www.xometry.com/resources/3d-printing/yield-strength/), which is commonly used for ductile materials such as steel and aluminum. This criterion allows the tensile yield strength to be converted into an equivalent shear yield strength, which can then be used to determine the minimum shaft diameter.



## Journal Bearing

<img width="281" height="332" alt="image" src="https://github.com/user-attachments/assets/a83b6453-b007-43d6-9e95-853822545a8b" />

Based on my calculations, I decided to use a 3/16-inch shaft diameter and a 1/4-inch bearing length for my preliminary journal bearing design. The selected 3/16-inch (0.1875-inch) shaft is larger than my calculated minimum shaft diameter of 0.1398 inches. This means the selected shaft exceeds the minimum diameter required by the torsional calculations.

<img width="413" height="260" alt="image" src="https://github.com/user-attachments/assets/1b253dde-1f99-4072-b960-8b42e43326d8" />

I decided to use an 841 bronze bearing because it falls under the category of porous bronze, which was the material I had previously selected for my journal bearing design. To find a suitable product, I visited the McMaster-Carr website and filtered the available options based on the material and dimensions I needed.

I selected McMaster-Carr part number 9368T41, which is an 841 bearing bronze sleeve bearing. According to the product specifications, it is designed for a 3/16-inch shaft, has a 5/16-inch housing bore, and has a bearing length of 1/4 inch. These dimensions match my selected shaft diameter and preliminary bearing length. This makes the bearing a suitable option for the initial design because it fits the shaft and provides the required bearing length.

<img width="414" height="172" alt="image" src="https://github.com/user-attachments/assets/3dae8569-99cb-4484-ab4c-ce8a1a096545" />

<img width="405" height="277" alt="image" src="https://github.com/user-attachments/assets/118ac43e-0c7b-49bf-a11f-f1bc51f9d56a" />

## Design Frame

I planned the frame to hold the two shafts and journal bearings in position while maintaining the required 5-inch center distance between the pulleys. The frame must also be rigid enough to prevent excessive movement, vibration, or misalignment while the system is operating at 1,500 rpm.

There were several important factors I needed to consider when selecting a material for the frame. First, it must be strong enough to support the weight of the pulleys, shafts, and bearings, as well as the forces created by the belt during operation. Another important factor is the frame's ability to resist bending and twisting. This is known as stiffness, and it is important because excessive frame movement could cause the shafts to become misaligned. This could lead to uneven loading on the bearings and affect how smoothly the pulley system operates.

<img width="456" height="210" alt="image" src="https://github.com/user-attachments/assets/cbdf04eb-677f-47f5-8359-542a78ffd981" />

After consideration, I decided to use A36 structural steel for the frame. However I did considered aluminum as it is lighter, I ultimately chose A36 steel because it provides sufficient strength for the expected loading while also offering the stiffness needed to maintain proper alignment between the shafts.

The frame is designed as a 6-inch-long bracket with a thickness of 1/4 inch. It has two circular holes positioned at each end, with their centers 5 inches apart. Each hole has a diameter of 5/16 inches to accommodate the selected bearing housing.

One important factor I considered when designing the frame was its ability to resist bending. The areas I would be most concerned about are the middle section between the two holes and the material surrounding the holes themselves. The belt forces are transferred through the pulleys, shafts, and bearings into the frame. These forces can cause the bracket to bend, depending on how it is mounted and supported. The areas around the holes are also important because removing material to create the openings reduces the amount of material available to support the loads.

To help reduce excessive bending and deflection, I selected a bracket thickness of 1/4 inch. I chose this thickness to match the length of the selected journal bearings, keeping the dimensions consistent throughout the design. The thickness also provides more material to resist bending compared to using a thinner bracket.

## Lessons Learned 

One of the biggest things I learned was how belt tension and friction affect torque transfer between two pulleys. By calculating the tight-side and loose-side forces, I understood how the difference in tension is what allows torque to be transferred without the belt slipping. 

I also learned how important material selection is when designing mechanical components. When choosing the pulley material, I compared aluminum, ABS, and steel before settling on steel because of its strength and durability. I learned that material selection involves more than just strength, since factors like friction and how materials interact with other components also play an important role.

Another thing I learned was that calculated dimensions do not always match the sizes of actual products available for purchase. I had to consider commercially available sizes when selecting my belt, shaft, and bearings. For example, I chose a shaft diameter larger than my calculated minimum and increased the belt size to meet the required dimensions. This helped me understand that engineering design involves applying calculations to real-world products and limitations.

A challenge that I experienced was selecting actual components based on my calculated dimensions. Some of my calculated minimum sizes did not directly match the available products, so I had to adjust my selections to the next suitable size. For example, I increased the belt diameter and selected a shaft diameter larger than the calculated minimum. I also had to make sure the selected journal bearing matched the shaft diameter and required dimensions. I also had to revisit some of my design decisions to make sure the materials and dimensions worked together. This helped me understand that engineering calculations are only part of the design process, and that the final selections must also make sense when considering real components and operating conditions.

The total time spent completing this project was about 5 hours from the calculations and research to completing the final design.
