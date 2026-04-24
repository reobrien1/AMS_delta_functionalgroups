# AMS delta functional groups: Quantifying functional group distributions from AMS data sets

## Overview
**AMS-Delta-Groups** is a validated Python-based workflow designed to deconvolve High-Resolution Aerosol Mass Spectrometer (HR-AMS) data into specific chemical functional groups. This method allows for the quantification of the relative fractions of five functional groups: alkyls, aromatics, alcohols, carboxylic acids, and ketones.

## Citation
If you use this tool or this method for you research, please cite: 
**O'Brien et al., "Application of a Chemical Index to Aerosol Mass Spectrometry: Delta Plots and Functional Group Distributions" ES&T Air 2026. 
Note: this will be updated once the full citation is avaiable.

## Key Features
**Radial Delta Plots:** Visualize the distribution of carbon, hydrogen, and oxygen containing fragments. 

**Functional Group Quantification:** An algorithm tested against standards and FTIR data to provide chemical characteristics of the mixtures

## Getting Started
### Data Requirements
Two code blocks are included here for delta analysis of AMS data. The first generates radial delta plots for carbon, hydrogen, and oxygen containing fragments (Delta_plot_). The second calculates the functional group distribution for an AMS mass spectrum (Delta_functional_groups_). 

To use these code blocks, data sets must be '.csv' files with the following columns:
1. 'mass'" the m/z value.
2. 'formula': the assigned ion formula
3. 'frac_abundance'": the fractional abundance of the ion (the data should be **normalized** to a sum of 1 for all the ion intensities)

### How to Run
Open your Google Collaboraotry. On the opening page, you should have the option to click on GitHub under "Open notebook". Paste this Github link (https://github.com/reobrien1/AMS_delta_functionalgroups) into this page and it will open the Google Collaboratory pages that are available here. We recommend storing the .csv data files in a google folder under your account. You can then change the information in the third block: "Import your data" to match the location of your data sets. Once this is done, you should be able to click "Run all" at the top and your figure should be displayed at the bottom of the page.

## Support and Feedback
We appreciate feedback! If you encounter performance issues or have suggestions for refinement, please let us know. For questions please reach out to Rachel O'Brien (reobrien@umich.edu). If you have issues, feel free to open an Issue in this GitHub repostiory to report bugs. We are unable to provide extensive individual troubleshooting for all data sets, but we will do our best to answer questions about the algorithm's logic and setup.

----
*Developed at the University of Michigan*
