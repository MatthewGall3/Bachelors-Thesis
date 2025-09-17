# Phase-Field Models with Multiple Resolution Grids: Stability and Convergence 

This is my undergraduate thesis project for Applied and Computational Mathematics at University College Dublin. The goal was to study phase-field models for simulating melting and solidification, focusing on stability, convergence, and computational efficiency. We started with a 1D Stefan problem (melting from a heated boundary), then applied asymptotic analysis and finally developed a multi-resolution grid method to reduce computational cost while preserving accuracy.

***
1-Move each point of the river out in the orthonormal direction of the point by an amount proportional to a constant times the square root of the width of the river at that point and the curvature at that point.
***




1 – Analytical vs Numerical Temperature Profiles

We compared the analytical Stefan solution with numerical simulations of the phase-field model.

The numerical solution (dashed) matches the analytical solution (solid) closely.

The small discrepancy at the interface is due to the phase-field’s “smoothing” effect.

2 – Asymptotic Expansion of Initial Conditions

A sharp initial condition introduced a persistent error jump in the first timestep.

By applying asymptotic analysis, we corrected this and constructed a smoother initial condition.

This improved spatial convergence and reduced long-term errors in the simulations.

3 – Multiple Resolution vs Single Grid

Finally, we implemented a multiple resolution method:

Phase-field variable (ϕ) solved on a fine grid

Temperature (T) solved on a coarse grid

This approach achieved similar or better accuracy while reducing runtime by up to 2× at high resolutions.

4 – Extension to 2D

The method was extended to 2D problems to include curvature effects (Gibbs–Thomson relation). This validated the robustness of the approach in more realistic geometries.

5 – Key Outcomes

Crank–Nicolson scheme improved stability.

Asymptotic expansion fixed initial-condition errors.

Multiple resolution grids provided major computational savings.

Extended successfully to 2D with curvature effects.
