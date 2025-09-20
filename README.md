# What is this repository for?
This code is from our paper "The unlocked mechanism and instability prediction of locked-segment-type slopes containing counter-tilted weak planes of different thicknesses".
# Who do I talk to?
Baicun Yang; a. School of Resources and Civil Engineering, Northeastern University, Shenyang, Liaoning 110819, China; b. State Key Laboratory of Intelligent Deep Metal Mining and Equipment, Shenyang, Liaoning 110819, China
E-mail: yangbaicun@mail.neu.edu.cn
# Usage
Open the file with the `.prj` extension and run the following codes in sequence:  
1-`model_initialization.dat`: Import the grid file `H180.f3grid`, disable large-strain mode, assign different elastic parameters and densities to zones, apply gravity and boundary constraints, run the initial solution, and save the snapshot `first_solve.f3sav`.  
2-`material_assignment.dat`: Restore the previous calculation state, reset displacements/velocities and initialize stresses; define banded and monitoring-point groups, and assign constitutive models and material parameters to each group.  
3-`show_plastic_zones.dat`: Use functions to mark zones in shear, tension, or their combinations in real time based on zone states, allowing intuitive visualization of failure range and evolution.  
4-`monitoring_point_output.dat`: Define histories of stress, strain increments, maximum shear stress, and displacements for a large number of key coordinate points, in order to generate time-response curves for each point, which facilitates post-processing and time-series analysis.  
5-`auto_save.dat`: Loop from 1 to 400, performing model cycle 50 each time and saving as `cycle.f3sav`, for regularly generating calculation snapshots to enable mid-process checks and post-processing.
