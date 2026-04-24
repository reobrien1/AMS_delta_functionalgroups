# AMS delta functional groups: Quantifying functional group distributions from AMS data sets
This program provides the fraction of alkyl, aromatic, ketone, alcohol, and carboxylic acid groups present in an AMS mass spectrum. If you use this tool or this method for you research, please cite: O'Brien et al., "Application of a Chemical Index to Aerosol Mass Spectrometry: Delta Plots and Functional Group Distributions" ES&T Air 2026. Note: this will be updated once the full citation is avaiable.

## Overview
This repository provides Python-based programs for the deconvolution of High Resolution Time-of-flight Aerosol Mass Spectrometer (HR-ToF-AMS) data sets into specific chemical fractions. This method allows for the quantification of five functional groups: alkyls, aromatics, alcohols, carboxylic acids, and ketones.

# Key Features
-- Radial Delta Plots: These help visualize the distribution of Carbon, Hydrogen, and Oxygen containing fragments. 
-- Functional Group Quantification: An algorithm tested against standards and FTIR data to provide chemical characteristics of the mixtures

# Getting Started
Two code blocks are included here for delta analysis of AMS data. The first generates radial delta plots for carbon, hydrogen, and oxygen containing fragments (Delta_plot_). The second calculates the functional group distribution for an AMS mass spectrum (Delta_functional_groups_). 

To use these code blocks, data sets must be .CSV files with columns that are labeled mass, formula, and frac_abundance. The data should be normalized to a sum of one for all the ion intensities.

# Support and Feedback
We appreciate feedback! If you encounter performance issues or have suggestions for refinement, please let us know. For questions please reach out to Rachel O'Brien (reobrien@umich.edu). If you have issues, feel free to open an Issue in this GitHub repostiory to report bugs. We are unable to provide extensive individual troubleshooting for all data sets, but we will do our best to answer questions about the algorithm's logic and setup.

----
*Developed at the University of Michigan*
