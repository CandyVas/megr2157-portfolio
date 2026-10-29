# A8 – Gears

## Objective
Design a gearbox which can be assembled and disassembled. The spur gears have a gear ratio of 24:9 and are listed in the resource section. The output gear torque and speed are to be 1.25 in-lbf and 1100 rpm relative. The input (pinion,power-transmission) and output (gear, short shaft) shaft diameters are .125 and .25 inches respectively and each have a length of 1 inch. Use the appropriate equations in the Machinery’s Handbook for empirical units. The critical features of the gearbox include the shafts, and the journal bearings.

## Design of the shafts
### parts a & b.

Using Machinery’s Handbook, I found the allowable stresses for each shaft and compared my calculated values with the allowable stresses listed in the handbook. This helped me figure out whether the selected shaft diameters were sufficient or not.

<img width="263" height="131" alt="image" src="https://github.com/user-attachments/assets/b89067c7-14b6-4ebf-8c39-f0cabea1dadf" />

As shown in the image above, input power-transmission shaft has an allowable stress of 4,000 psi while the output short shaft has an allowable stress of 8,500 psi. 

<img width="346" height="406" alt="image" src="https://github.com/user-attachments/assets/0a42f42e-2c7c-4cba-8f66-7d99fad51f23" />

After completing the calculations, the calculated maximum shear stresses i got were 1,222.3 psi for the 0.125-in input shaft and 407.4 psi for the 0.250-in output shaft. Both calculated stresses are below their allowable stresses, meaning both shaft diameters are sufficient for the allowable stress, and no increase in shaft diameter is needed.

## Design journal bearings

### a & b
When looking through the [McMaster-Carr website](https://www.mcmaster.com/products/7880k19/number-of-teeth~48/number-of-teeth~18/shaft-diameter~1-8/shaft-diameter~1-4-1/)  I found that there was no available gear with only 9 teeth, but there was a matching gear with 24 teeth. To resolve this, I selected gears with 48 and 18 teeth. The tooth-count ratio is 48:18 which simplifies to 24:9, matching the ratio in the assignment.

Next, I narrowed down the search to gears that matched the required shaft diameters of 1/8 in (0.125 in) and 1/4 in (0.250 in). I settled on gears 7880K19 and 7880K24, which are 20-degree metal spur gears. These gears meet both the gear ratio and shaft diameter requirements. I chose them over the stainless steel alternatives because the available options did not provide the same variety of shaft diameters that I needed for the design.

<img width="747" height="217" alt="image" src="https://github.com/user-attachments/assets/6ed842ff-e3b5-4f85-86b7-0981179afc44" />

<img width="346" height="406" alt="image" src="https://github.com/user-attachments/assets/9649007d-91ec-4757-8707-991094ed759f" />


### b. v- 

For the journal bearing material, I used the chart provided in the lecture, which is also found in Machinery’s Handbook. After comparing the available materials, I selected **lubricated graphite** for the journal bearings. Its load capacity and PV rating were suitable based on the values I calculated and the limits shown in the handbook chart.

<img width="535" height="273" alt="Screenshot 2026-10-28 150258" src="https://github.com/user-attachments/assets/2532da79-e607-4274-999f-30eb01578c80" />

Dry graphite was another option, but I had a hard time finding matching options on McMaster-Carr website. Since the main difference between the dry and lubricated graphite options in the chart was their allowable PV rating, I chose lubricated graphite because it offered a higher PV limit while remaining within the required design limits.

### c. Select

For this part of the gearbox design, I chose oil-impregnated 841 bronze sleeve bearings from McMaster-Carr. I chose bronze for both shafts because I wanted to keep the material consistent throughout the design.

<img width="502" height="253" alt="image" src="https://github.com/user-attachments/assets/4170299e-40eb-4b04-a3b2-354cd6a704ff" />

For the input shaft, I selected McMaster-Carr part 9368T96, which fits a 1/8 in shaft and has a length of 1/4 in. For the output shaft, I selected part 9368T11, which fits a 1/4-in shaft and also has a length of 1/4 in. Since the output shaft has a larger diameter, its bearing also requires a larger housing bore than the input bearing. I chose these bearings to match the shaft diameters and bearing lengths from before.

## Sketch 

For this section, we were tasked to sketch a two component gearbox that could be fitted together. For my design, I decided to make the housing out of two halves that could be joined and secured with bolts. The original sketch shows my initial idea for how the two housing components would fit together.

<img width="406" height="346" alt="image" src="https://github.com/user-attachments/assets/ef77a526-7718-4af7-a5de-9ca44419f874" />

However as I'm writing my report, I noticed that my finalized gearbox CAD design was not identical to the original sketch. In the final model, the shafts pass through both ends of the housing instead of passing through only one end as shown in my sketched concept. I made this change because I wanted to create two identical housing halves rather than design an asymmetrical housing with a different hole arrangement on opposite ends to keep the design straightfoward.

## CAD Model

For the CAD model, I used parametric equations to keep the dimensions consistent throughout the design. I based the dimensions on the information provided on the McMaster-Carr website and the calculations I completed earlier in the assignment. Using parameters made it easier to keep related dimensions connected.

<img width="514" height="188" alt="image" src="https://github.com/user-attachments/assets/33b420b8-ba40-4c37-b744-59c01d48e92f" />

> Parametric Equations

<img width="442" height="311" alt="Screenshot 2026-10-28 194758" src="https://github.com/user-attachments/assets/4e251924-b9ad-4a65-b5c2-b90fbafde991" />

<img width="485" height="323" alt="Screenshot 2026-10-28 201251" src="https://github.com/user-attachments/assets/ca2d672d-32e1-4f6f-b067-15e8a1c575b4" />

<img width="380" height="298" alt="image" src="https://github.com/user-attachments/assets/8f1f7517-eab6-4a13-b159-c501d53e2f88" />


Once I had the housing constructed, I decided to open the individual files for the gears and journal bearings. This allowed me to look at each component separately before putting everything together in the assembly.

<img width="150" height="125" alt="image" src="https://github.com/user-attachments/assets/aa46b244-61c1-46a1-baf8-f08cc01fa5db" />

> 7880K19

<img width="150" height="125" alt="image" src="https://github.com/user-attachments/assets/9e4d1dcb-567b-45a4-b0eb-b7a0a00a2ae9" />

> 7880K24

<img width="150" height="125" alt="image" src="https://github.com/user-attachments/assets/0c15308e-1fe1-459b-861b-a66086e180ea" />

> 9368T96

<img width="150" height="125" alt="image" src="https://github.com/user-attachments/assets/8ad34dac-4b44-4a0e-bb10-3800e040065e" />

> 9368T11

From here I created an assembly to combine the parts into one gearbox. I used the mate feature to align the components and position them relative to one another

<img width="461" height="353" alt="image" src="https://github.com/user-attachments/assets/b6ee0b92-6917-424c-a2cb-7e803a32a5b5" />

<img width="395" height="346" alt="image" src="https://github.com/user-attachments/assets/6cd1f46a-2f3e-4923-b88b-a728ff2dd62e" />

<img width="411" height="337" alt="image" src="https://github.com/user-attachments/assets/5b663521-ce77-4598-98e1-750299fb6652" />

<img width="404" height="337" alt="image" src="https://github.com/user-attachments/assets/352e34fe-0403-4ce9-8b00-883a2ab81a00" />

<img width="437" height="346" alt="image" src="https://github.com/user-attachments/assets/86a7007f-2561-4a61-8bab-47d08dbff027" />


### Lessons Learned

Throughout this assignment, I learned how important it is to plan a CAD model around the actual components since they all affect how the final gearbox fits together. Finding a part that matches the required dimensions is not always easy, especially when there are limited options available. For example, I could not find a 9-tooth gear, so I selected gears with 48 and 18 teeth instead. This allowed me to maintain the required gear ratio while using parts that were actually available.

Another lesson is the fact that my original sketch was not exactly the same as my final CAD model because I changed the shaft openings to make the two housing halves identical. I found that using matching halves made the design simpler and easier to manage. This showed me that the first design idea is not always the most practical, and changes may be needed as the project develops.

And finally, I learned how to properly use the assembly feature in SolidWorks. Before this project, I was not as comfortable with putting different parts together but by assembling the gears, shafts, journal bearings, I got more practice using the mate feature to position each component correctly.
