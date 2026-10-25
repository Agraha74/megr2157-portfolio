# A7 – FEA on Bracket

# Objective
The objective of this assignment is to use Finite Element Analysis (FEA) in SOLIDWORKS to improve the strength and stiffness of my bracket from A6 while keeping its mass as low as possible. I will use static simulations to check stress, deflection, and factor of safety, and I will compare three geometry designs. For each design, I will run three different mesh refinements before making the next geometry change.
Design requirements
The bracket attaches to a rigid T-beam and supports a strap through the lower cylindrical feature. I kept the same 6061-T6 aluminum material used in A6, as required by the assignment.
- Material: aluminum 6061-T6
- Yield strength used in the SOLIDWORKS FEA: 39,890 psi (approximately 40,000 psi in A6)
- Elastic modulus used for my earlier A6 calculations: 10,000,000 psi
- Required design factor of safety from A6: 4
- Allowable stress from my A6 calculation: 40,000 / 4 = 10,000 psi (approximately 9,972.5 psi using the simulation yield strength)
- Maximum allowable deflection from A6: 0.005 in
- Applied FEA load: 1,400 lbf, downward on the selected curved surface of the bottom cylindrical support
- Mesh convergence requirement: 7% difference between successive results; after three attempts, use the finest mesh if the results have not converged
The mounting feature also follows the previous A6 interface dimensions: a = 0.498 in, b = 0.9992 in, and c = 1.499 in. I did not change the assigned material while optimizing the geometry.

# Initial CAD model
I started with my A6 bracket CAD model and used it as the first design. The original model had an upper mounting feature, a narrow drop-down arm, and a lower cylindrical support. Its calculated mass in SOLIDWORKS was 0.58 lb.

<img width="500" height="500" alt="Screenshot 2026-10-23 175118 (1).jpg" src="Screenshot 2026-10-23 175118 (1).jpg">


# FEA setup
I used a static study in SOLIDWORKS Simulation. First, I applied fixed geometry to the two inside mounting faces near the top of the bracket. This represents the bracket being restrained at the T-beam connection.

<img width="500" height="500" alt="Screenshot 2026-10-23 175238 (1).jpg" src="Screenshot 2026-10-23 175238 (1).jpg">

I then added the 1,400 lbf downward force to the split face on the top of the lower cylinder. I kept the same support and load arrangement for the design comparisons.

<img width="500" height="500" alt="Screenshot 2026-10-23 180318 (1).jpg" src="Screenshot 2026-10-23 180318 (1).jpg">

I used a curvature-based solid mesh and adjusted the mesh controls to increase the element count for each successive run. I recorded the maximum von Mises stress, maximum resultant displacement, minimum factor of safety, and element count. I also checked mass after geometry changes.

# Workflow and mesh validation
I completed the inner validation loop by running the same geometry three times with a progressively finer mesh. I then used the outer design loop to make a geometry change based on the stress and displacement plots. I repeated this process for three designs.

To check convergence, I used:

Percent change = |new result − previous result| / previous result × 100%

For the results to meet the assigned convergence limit, the important values should change by no more than 7% from one run to the next. When stress did not converge after three runs, I documented the finest mesh result, following the assignment instructions. 

# Design 1 – Original A6 bracket
I started with the bracket from A6 without changing the geometry. The initial model had a narrow vertical section between the upper mounting feature and the lower cylindrical strap support. I expected this connection to carry most of the bending load.

<img width="500" height="500" alt="Screenshot 2026-10-23 175118 (1).jpg" src="Screenshot 2026-10-23 175118 (1).jpg">

D1-1 – Coarse mesh
For run 1, the mesh contained 9,052 elements. The maximum von Mises stress was 391,200 psi, the maximum displacement was 1.285 in, and the minimum factor of safety was 0.102.

<img width="500" height="500" alt="Screenshot 2026-10-23 181547 (1).jpg" src="Screenshot 2026-10-23 181547 (1).jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 183504 (1).jpg" src="Screenshot 2026-10-23 183504 (1).jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 183524 (1).jpg" src="Screenshot 2026-10-23 183524 (1).jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 182905 (1).jpg" src="Screenshot 2026-10-23 182905 (1).jpg">

D1-2 – Medium mesh
For run 2, the mesh contained 47,722 elements. The maximum von Mises stress was 553,700 psi, the maximum displacement was 1.329 in, and the minimum factor of safety was 0.072.

<img width="500" height="500" alt="Screenshot 2026-10-23 184027 (1).jpg" src="Screenshot 2026-10-23 184027 (1).jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 195652 (1).jpg" src="Screenshot 2026-10-23 195652 (1).jpg">

<img width="500" height="500" alt="Untitled design.jpg" src="Untitled design.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 195802 (1).jpg" src="Screenshot 2026-10-23 195802 (1).jpg">

D1-3 – Finest mesh
For run 3, the mesh contained 222,098 elements. The maximum von Mises stress was 851,300 psi, the maximum displacement was 1.333 in, and the minimum factor of safety was 0.047.

<img width="500" height="500" alt="Screenshot 2026-10-23 195917.jpg" src="Screenshot 2026-10-23 195917.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 201248.jpg" src="Screenshot 2026-10-23 201248.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 201248.jpg" src="Screenshot 2026-10-23 201248.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 195802 (1).jpg" src="Screenshot 2026-10-23 195802 (1).jpg">

D1 – Resulting data

<img width="500" height="500" alt="A7_Design_1_Results.jpgg" src="A7_Design_1_Results.jpg">

Mass: 0.58 lb.

Design 1 – Discussion about data and changes
The original bracket had the lowest mass, but it experienced severe bending and stress around the connection beneath the top mounting section. At the finest mesh, the stress reached 851,300 psi, the displacement was 1.333 in, and the factor of safety was 0.047. The displacement remained nearly unchanged between the last two meshes, but the peak stress continued to rise. I decided to add a second supporting member in Design 2 to give the applied load another path into the top bracket.

# Design 2 – Added vertical reinforcement
For the second design, I added another support alongside the original arm connecting the lower cylinder to the mounting bracket. This increased the amount of material slightly, but I wanted to see whether dividing the load between the members would reduce the amount of bending.

<img width="500" height="500" alt="Screenshot 2026-10-23 202004.jpg" src="Screenshot 2026-10-23 202004.jpg">

D2-1 – Coarse mesh
For run 1, the mesh contained 9,776 elements. The maximum von Mises stress was 537,300 psi, the maximum displacement was 0.6772 in, and the minimum factor of safety was 0.074.

<img width="500" height="500" alt="Screenshot 2026-10-23 202222.jpg" src="Screenshot 2026-10-23 202222.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 202545.jpg" src="Screenshot 2026-10-23 202545.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 202634.jpg" src="Screenshot 2026-10-23 202634.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 202700.jpg" src="Screenshot 2026-10-23 202700.jpg">


D2-2 – Medium mesh
For run 2, the mesh contained 57,512 elements. The maximum von Mises stress was 702,900 psi, the maximum displacement was 0.711 in, and the minimum factor of safety was 0.057.

<img width="500" height="500" alt="Screenshot 2026-10-23 203029.jpg" src="Screenshot 2026-10-23 203029.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 203052.jpg" src="Screenshot 2026-10-23 203052.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 203106.jpg" src="Screenshot 2026-10-23 203106.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 203122.jpg" src="Screenshot 2026-10-23 203122.jpg">


D2-3 – Finest mesh
For run 3, the mesh contained 258,400 elements. The maximum von Mises stress was 755,700 psi, the maximum displacement was 0.7192 in, and the minimum factor of safety was 0.053.

<img width="500" height="500" alt="Screenshot 2026-10-23 203029.jpg" src="Screenshot 2026-10-23 203029.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 203052.jpg" src="Screenshot 2026-10-23 203052.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 203106.jpg" src="Screenshot 2026-10-23 203106.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-23 203122.jpg" src="Screenshot 2026-10-23 203122.jpg">


D2 – Resulting data

<img width="500" height="500" alt="A7_Design_2_Results.jpg" src="A7_Design_2_Results.jpg">


Mass: 0.62 lb.

Design 2 – Discussion about data and changes
Adding the support reduced the finest-mesh displacement from 1.333 in to 0.7192 in, a reduction of about 46.1%. The maximum stress fell by about 11.2%, but it was still concentrated near the upper bracket connection. The factor of safety was only 0.053, so the change improved stiffness without fixing the strength problem. I moved on to a more substantial geometry change rather than just adding another narrow support.

# Design 3 – Wider, reinforced support
For Design 3, I changed the geometry more significantly. I added material around the upper mounting section and made the load path down to the cylinder wider and more continuous. This was intended to reduce bending and spread the applied load over a larger area. The extra material also made this the heaviest design.

<img width="500" height="500" alt="Screenshot 2026-10-24 202424.jpg" src="Screenshot 2026-10-24 202424.jpg">

D3-1 – Coarse mesh
For run 1, the mesh contained 17,408 elements. The maximum von Mises stress was 40,210 psi, the maximum displacement was 0.01442 in, and the minimum factor of safety was 0.992.

<img width="500" height="500" alt="Screenshot 2026-10-24 202623.jpg" src="Screenshot 2026-10-24 202623.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 202709.jpg" src="Screenshot 2026-10-24 202709.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 202743.jpg" src="Screenshot 2026-10-24 202743.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 202821.jpg" src="Screenshot 2026-10-24 202821.jpg">

D3-2 – Medium mesh
For run 2, the mesh contained 128,825 elements. The maximum von Mises stress was 37,080 psi, the maximum displacement was 0.01475 in, and the minimum factor of safety was 1.076.

<img width="500" height="500" alt="Screenshot 2026-10-24 203624.jpg" src="Screenshot 2026-10-24 203624.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 203748.jpg" src="Screenshot 2026-10-24 203748.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 203818.jpg" src="Screenshot 2026-10-24 203818.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 203841.jpg" src="Screenshot 2026-10-24 203841.jpg">

D3-3 – Finest mesh
For run 3, the mesh contained 857,837 elements. The maximum von Mises stress was 62,800 psi, the maximum displacement was 0.01493 in, and the minimum factor of safety was 0.64.

<img width="500" height="500" alt="Screenshot 2026-10-24 203938.jpg" src="Screenshot 2026-10-24 203938.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 204458.jpg" src="Screenshot 2026-10-24 204458.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 204524.jpg" src="Screenshot 2026-10-24 204524.jpg">

<img width="500" height="500" alt="Screenshot 2026-10-24 204618.jpg" src="Screenshot 2026-10-24 204618.jpg">

D3 – Resulting data
<img width="500" height="500" alt="A7_Design_3_Results.jpg" src="A7_Design_3_Results.jpg">


Mass: 1.21 lb.
Design 3 – Discussion about data and changes
The thicker support made the largest difference. At the finest mesh, the displacement was down to 0.01493 in, and the maximum stress was 62,800 psi. The stress was much lower than in the first two designs, but the minimum factor of safety still came out to 0.64. The medium mesh had suggested a factor of safety of about 1.1; the finer mesh revealed a higher peak stress and a lower safety factor. This was an important reminder that results 
from one mesh are not enough to justify a design.

# Final design comparison
<img width="500" height="500" alt="A7_Final_Design_Comparison.jpg" src="A7_Final_Design_Comparison.jpg">


# Convergence check
<img width="500" height="500" alt="A7_Convergence_Check.jpg" src="A7_Convergence_Check.jpg">


The deflection results were within 7% between the final two meshes for all three designs, but the peak stress never converged within 7%. Because I had already completed three mesh runs for each design, I used the finest mesh values as directed. This does not mean the reported peak stress is fully mesh-independent. The highest stress is close to corners and the mounting region, so a localized stress concentration or an overly restrictive fixed boundary might be affecting the result.
Checking the factor of safety
The factor of safety shown in the FEA results is based on the material yield strength and the maximum von Mises stress:

FOS = Yield strength / Maximum von Mises stress

For the finest mesh of Design 3:

FOS = 39,890 / 62,800 = 0.635 ≈ 0.64

The medium mesh of Design 3 gave a factor of safety of about 1.1, but the finest mesh lowered this to 0.64. This is why I cannot use 1.1 as my final result. To reach my A6 target of FOS = 4, the stress would need to be at or below about 10,000 psi. The Design 3 displacement of 0.01493 in also exceeds my A6 deflection limit of 0.005 in. Design 3 is a major improvement but still does not meet my original design requirements.
Reflections

This assignment showed me how much the results of a simulation can change as the mesh gets finer. In Design 3, the deflection was almost unchanged between the last two runs, but the maximum stress increased substantially. I learned that I have to check both stress and displacement rather than trusting one result or using a larger factor of safety from a less refined simulation.

I also learned that the shape of the load path can make a bigger difference than simply adding a little material. The second vertical support helped reduce bending, but the wider and more continuous support in Design 3 produced a much larger improvement. However, it also increased the mass from 0.58 lb to 1.21 lb, so I still need to work on the balance between stiffness, strength, and weight.

If I continued the project, I would first investigate the high-stress region near the top mounting opening and test smooth fillets or revised transitions. I would also recheck the fixed boundary conditions, refine the mesh locally, and try to remove material from areas that show low stress. These are future improvements, not simulations that I have already completed.

# Communicate
Time spent: 6-8 Hours ( Went down a rabbit hole)

CAD file: https://github.com/Agraha74/megr2157-portfolio/blob/main/docs/assignments/A07/Megr%202157%20A6.SLDPRT

Conclusion: Design 3 had the best structural performance out of the three designs I tested. It greatly reduced stress and deflection, but it added mass and still did not meet the required factor of safety or maximum deflection. The next step would be another geometry iteration and a closer investigation of the concentrated peak stresses.

