# A8 – Gears

## Objective
Design a gearbox which can be assembled and disassembled. The spur gears have a gear ratio of 24:9 and are listed in the resource section. The output gear torque and speed are to be 1.25 in-lbf and 1100 rpm relative. The input (pinion,power-transmission) and output (gear, short shaft) shaft diameters are .125 and .25 inches respectively and each have a length of 1 inch. Use the appropriate equations in the Machinery’s Handbook for empirical units. The critical features of the gearbox include the shafts, and the journal bearings.

## Design of the shafts
### parts a & b.

Using the Machinery’s Handbook, I found the allowable stressed appropriate for each part of the gear. I compared my answer to the allowable stresses selected from Machinery’s Handbook

<img width="263" height="131" alt="image" src="https://github.com/user-attachments/assets/b89067c7-14b6-4ebf-8c39-f0cabea1dadf" />

The input power-transmission shaft has an allowable stress of 4,000 psi, while the output short shaft has an allowable stress of 8,500 psi. 

<img width="346" height="406" alt="image" src="https://github.com/user-attachments/assets/0a42f42e-2c7c-4cba-8f66-7d99fad51f23" />

The calculated maximum shear stresses i got were 1,222.3 psi for the 0.125-in input shaft and 407.4 psi for the 0.250-in output shaft. Both calculated stresses are below their allowable stresses. Meaning both shaft diameters are sufficient for the allowable stress, and no increase in shaft diameter is needed.

## Design journal bearings

### a & b
When looking through the [McMaster-Carr website](https://www.mcmaster.com/products/7880k19/number-of-teeth~48/number-of-teeth~18/shaft-diameter~1-8/shaft-diameter~1-4-1/)  I found that there was no available gear with only 9 teeth, but there was a matching gear with 24 teeth. To resolve this, I selected gears with 48 and 18 teeth. The tooth-count ratio is 48:18 which simplifies to 24:9, matching the ratio in the assignment.

Next, I narrowed down the search to gears that matched the required shaft diameters of 1/8 in (0.125 in) and 1/4 in (0.250 in). I settled on gears 7880K19 and 7880K24, which are 20-degree metal spur gears. These gears meet both the gear-ratio and shaft-diameter requirements. I chose them over the stainless steel alternatives because the available options did not provide the same variety of shaft diameters.

<img width="747" height="217" alt="image" src="https://github.com/user-attachments/assets/6ed842ff-e3b5-4f85-86b7-0981179afc44" />

<img width="346" height="406" alt="image" src="https://github.com/user-attachments/assets/9649007d-91ec-4757-8707-991094ed759f" />


### v. 
For the journal bearing material, I used the chart provided in the lecture, which is also found in Machinery’s Handbook. After comparing the available materials, I selected lubricated graphite for the journal bearings. Its load capacity and PV rating were suitable based on the values I calculated and the limits shown in the handbook chart. Dry graphite was another option, but I had a hard time finding matching options on the McMaster-Carr website. Since the main difference between the dry and lubricated graphite options in the chart was their allowable PV rating, I chose lubricated graphite because it offered a higher PV limit while remaining within the required design limits.

### c. Select
Journal Bearing Selection

For this part of the gearbox design, I selected oil-impregnated 841 bronze sleeve bearings from McMaster-Carr. I chose bronze for both shafts because it is a suitable candidate for a small rotating-shaft application, and I wanted to keep the material consistent throughout the design.

<img width="502" height="253" alt="image" src="https://github.com/user-attachments/assets/4170299e-40eb-4b04-a3b2-354cd6a704ff" />

For the input shaft, I selected McMaster-Carr part 9368T96, which fits a 1/8-in shaft and has a length of 1/4 in. For the output shaft, I selected part 9368T11, which fits a 1/4-in shaft and also has a length of 1/4 in. The output bearing requires a larger housing bore than the input bearing.

The selected bearings match the shaft diameters and preliminary bearing lengths. However, their catalog load ratings are listed at 120 rpm, which is below the actual operating speeds of the shafts. The speed and PV limits therefore need to be checked before the bearings can be considered fully verified for the application.


## Sketch 

For the gearbox housing, I chose a two-piece design that uses bolts and nuts to hold the housing together


## CAD Model



### Lessons Learned

Lessons Learned

Throughout this assignment, I learned how to design a gearbox by using calculations, research, and CAD modeling. One of the biggest things I learned was how to use gear ratios, torque, and rotational speed to understand how two gears work together. I also learned how to calculate the distance between the gear shafts using the pitch diameters of the gears.

Another important lesson was learning how to determine whether the shaft diameters were suitable for the amount of stress they experience. I also learned how to calculate journal bearing pressure, sliding velocity, and the PV value to help choose an appropriate bearing material. Using Machinery’s Handbook helped me understand how engineering charts and equations can be applied to a real design.

I also learned that selecting components is not just about finding parts that fit. The material, dimensions, speed limits, and load capacity all need to be considered. For example, choosing journal bearings required me to consider the shaft diameters, bearing lengths, and the space available inside the housing.

Finally, I learned how important it is to plan a CAD model around the actual components. The gear sizes, shaft center distance, bearing dimensions, and housing clearances all affect how the final gearbox fits together. Designing a two-piece housing with bolts and nuts also showed me how to make a mechanical assembly that can be taken apart for maintenance.

Overall, this assignment helped me understand how calculations, material selection, component research, and CAD modeling work together in mechanical design. I also learned that engineering involves making assumptions, checking whether they are reasonable, and revising a design when something does not work as expected.
