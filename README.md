<p align="left">
  <img src="promo.png" width="400" alt="DFG Logo">
</p>
<br>

# DFG: Delta Functional Group analysis
**Quantifying functional group distributions from AMS data sets**
<br>

## Contents
- [Overview](#overview)
- [Citation](#citation)
- [Key Features](#key-features)
- [Limitations](#limitations)
- [Getting Started](#getting-started)
- [Dependencies](#dependencies)
- [Support and Feedback](#support-and-feedback)
- [License](#license)
<br>
<br>

## Overview
**AMS Delta Functional Group analysis (DFG)** is a Python-based workflow designed to deconvolve High-Resolution Aerosol Mass Spectrometer (HR-AMS) data sets into specific chemical functional groups. This method allows for the quantification of the relative fractions of five functional groups: alkyls, aromatics, alcohols, carboxylic acids, and ketones. AMS DFG is validated against FTIR measurements and chemical standards, and is corrected using the improved-ambient O:C framework (Canagaratna et al., 2015). This approach enables functional group quantification from existing HR-ToF-AMS datasets without requiring additional instrumentation.
<br>
<br>

## Citation
If you use this tool or this method for your research, 
please cite:

O'Brien et al., "Application of a Chemical Index to Aerosol Mass 
Spectrometry: Delta Plots and Functional Group Distributions" 
ES&T Air 2026.
<br>

*Note: this will be updated once the full citation is available.*
<br>
<br>

## Key Features

**Radial Delta Plots:** Visualize the distribution of carbon, hydrogen, and oxygen containing fragments.
<br>
<br>
<p align="left">
  <img src="Example_deltaplot.png" width="400" alt="Example radial delta plot">
</p>
<br>

**Functional Group Quantification:** An algorithm validated against chemical standards and FTIR measurements, corrected using the improved-ambient O:C ratio framework. Provides relative fractions of five functional groups: alkyls, aromatics, alcohols, carboxylic acids, and ketones.
<br>
<br>

<p align="left">
  <img src="Example_FG.png" width="400" alt="Example functional group distribution output">
</p>
<br>

## Limitations
- Requires HR-ToF-AMS data with ion formula assignments. 
- Not compatible with ACSM data (insufficient mass resolution). This is an area of ongoing work, check back here for updates.
- Currently recommended for ambient and chamber organic aerosol data sets. Performance may vary for unique aerosol types that are not chemically similar to these types.
- Aromatic fractions are lower bounds.
- Other limitations are provided in the citation above.
<br>
<br>
  
## Getting Started
### Data Requirements
Two code blocks are included here for delta analysis of AMS data. The first generates radial delta plots for carbon, hydrogen, and oxygen containing fragments (Delta_plot_v1_0_1.ipynb). The second calculates the functional group distribution for an AMS mass spectrum (Delta_functional_groups_v1_0_2.ipynb). 
<br>

To use these code blocks, data sets must be '.csv' files with the following columns:
1. 'mass': the m/z value.
2. 'formula': the assigned ion formula
3. 'frac_abundance': the fractional abundance of the ion, **normalized to a sum of 1** for all the ion intensities
<br>
<img width="293" height="228" alt="example .csv file structure" src="https://github.com/user-attachments/assets/3a4d5c47-6d59-487d-bd65-968e95a44a1b" />
<br>

**Tip** If your data is not normalized, divide each value in the frac_abundance column by the total abundance. This column becomes the new frac_abundance column.
<br>
A sample dataset is provided in the `data/example_data/` folder 
to help you verify the code is running correctly before applying 
the workflow to your own data.
<br>
<br>

### How to Run
1. **Open Google Colab:** Go to [colab.research.google.com](https://colab.research.google.com).
2. **Import from GitHub:** On the opening "Select File" screen, click the **GitHub** tab. 
3. **Link the Repo:** Paste this repository link: `https://github.com/reobrien1/AMS_delta_functionalgroups` and select the notebook you wish to run.
4. **Connect your Data:** We recommend storing your `.csv` data files in a folder on your **Google Drive**. 
    * Ensure you run the "Mount Google Drive" step in the notebook to allow Colab to access your files.
    * Update the file path in the **"Import your data"** code block to match your specific folder location.
5. **Execute:** Once the path is set, go to the **Runtime** menu at the top and select **"Run all"**. Your generated figures and functional group distributions will be displayed at the bottom of the page.
<br>
> **Tip:** If the code fails to run, double-check the file name and that your CSV column headers exactly match the requirements (`mass`, `formula`, `frac_abundance`) and that your data is normalized to a sum of 1.
<br>

### Stay Updated
We are continuously refining this tool as new standards and methods are integrated. Please check back regularly for updates to the deconvolution algorithm and expanded example datasets.
<br>

**To stay informed of the latest versions:**
* **Watch:** Click the **"Watch"** button at the top of this repository to receive notifications when we release code updates or new features.
* **Star:** **"Star"** this project to save it to your GitHub profile for easy access and to support the visibility of this tool in the atmospheric science community.
<br>

## Dependencies
This workflow requires the following Python packages
(automatically available in Google Colab):
- `numpy`
- `pandas`
- `matplotlib`
<br>

## Support and Feedback
We appreciate feedback! If you encounter performance issues or have suggestions for refinement, please let us know. For questions please reach out to Rachel O'Brien (reobrien@umich.edu). If you have issues, feel free to open an Issue in this GitHub repository to report bugs. We are unable to provide extensive individual troubleshooting for all data sets, but we will do our best to answer questions about the algorithm's logic and setup.
<br>

## License
This project is licensed under the GNU General Public License v3.0.
See the [LICENSE](LICENSE) file for details.
<br>
----
*Developed at the University of Michigan Department of Civil and Environmental Engineering*
