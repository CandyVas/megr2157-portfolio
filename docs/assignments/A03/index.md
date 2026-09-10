# A3 – [Parametric and FEA]

## Objective
We are to design a bar which has a circular cross section using the values of the criteria given for the material, maximum deflection, and load. This is meant to determine the bar’s minimum geometry, for example its length, diameter, and weight, through parametric design while under direct tension. Only then can we verify the geometry through finite element analysis.

<img width="650" height="143" alt="image" src="https://github.com/user-attachments/assets/61611d9c-ad92-49cf-9e84-eff8cf7c3304" />

[Use this link](https://drive.google.com/file/d/1855GWirkCnZJMhWWx79BQbYXRzbFPLYa/view?usp=drive_link) to download the CAD file for this assignment !
## 1. Parametric Design
The first set of instruction is to parametrically design a bar in CAD with an <ins>applied direct load</ins> between **300 lbf < F < 500 lbf** and the <ins>max axial</ins> deflection of the bar being **.009 inches.** The material it will be designed with is from <ins>Aluminum</ins> with a range of Young’s Modulus from **(8.5 - 11.5) x 10^6 psi.**


I decided to choose a direct load of 500 lbf because it is the largest load within range. Since the bar should not exceed 0.009-in deflection, if I were to choose 300 lbf, there could be a chance of it deflecting when the load reaches 500 lbf. Would be best to design it. 

We are also tasked to choose from the Young’s Modulus range, and I settled on 10 x 10^6 (10,000,000) psi for the sake of convenience, same for my radius i decided to go with .600 inches. 

with that in mind then... 
+ Maximum load: F = 500 lbf
+ Aluminum modulus: E = 10 x 10^6 psi
+ Maximum axial deflection: δ = 0.009 in
+ r = .600 inches

<img width="649" height="232" alt="image" src="https://github.com/user-attachments/assets/d3ba4269-38d1-49d3-ab66-b3004e503723" />

Using the direct tension elongation equation in the Machinery’s Handbook, I found the length of the bar 32.4 inches. I wanted to confirm this manual calculation was correct, so using the Equations Tab in solidworks, I added all the given values I provided above. This helped me confirm that my Length of the axial deflection was indeed correct. 

<img width="589" height="253" alt="image" src="https://github.com/user-attachments/assets/031c7e1f-9b28-4ebd-8c4d-d644f46548e2" />

I used the global variables inserted into Solidworks's equation tab to then build the shape of my bar. 

<img width="495" height="358" alt="image" src="https://github.com/user-attachments/assets/5ce37f43-86df-4567-bfbd-88352f5daf6c" />
<img width="830" height="288" alt="image" src="https://github.com/user-attachments/assets/5bbd031d-dc61-49d6-b127-788a9de3a77e" />

## 2. Conduct FEA

We are then tasked to work with Solidworks stimulation, also known as FEA. Since the bar is to be designed from Aluminum, i went into the materials and switched it to the aluminum alloy material available, Alumina. 

<img width="728" height="371" alt="image" src="https://github.com/user-attachments/assets/2527add2-fda0-4e2d-8f55-984b5c718a7f" />

After parametrically determining the length of the beam and assigning a material, Then i went into the "simulation" tab on the top left corner of my solidworks panel to created a new study of my design. This is meant to generate simulated values for deflection, strain, and to generate a Von Mises stress map. I kept my design on the "static' setting 

I started off by applying the fixture of one end of my beam. The green marks on my canvas indicate that its been fixed, which leads me to the last step of applying the loads. 

<img width="713" height="358" alt="image" src="https://github.com/user-attachments/assets/a7988d6c-5db7-458d-a20d-6410d9ea148b" />

I then selected the entire bar to carry the load as for the direction of the forces, I selected it to be normal to the surface. 

<img width="897" height="296" alt="image" src="https://github.com/user-attachments/assets/bbeee518-3d21-4638-834b-8b14839cdf99" />


### a. Deflection Map

<img width="878" height="309" alt="image" src="https://github.com/user-attachments/assets/4f3b6be5-ab7a-463d-9acf-101e39d58364" />
<img width="158" height="272" alt="image" src="https://github.com/user-attachments/assets/e83fe708-3e2e-41f2-bb50-b81be8920bf6" />


### b. Von Mises

I then converted it to a mesh, and began to run the simulation to generate results of my bar. 

<img width="918" height="356" alt="Screenshot 2026-09-09 194407" src="https://github.com/user-attachments/assets/2a9939c3-31f3-4bfe-91df-aa2d25892af1" />
<img width="635" height="341" alt="Screenshot 2026-09-09 195130" src="https://github.com/user-attachments/assets/f5d28454-c9e9-41c8-8450-f2fc4359b2d2" />

## 3. Design Reflection

### a.

My hand calculation was based on a maximum axial deflection of 0.009 inches, while the maximum displacement obtained from SolidWorks FEA was 1.5e-3 (or .0015 inches). Similaraly, alluminum has a set strentgh of Sy = 40 ksi, the maximum stress I recieved on my bar was WAY below, a whopping 4.309e-02. 


<img width="513" height="146" alt="image" src="https://github.com/user-attachments/assets/648996f3-7b50-4566-ae3c-4e7678f9c08f" />

There is a drastic discrepancy in my calculations, so much so that i could have done this completely wrong. One likely source that i can come up with is something in the FEA setup, such as the  material properties, load application, or units. Since the bar has a simple circular cross section and is only being loaded via normal force, I would expect the FEA result to be fairly close to the hand calculation. The large difference suggests that some of the input values are different. However for this particular design, I would trust the hand calculation more because they are also the design limits. 

### b.
Using Peterson's Chart, the stress concentration factor (Kt) for a hole in a flat bar in tension is approximately Kt= 2.16. Using my FEA's nominal stress away from the hole (4.309×10−3 ksi), the estimated peak stress at the hole that I've determine was 9.31 * 10e-2 ksi (0.0931 ksi) which is much lower than the aluminum strength of 40 ksi. With that, i calculated the Safety Factor of 429 which technically the bar would still pass the safety factor requirement even with the addition of a pin hole. 

<img width="403" height="93" alt="image" src="https://github.com/user-attachments/assets/e5ea2d0d-fda3-495d-98e0-7198eb336492" />


## 4. Lessons Learned

One of the biggest things I learned from this project was that hand calculations and FEA results should be compared for the sake of checking accuracy. Cross referencing your results can help confirm whether or not a assignment was done correctly. This also leads me to my mistakes, which contributed to having a large difference between my calculated axial deflection and my SolidWorks FEA result. My hand calculation gave an axial deflection of 0.009 in, while the FEA gave 0.0015 in. This resulted in an 83.3% difference. This showed me that I need to pay closer attention to the material properties, boundary conditions, load application, and units in the FEA setup. Another thing I learned was that Solidworks Simulation (FEA) should be used as a verification tool, not something that you should assume to be automatically correct. It's good to compare them to hand cslculation so that they seem reasonable.

Overall, I spent approximately 7 hours on this assignment. Most of the time was spent trying to understand the project and how to produce it into Solidworks.
