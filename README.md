# Phase-Field Models with Multiple Resolution Grids: Stability and Convergence 

This is my undergraduate thesis project for Applied and Computational Mathematics at UCD. The goal was to study phase-field models for simulating melting and solidification, focusing on stability, convergence, and computational efficiency. 

We started with a 1D Stefan problem (melting from a heated boundary), This problem is useful as it has an anaylitical solution which we can use to verify the accuracy of our phase-field model. The phase-field equations does not have an anaylitical solution instead requiring numerical methods to solve. We used a Crank-Nicolson scheme to solve the phase-field equations for stability purposes.

***
1-Analytical vs Numerical Temperature Profiles

We compared the analytical Stefan solution with numerical simulations of the phase-field model. The numerical solution (dashed) matches the analytical solution (solid) closely. The small discrepancy at the interface is due to the phase-field’s “smoothing” effect.
<img width="800" height="600" alt="Temperature_Profile" src="https://github.com/user-attachments/assets/f4842c1e-7e59-4613-89a6-9dadebac84c3" />


***
2–Asymptotic Expansion of Initial Conditions

A sharp initial condition introduced a persistent error jump in the first timestep. By applying asymptotic analysis, we corrected this and constructed a smoother initial condition.
This improved spatial convergence and reduced long-term errors in the simulations.
<img width="800" height="600" alt="Asmytotics" src="https://github.com/user-attachments/assets/532f158b-9ea4-46c7-9eec-3d6661496ff2" />

***

3 – Multiple Resolution vs Single Grid

Finally, we implemented a multiple resolution method: Phase-field variable (ϕ) solved on a fine grid, Temperature (T) solved on a coarse grid This approach achieved similar or better accuracy while reducing runtime by up to 2× at high resolutions.


<img width="447" height="240" alt="Screenshot 2025-09-17 at 18 01 23" src="https://github.com/user-attachments/assets/2e5018b4-6b1e-4a40-a0a2-737fc47c2755" />

***
4 – Extension to 2D

The method was extended to 2D problems to include curvature effects (Gibbs–Thomson relation). This validated the robustness of the approach in more realistic geometries.

***

5 – Key Outcomes

Crank–Nicolson scheme improved stability. Asymptotic expansion fixed initial-condition errors. Multiple resolution grids provided major computational savings. Extended successfully to 2D with curvature effects.
***
