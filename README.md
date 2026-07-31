# Analyses of bent spindles reveal the mechanics of anaphase B in fission yeast

This repository contains the analysis code used in the publication. 
## Paper
  [Paper published on Molecular Biology of the Cell](https://doi.org/10.1091/mbc.E25-11-0556)
  [Preprint on Biorxiv](https://doi.org/10.1101/2025.11.20.689516)
   
All scripts can be run directly in **Google Colab**, so there is **no need to install Python locally**.

**Authors:**  
Paula Real-Calderón (1,2), Thomas Fai (3), Rafael R. Daga (2), Joël Lemière* (1), Fred Chang* (1)

(1).	Department of Cell and Tissue Biology, University of California San Francisco, San Francisco, CA 94117, United States<br>
(2).	Department of Nuclear Architecture and Dynamics, Andalusian Center for Development Biology (CABD), Seville, Spain, 41013<br>
(3).	Department of Mathematics and Volen Center for Complex Systems, Brandeis University, Waltham, MA 02453, United States<br>
*co-corresponding authors


## Description of the different files and folders
-> Data/Spindle Example Data/
This folder contains two examples of raw data (in the subfolders sp3 and sp4).
The codes provided in this repository uses these datasets, and can be run in Google Colab to demonstrate how the analysis is performed.
The codes were originally written to run in a Jupyter Notebook.

-> Ase1_Intensity.ipynb
This code accesses a GitHub folders containing raw data: spindle positions (x, y) and Ase1 intensity along two spindles.
The spindles are aligned parallel to the X-axis, and the Ase1 intensity is interpolated along that axis. The code generates a figure and records the following values:
X1 and X2: the X-axis positions where Ase1 is localized
Ase1 length
Spindle length (as the X-axis projection)

-> BeamTheory_Spindle.ipynb
This code fits a real spindle with a polynomial function (z). The resulting polynomial is then used to measure the spindle length (L). In the second part, the code plots the coordinates of a bent theoretical spindle modeled as a homogeneous beam of the same length (L), with the same attachement points as the real splindle one of which is (0,0) and the second (X_L,0), X_L being the projected length of the real spindle on the X axis. Finally, it plots the results and calculates the deviation coefficient between the real (green) and theoretical (blue dashed line) spindle.

-> Local_curvarture_spindle.ipynb
This code accesses a Google Drive or GitHub folder containing raw data (position x,y) from two spindles. It analyzes the curvature along each spindle and plots the results.
