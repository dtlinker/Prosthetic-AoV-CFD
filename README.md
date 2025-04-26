# Prosthetic-AoV-CFD
This is a collection of axisymmetric computational fluid dynamics simulations of stenotic prosthetic valves

## Introduction
Patient-prosthesis mismatch (PPM) is a situation where patient has a prosthetic valve (usially aortic) which is too small for the amount of flow through the valve, causing an increased valve gradient, symptoms and ultimately poor clinical outcomes. For decades the measure to estimate and evaluate has been the calculated effective orifice area, indexed (normalized) to the patient's body surface area, to account for differences in flow through the valve due to body size. This measure predicts poor clinical outcomes with surgical prosthetic valves.

With the advent of non-surgical valves, called trans-aortic valve replacement, or TAVR, the results have been less clear, with many patients doing better clinically than expected from the standard measures.

This repository has results of a study using simplified computational fluid dynamic simulations of surgical, balloon expandible TAVR, and self-expanding TAVR valves, each of which has a distinct geometry. All of the simulations were performed using CFDTool (Version 1.10, Precise Simulation Ltd.) which is an application within MATLAB (Version R2024b, Mathworks, Inc). It performs a finite element analysis, computational fluid simulation. For simplicity, an axisymmetric model was used. Details are in the article

Here is a Graphical Abstract of the main result:


 ![Graphical Abstract](/images/Graphicalabstract.jpg)

 ## Geometries for simulation
 There were three geometries that were tested, to simulate a surgical bioprosthetic valve (SBV), a balloon expandable valve (BEV) and a self-expanding valve (SEV). The image below shows the baseline shape of each of these geometries.

 ![Baseline geometries](/images/Geometries.jpg)

 Variations of these baseline geometries were created taking each baseline and decreasing the AoV by 1 mm four times from 9 mm down to 5 mm, resulting in a total of 15 geometries. Additional variations then were created from these 15 variations of each geometry by reducing all of the dimensions simultaneously by 0.5 mm four times, resulting in a total of 75 geometries. Note that when all of the dimensions were reduced by 0.5 mm, this included the AoV. An overview of all the dimensions tested is shown in the table below.

 |LVOT  |AoV  |SoV	|AscAo|
 |:----:|:---:|:---:|:---:|
 |11	|9	|15	|14.5|
 |11	||8	|15	|14.5|
 |11	|7	|15	|14.5|
 |11	|6	|15	|14.5|
 |11	|5	|15	|14.5|
 |10.5	|8.5	|14.5	|14|
 |10.5	|7.5	|14.5	|14|
 |10.5	|6.5	|14.5	|14|
 |10.5	|5.5	|14.5	|14|
 |10.5	|4.5	|14.5	|14|
 |10	|8	|14	|13.5|
 |10	|7	|14	|13.5|
 |10	|6	|14	|13.5|
 |10	|5	|14	|13.5|
 |10	|4	|14	|13.5|
 |9.5	|7.5	|13.5	|13|
 |9.5	|6.5	|13.5	|13|
 |9.5	|5.5	|13.5	|13|
 |9.5	|4.5	|13.5	|13|
 |9.5	|3.5	|13.5	|13|
 |9	|7	|13	|12.5|
 |9	|6	|13	|12.5|
 |9	|5	|13	|12.5|
 |9	|4	|13	|12.5|
 |9	|3	|13	|12.5|
 
## File Organization
The folders each contain the simulations for a given iteration of LVOT radius. The file name has that value. Within the folder, each simulation is named for the type of valve and the AoV radius.

## Summary data
There is an Excel fille "Summary data final.xlsx" which contains extracted data from the simulationss. Pressure and velocity values were abstracted from the midline values of the simulation.

The columns are 
* **Type** - The type of valve, SBV, BEV or SEV
* **LVOT** - The LVOT radius	
* **SoV**	- Sinus of Valsalva radius
* **AscAo** - Ascending aorta radius
* **AoV**	- Aortic valve minimum radius
* **AoV area** - Aortic valve area calculated based on the radius	
* **Vmax** - The maximum velocity from the midline of the simulation
* **Vend** - The velocity at the distal end of the aorta in the simulation	
* **PdiffMax** - The difference between the maximum and minimum pressure in the simulation
* **PdiffEnd** - The difference between the inlet pressure and outlet pressure
* **LVOT Area** - THe calculated LVOT area	
* **OA** - Same as AoV
* **EOA**	- Efiective orifice area calculated by peak velocity
* **DVI**	- Dimensionless valve index
* **EstMaxP** - Estimated maximum pressure based on the simplified Bernoulli equation

## Publication
This analysis is being submitted for publication. When it has been accepted, the reference will be placed here.