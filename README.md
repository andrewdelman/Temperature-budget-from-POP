# Temperature-budget-from-POP

Andrew Delman, March 2018

This repository consists of a suite of scripts and functions that can be run in MATLAB (or open-source equivalent).  These scripts use output from POP (the ocean component of CESM) to compute seasonal and process-based decompositions of the temperature budget.  If you have any questions or need assistance running the code, please do not hesitate to contact me at Andrew.S.Delman@jpl.nasa.gov.

The reference for these scripts/functions is as follows (please cite if using or adapting this code):

Delman, A. S., J. L. McClean, J. Sprintall, L. D. Talley, and F. O. Bryan (2018), Process-specific contributions to anomalous Java mixed layer cooling during positive IOD events, J. Geophys. Res. Oceans, in review, doi:10.1002/2017JC013749.

The included .tar archives contain the .m files necessary to reproduce figures in the analysis of the paper (or analogous figures for different regions and processes).  When extracting files, keep them in the same directory 

Figures 5-7: temp_budget_inbox_calc_seasonal_decomp.tar
Run temp_budget_inbox_calc_seasonal_decomp_script.m first.
This will produce time series analogous to those in Figures 5 and 6 (time_bounds needs to be adjusted to obtain time series for different ranges as in Figure 6).
Run temp_budget_inbox_calc_composite_year_anom.m to form composite anomaly time series (analogous to Figure 7) using specified years in the output -- only works if the other script has been run first and a .mat file saved from it.

Figures 8-9: temp_budget_maps_ML_reg_decomp_multipart.tar
Run temp_budget_maps_ML_reg_decomp_multipart_script.m.
The topo2.grd file is also needed for the land mask in the maps (which is generated using the function landfind_indices.m).  topo2.grd contains 2-minute global topography as described in Smith and Sandwell (1997, Science).  Please contact me for this file, or alternatively another land mask may be used.

Figures 10d-g: temp_corr_maps_ML_multipart.tar
Run temp_corr_maps_ML_multipart_script_seasonreg.m.
The topo2.grd file is also needed for the land mask in the maps (which is generated using the function landfind_indices.m).  topo2.grd contains 2-minute global topography as described in Smith and Sandwell (1997, Science).  Please contact me for this file, or alternatively another land mask may be used.

Figures 11b-13: temp_budget_maps_ML_reg_decomp_multipart_seasonreg.tar
Run temp_budget_maps_ML_reg_decomp_multipart_script_seasonreg.m first.
This will produce maps analogous to those in Figures 13.
The topo2.grd file is also needed for the land mask in the maps (which is generated using the function landfind_indices.m).  topo2.grd contains 2-minute global topography as described in Smith and Sandwell (1997, Science).  Please contact me for this file, or alternatively another land mask may be used.
Run temp_budget_inbox_adv_process_composite_year_anom.m to form process-specific composite anomaly time series (analogous to Figures 11b and 12) using specified years in the output -- only works if the other script has been run first and a .mat file saved from it.
