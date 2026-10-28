# Computational Analysis of p53 Mutations

## Overview

This project uses computational biophysics to investigate how mutations in the p53 tumor-suppressor protein may affect protein structure, dynamics, and interactions with DNA. The work combines molecular dynamics trajectory analysis, structural visualization, electrostatic characterization, and residue-distance calculations to examine differences between wild-type and mutant p53 systems.

p53 plays a critical role in tumor suppression and cellular responses to DNA damage. Understanding how amino acid substitutions influence its structural properties can provide insight into the molecular mechanisms associated with p53 mutants in cancer.

## Research Objectives

Characterize structural differences between wild-type and mutant p53.

Quantify protein and DNA structural deviations across molecular dynamics trajectories.

Compare residue-level fluctuations in p53–DNA complexes.

Examine distances associated with the R273H and T284R mutations.

Investigate the electrostatic properties of selected amino acid substitutions using APBS.

Explore potential relationships between mutation combinations, structural changes, and protein function.

## Computational Methods

1. Molecular Dynamics Trajectory Analysis

Molecular dynamics trajectories of wild-type, mutant, and drug-associated p53–DNA complexes were analyzed using MDTraj. Trajectories were loaded with their corresponding structural topology files and aligned to reference frames before structural analyses.

These comparisons were designed to characterize differences in protein and DNA structural behavior across the systems.

2. Root-Mean-Square Deviation (RMSD)

RMSD calculations were used to quantify structural deviations across trajectory frames.

The analysis included:

Protein backbone Cα atoms.

DNA backbone phosphate (P) atoms.

Comparisons among wild-type, mutant, and drug-associated trajectories.

Visualization of RMSD as a function of trajectory time.

RMSD provides a quantitative measure of structural deviation relative to a reference structure.

3. Root-Mean-Square Fluctuation (RMSF)

RMSF calculations were used to investigate atom-level fluctuations throughout the trajectories.

The analyses examined Cα atoms in the protein and phosphate atoms in the DNA backbone. RMSF values were converted from nanometers to angstroms and plotted against residue or atom indices to compare structural fluctuations across trajectories.

The script Distance_RMSD_RMSF_by_trajectory.ipynb contains calculations and visualizations for comparing wild-type, mutant, and drug-associated p53–DNA trajectories. Analyses include RMSD and RMSF calculations for protein Cα atoms and DNA backbone phosphate atoms.

4. Residue-Distance Calculations

A separate analysis examined the distance between the R273H and T284R mutation sites in a p53 structural model using MDTraj (Distance_Calcs_R273H_T284R.ipynb). The analysis contains residue-distance calculations for the R273H and T284R mutation sites using Cα, closest-heavy-atom, and sidechain-heavy-atom distances.

Three contact-distance schemes were evaluated:

Cα: Distance between selected alpha-carbon atoms.

Closest-heavy: Minimum distance between heavy atoms in the selected residues.

Sidechain-heavy: Minimum distance between sidechain heavy atoms.

5. Electrostatic Analysis

The Adaptive Poisson–Boltzmann Solver (APBS) webserver was used to characterize electrostatic properties associated with selected p53 amino acid substitutions. This analysis complemented structural investigations by examining how mutations may alter the protein's electrostatic environment. Electrostatic maps of mutations were visualized in PyMol.

6. Structural Visualization

PyMOL was used to visualize protein structures and examine structural differences between wild-type and mutant p53 variants, including selected mutation combinations and potential rescue mutations.

Software and Libraries

Python: Computational analysis and data processing.

MDTraj: Molecular dynamics trajectory processing, structural alignment, RMSD, RMSF, and contact-distance calculations.

NumPy: Numerical calculations and array operations.

Pandas: Organization of calculated results into data tables.

Matplotlib: Plot generation.

Seaborn: Visualization of structural metrics across trajectories.

PyMOL: Protein structure visualization.

APBS webserver: Electrostatic characterization.

Notebooks


