# Bachelors-Thesis
Phase-Field Models with Multiple Resolution Grids

This repository contains the code and results from my undergraduate thesis:
Phase-Field Models with Multiple Resolution Grids: Stability and Convergence.

The project investigates phase-field models for simulating phase-change processes such as melting and solidification. Instead of tracking a sharp interface, the phase-field method smooths it into a diffuse region, making the equations easier to simulate. My work focused on:

Stability & convergence of numerical methods

Asymptotic analysis to reduce initial errors

Multiple-resolution grids for efficiency (fine grid for the phase-field variable, coarse grid for temperature)

Key Results & Figures
1. Temperature Profile Over Time

Compares analytical (blue) vs. numerical (dashed black) solutions of the 1D Stefan problem.

Shows that the phase-field model reproduces the analytical solution well, validating the numerical scheme.

The slight mismatch at the interface highlights inherent “smoothing” from the diffuse interface.

2. Asymptotic Expansion of Initial Condition

The sharp analytical initial condition introduces a persistent error jump at the first timestep.

Asymptotic expansion smooths this initial condition by blending outer and inner solutions.

Result: A corrected profile (T_new, red dashed) that improves spatial convergence and reduces error growth.

3. Multiple Resolution vs. Single Grid

Runtime comparison between single-grid and multiple-resolution methods.

Multiple resolution (fine grid for phase-field ϕ, coarse grid for temperature T) achieves:

Comparable or better accuracy

Up to 2× faster performance at high resolutions

Demonstrates that computational efficiency can be substantially improved without sacrificing accuracy.

Contributions

Implemented Crank–Nicolson scheme for stability.

Applied asymptotic analysis to improve convergence.

Developed a multi-resolution method for phase-field models — a novel application in this context.

Extended the approach to 2D problems with curvature (capturing Gibbs–Thomson effects).
