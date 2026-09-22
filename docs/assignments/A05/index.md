# A5 – Bracket Decign

### Objective

The objective of this project is to design a structural bracket capable of supporting the required applied load using strength and stiffness analysis. Free-body diagrams, normal and bending stress equations, and deflection equations are used to determine the minimum dimensions of each feature while maintaining the required factor of safety and deflection limit.

---

# Design Inputs

For this project, I selected an applied load of:

F = 700 lbf

Since the strap applies force on both sides:

W = 2F

W = 1400 lbf

The selected material is:

Aluminum 6061-T6

Material properties used:

S_y = 40,000 psi

E = 10,000,000  psi

The required factor of safety is:

N = 4

Therefore, the allowable stress is:

sigma_allow = \frac{S_y}{N}

sigma_allow = 10,000 psi

The maximum allowable deflection for each feature is:

delta_allow= 0.005 in

---

# Feature A

Feature A is the cylindrical member that supports the polyester strap. It is modeled as a cantilever beam with a uniformly distributed load.

## Known Values

F = 700 lbf

W = 1400 lbf

L_A = 2.0 in

S_y = 40,000 psi

sigma_allow = 10,000 psi

E = 10,000,000 psi

delta_allow= 0.005 in

Unknowns

Determine the required section modulus and diameter of Feature A.

Z_A = ?

d_A = ?

Assumptions

- Feature A is treated as a cantilever beam.
- The strap load is uniformly distributed across Feature A.
- The connection between Feature A and Feature B is treated as fixed.
- Direct shear failure is neglected.
- The material remains within the linear-elastic range.
- The cross section is constant.
- Deflections are assumed to be small.

<img width="500" alt="Feature A Free Body Diagram" src="INSERT-IMAGE-HERE">


# Feature B

Feature B is modeled as an axially loaded rectangular bar.

## Known Values

P_B = 1400 lbf

L_B = 2.0 in

S_y = 40,000 psi

sigma_allow=10,000 psi

E=10,000,000 psi

delta_allow=0.005 in


## Unknowns

A_B=?

t_B=?

## Assumptions

- Feature B is treated as a straight axially loaded member.
- The load acts through the centroid of the cross section.
- Bending is neglected.
- Direct shear is neglected.
- The cross section is constant.
- Aluminum remains within the linear-elastic range.
- Deformations are small.

<img width="500" alt="Feature B Free Body Diagram" src="INSERT-IMAGE-HERE">

# Feature C

Feature C is modeled as a simply supported beam with a concentrated load at the center.

## Known Values

P_C=1400lbf

L_C=4.0 in

b_C=1.25 in

S_y=40,000 psi

sigma_allow=10,000 psi

E=10,000,000 psi

delta_allow=0.005 in

## Unknowns

h_C=?

I_C=?

Z_C=?

## Assumptions

- Feature C is treated as a simply supported beam.
- The 1400 lbf load is applied at the center.
- The cross-section is rectangular and constant.
- Bending is the primary loading mode.
- Direct shear failure is neglected.
- Shear deflection is neglected.
- The material remains linear elastic.
- Deflections are small.


<img width="500" alt="Feature C Free Body Diagram" src="INSERT-IMAGE-HERE">


# Feature D

The reaction force from Feature C becomes the applied load for Feature D.

Since:

R_1=R_2=700 lbf

the applied load for one side of Feature D is:

P_D=700 lbf

## Known Values

P_D=700 lbf

S_y=40,000 psi

sigma_allow=10,000 psi

E=10,000,000 psi

delta_allow=0.005 in

L_D=1

b_D=1.25

## Unknowns

t_D=?


## Assumptions

- Feature D is treated as an axially loaded member.
- The 700 lbf load acts through the centroid of the cross section.
- Bending is neglected.
- Direct shear failure is neglected.
- The cross section is constant.
- Aluminum 6061-T6 remains in the linear-elastic range.
- Deflections are small.


**Insert Feature D FBD here**

<img width="500" alt="Feature D Free Body Diagram" src="INSERT-IMAGE-HERE">



# Feature E

Feature E transfers the load from Feature D into the rigid T-beam.

## Known Values

P_E=700 lbf

S_y=40,000 psi

sigma_allow=10,000 psi

E=10,000,000 psi

delta_allow=0.005

L_E=1.0 in

## Unknowns

t_E=?

## Assumptions

- Feature E carries the load transferred from Feature D.
- The load is assumed to act through the center of the member.
- The cross section is constant.
- Aluminum 6061-T6 remains in the linear-elastic range.
- Direct shear failure is neglected.
- Shear deformation is neglected.
- Deflections are small.

<img width="500" alt="Feature E Free Body Diagram" src="INSERT-IMAGE-HERE">


# Overall Stress and Stiffness Comparison

| Feature | Stress Requirement | Stiffness Requirement | Governing Requirement | Final Dimension |
|---|---:|---:|---|---:|
| A | 1.13 in | 0.87 in | Stress | 1.25 in |
| B | 0.140 in² | 0.056 in² | Stress | 0.1875 in thickness |
| C | 0.820 in | 0.710 in | Stress | 0.875 in |
| D | 0.056 in | 0.0112 in | Stress | 0.0625 in |
| E | 0.056 in | 0.0112 in | Stress | 0.0625 in |

The final dimension for each feature will be selected using:


D_final=max(D_{stress}/D_{stiffness})


---

# Initial CAD Design

The calculated feature dimensions will be used to create the first CAD model of the bracket.

**Insert initial CAD model here**

<img width="600" alt="Initial CAD Design" src="INSERT-IMAGE-HERE">

---

# Initial CAD Evaluation

The initial CAD model will be evaluated to determine whether the calculated dimensions fit together correctly and whether any geometry needs to be changed for manufacturing, clearances, or fit requirements.

**Insert CAD evaluation image here**

<img width="600" alt="Initial CAD Evaluation" src="INSERT-IMAGE-HERE">

---

# Final Design Revision

After evaluating the initial CAD model, any necessary dimensional or geometric changes will be made.

**Insert revised CAD model here**

<img width="600" alt="Final Design Revision" src="INSERT-IMAGE-HERE">

---

# Decide

## Final Design

The final bracket will use the dimensions that satisfy both the stress and stiffness requirements while maintaining proper fit with the rigid T-beam.

**Insert final CAD model here**

<img width="600" alt="Final CAD Design" src="INSERT-IMAGE-HERE">

---

## Final Stress Check

Each final CAD dimension will be substituted back into the appropriate stress equation.

The requirement for every feature is:

\[
\boxed{
\sigma_{actual}
\leq
\sigma_{allow}
}
\]

where:

\[
\boxed{\sigma_{allow}=10,000\text{ psi}}
\]

**Insert final stress calculations or SolidWorks results here**

<img width="600" alt="Final Stress Check" src="INSERT-IMAGE-HERE">

---

## Final Stiffness Check

Each final CAD dimension will also be checked against the maximum allowable deflection:

\[
\boxed{
\delta_{actual}
\leq
0.005\text{ in}
}
\]

**Insert final displacement calculations or SolidWorks results here**

<img width="600" alt="Final Stiffness Check" src="INSERT-IMAGE-HERE">

---

# Communicate

## Final Design Communication

The final design was developed by tracing the 1400 lbf strap load through each structural feature and determining the minimum dimensions required by both strength and stiffness. The larger requirement for each feature was used to establish the final geometry.

**Insert final isometric CAD image here**

<img width="600" alt="Final Design" src="INSERT-IMAGE-HERE">

### CAD Download

[Download Final CAD Model](INSERT-CAD-LINK-HERE)

---

# Multiview Drawings

Two detailed multiview drawings will be included: one showing the dimensions determined from stress analysis and one showing the dimensions determined from stiffness analysis.

## Stress-Based Multiview Drawing

**Insert stress multiview drawing here**

<img width="600" alt="Stress Multiview Drawing" src="INSERT-IMAGE-HERE">

## Stiffness-Based Multiview Drawing

**Insert stiffness multiview drawing here**

<img width="600" alt="Stiffness Multiview Drawing" src="INSERT-IMAGE-HERE">

---

# Lessons Learned

## Governing Failure Mode

For the features completed so far, stress has governed the required dimensions.

Feature A:

\[
d_{stress}=1.13\text{ in}
\]

\[
d_{stiffness}=0.87\text{ in}
\]

Feature C:

\[
h_{stress}=0.820\text{ in}
\]

\[
h_{stiffness}=0.710\text{ in}
\]

This demonstrates that both strength and stiffness calculations are necessary because either requirement could potentially control the final design.

## Error Propagation

The forces found in one feature are used as the applied loads for the next feature. Because of this, an incorrect reaction force early in the analysis would affect all later calculations. For example, Feature C splits the 1400 lbf load into two 700 lbf reactions. These reactions become the loads used to design the upper features.

## Assumption Sensitivity

One major assumption in the project is that direct shear failure and shear deflection are negligible. If shear effects were included, additional deformation and stress could increase the required dimensions of some features.

## Mistakes and Design Changes

**Add mistakes or corrections made during the project here.**

Example:

> During the design process, I initially had to determine how each feature should be modeled. Reviewing the assignment appendices helped identify Feature A as a cantilever, Feature B as an axially loaded member, and Feature C as a simply supported beam.

## Project Time

Total time spent on the project:

\[
\boxed{\text{TBD}}
\]

