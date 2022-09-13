# Post-Wildfire-Stability-of-Unsaturated-Hillslopes-against-Rainfall-Triggered-Landslides
A physics-based coupled hydromechanical framework to model the post-wildfire rainfall-triggered shallow landslides in hillslopes. 
The drafted package includes set of primary (input) and processed (output) data as well as the numerical and analytical codes that are in included in the scienticif paper entitled "Post-Wildfire Stability of Unsaturated Hillslopes against Rainfall-Triggered Landslides" written by Masood Abdollahi, Farshid Vahedifard, and Fred Tracy. The presented framework is a solution for modeling the post-wildfire rainfall-triggered shallow landslides in hillslopes using a physics-based method. 

Numerical solution for transient head boundary condition at the soil surface included is written in Fortran by Fred Tracy. 

The main analytical solution to model post-wildfire hillslopes' stability (MainFunction.m) is written in MATLAB 2020a by Masood Abdollahi. 

The analytical solution includes the coupled hydromechanical models to capture the water flow in soil based on different set of boundary conditions as follow:
1) "headboundary_2Part_steady": Head pressure is applied at the top boundary and the analysis is performed under staedy state conditions.
2) "Flowhead_tran_unif_2_NF": Head pressure is applied at the top boundary and the analysis is performed under transient conditions.
3) "Flow_Discharge_tran_unif_2": Discharge rate is applied at the top boundary and the analysis is performed under steady state conditions.
4) "case_1_hM_try_F": Discharge rate is applied at the top boundary and the analysis is performed transient conditions.

Two options are considered to cconsider the contribution of root reinforcement to soil strength in the analytical solution: "Consider" and "Manually".
The first uses the AFBM (MAX_Root_Rein.m) and the roots distribution characteristics to model the root reinforcement. "Manually" option asks the user for one value: apparent cohesion.

The model take the hillsope characteristics (i.e., soil hydraulic properties, soil mechanical properties, roots characteristics, Depth of water table), Transpiration rate and rainfall data.
The end result of the model is calculation of the factor of safety (SF) along the hillslope depth.

*The code is custamized to represent the characteristics of the "LAS LAMOS Basin" at the base of the San Gabriel Mountain, CA USA and model the post-fire landslides in this region in January 2019.
**For more info regarding the model derivation and case study refer to "Post-Wildfire Stability of Unsaturated Hillslopes against Rainfall-Triggered Landslides".
** To replicate the results in the paper (case study) make sure to modify the directories, select "Manually" option for root reinforcement and "discharge/transient" for water flow choice.
