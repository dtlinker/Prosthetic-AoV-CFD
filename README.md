# Prosthetic-AoV-CFD
This is a collection of axisymmetric computational fluid dynamics simulations of stenotic prosthetic valves

## Introduction
Patient-prosthesis mismatch (PPM) is a situation where patient has a prosthetic valve (usially aortic) which is too small for the amount of flow through the valve, causing an increased valve gradient, symptoms and ultimately poor clinical outcomes. For decades the measure to estimate and evaluate has been the calculated effective orifice area, indexed (normalized) to the patient's body surface area, to account for differences in flow through the valve due to body size. This measure predicts poor clinical outcomes with surgical prosthetic valves.

With the advent of non-surgical valves, called trans-aortic valve replacement, or TAVR, the results have been less clear, with many patients doing better clinically than expected from the standard measures.

This repository has results of a study using simplified computational fluid dymnamic simulations of surgical, balloon expandible TAVR, and self-expanding TAVR valves, each of which has a distinct geometry. All of the simulations were perfomred using CFDTool (Version 1.10, Precise Simulation Ltd.) which is an application within MATLAB (Version R2024b, Mathworks, Inc). It performs a finite element analysis, computational fluid simulation. For simplicity, an axisymmetric model was used. Details are in the article

Here is a Graphical Abstract of the main result:


 ![Graphical Abstract](/images/Graphicalabstract.jpg)