# A10 – Lead Screw Translating System

## My Part: Lead Screw Dia

## Objective
The objective of this assignment was to determine the minimum leadscrew diameter, required rotational speed, and maximum operating torque for a mechanically driven tensile testing machine. The tensile tester must apply a 
maximum axial load of 2,000 N while maintaining a controllable crosshead speed between 1 and 50 mm/min. The system uses two identical leadscrews to distribute the applied load evenly. A safety factor of 4 is required.

## Design Requirements

-Maximum tensile load: 2,000 N

-Number of leadscrews: 2

-Safety factor: 4

-Crosshead speed: 1–50 mm/min

-Minimum leadscrew length: 18 inches

-Power system: Purely mechanical

## Minimum Leadscrew Diameter

We began by determining the axial load on each leadscrew. Since the system uses two identical leadscrews, we assumed the load would be distributed equally.
Carbon steel was selected due to its strength, machinability, affordability, and availability through McMaster-Carr.


<img width="500" height="500" alt="A10 1.jpg" src="A10 1.jpg">

<img width="500" height="500" alt="A10 2.jpg" src="A10 2.jpg">

McMaster-Carr only had the ultimate tensile strength of 64,000 psi. Because the yield strength was not specified, we estimated it using an assumed yield-to-tensile strength ratio of 0.56.
The calculated minimum root diameter was approximately 4.5 mm based on axial yielding alone. Additional checks are needed to verify the screw under combined axial and torsional loading.

## Rotational Speed

<img width="500" height="500" alt="A10 3.jpg" src="A10 3.jpg">

<img width="500" height="500" alt="A10 4.jpg" src="A10 4.jpg">

The required rotational speed range is approximately 0.63–31.5 rpm. Both leadscrews must rotate at the same speed to ensure consistent crosshead movement and minimize misalignment.

## Maximum Torque

<img width="500" height="500" alt="A10 6.jpg" src="A10 6.jpg">

<img width="500" height="500" alt="A10 6.jpg" src="A10 6.jpg">

The operating thread torque is 0.69 N·m per screw, or 1.4 N·m total. The preliminary factored thread torque is 5.5 N·m.

These results use an assumed friction coefficient of 0.15 and exclude bearing friction and drivetrain losses. They do not establish the maximum allowable torsional capacity of the selected screw, which requires a separate strength check.

4. Leadscrew Selection

After evaluating the calculations, I've selected the following leadscrew 

https://www.mcmaster.com/98935A803/
