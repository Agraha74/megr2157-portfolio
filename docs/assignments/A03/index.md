# A3 – [Topic]

## Objective

For this project, I was tasked with designing an aluminum bar that has a maximum deflection of 0.009 in while subjected to a tensile load between 300 and 500 lbf. The aluminum has a Young’s modulus ranging from 8.5-11.5*10^6 psi. For my design, I selected an applied load of 400 lbf and a Young’s modulus of 10*10^6 psi.

## Analyze
Step one was to find the cross-sectional area. I tried different diameters but landed on .5in because it seemed like a reasonable size for the design. Once I decided on a diameter, I was able to solve for the length. The final design had a diameter of 0.50 in, a cross-sectional area of 0.1963 in², and a calculated length of 44.18 in. Then I plugged everything into SolidWorks. 

<img width="500" height="500" alt="Screenshot 2026-09-08 013725.jpg" src="Screenshot 2026-09-08 013725.jpg">

After creating the model, I set up a static simulation in SolidWorks. I fixed one end of the bar while applying the tensile load to the opposite end. I then generated displacement and stress plots to compare the simulation results with my hand calculations.

<img width="500" height="500" alt="Screenshot 2026-09-08 015153.jpg" src="Screenshot 2026-09-08 015153.jpg">

I checked the von Mises stress to make sure the bar remained below the yield strength of the aluminum. The maximum stress from the simulation was below the material's yield strength, giving the bar a factor of safety greater than 1. This shows that the bar should remain in the elastic region under the applied load.

<img width="500" height="500" alt="Screenshot 2026-09-08 015204.jpg" src="Screenshot 2026-09-08 015204.jpg">

The maximum displacement from the SolidWorks simulation was approximately 0.009 in. This gives a percent difference of approximately 0%. This was very close to the maximum allowable deflection used in my hand calculations, which shows that the analytical calculation and FEA results agree closely.

## Decide
The hand calculations and SolidWorks simulation produced very similar deflection results. This was expected because the geometry and loading conditions were simple and closely matched the assumptions used in the axial deformation equation. The FEA provides a more detailed view of the stress and displacement throughout the bar, while the hand calculations provide a quick way to determine the required geometry. Overall, the results show that the selected design meets the deflection and stress requirements.

<img width="500" height="500" alt="Screenshot 2026-09-08 022158.jpg" src="Screenshot 2026-09-08 022158.jpg">

For the pin-hole analysis, I pick a hole diameter of 0.125 in. With a bar width of 0.50 in, the ratio is 0.25. From a stress concentration chart for a circular hole in a bar under tension, I found that the stress concentration factor is approximately 3.2. Using the nominal FEA stress of 14.81 MPa, the estimated peak stress is approximately 47.4 MPa. This is greater than the aluminum yield strength of 27.57 MPa, so the bar would no longer meet the safety requirement once the hole is added.


[Megr 2156 FEA.SLDPRT](https://github.com/Agraha74/megr2157-portfolio/blob/main/docs/assignments/A03/Megr%202156%20FEA.SLDPRT)



## Communicate

This project helped me to learn how to use FEA in SolidWorks. It took me 2 hours.  
