# Molecular Docking of Favipiravir with SARS-CoV-2 RdRp

## Overview
This project performs molecular docking to investigate the interaction between the antiviral drug **Favipiravir** and the **SARS-CoV-2 RNA-dependent RNA polymerase (RdRp)**. The objective was to evaluate the potential binding affinity of Favipiravir with the viral polymerase enzyme using computational docking methods.

The protein structure used in this analysis is **PDB ID: 6VWW**, a crystal structure of the SARS-CoV-2 RdRp enzyme responsible for viral RNA replication. :contentReference[oaicite:0]{index=0}

## Objectives
- Prepare the RdRp protein structure for docking
- Prepare the Favipiravir ligand
- Define the docking search space
- Perform docking using **AutoDock Vina**
- Analyze binding poses and affinity scores

## Tools and Software
- UCSF Chimera
- AutoDock Vina
- OpenBabel
- BioPython
- Google Colab

## Methodology

### Protein Preparation
- Downloaded RdRp structure (PDB ID: 6VWW) from the RCSB Protein Data Bank
- Removed water molecules and unnecessary chains
- Added polar hydrogens and charges
- Saved the cleaned protein structure

### Ligand Preparation
- Downloaded Favipiravir structure from PubChem
- Converted structure from SDF to PDB format
- Converted ligand and receptor to `.pdbqt` format for AutoDock Vina

### Docking Workflow
1. Install required libraries (BioPython, OpenBabel)
2. Convert protein and ligand structures to docking format
3. Calculate grid center coordinates
4. Generate `vina_config.txt`
5. Run docking simulation with AutoDock Vina

### Docking Results
AutoDock Vina generated multiple docking poses with different binding affinities.

Best binding pose:

Affinity = **−4.365 kcal/mol**

This indicates **moderate binding between Favipiravir and the RdRp enzyme**, suggesting potential inhibitory activity. :contentReference[oaicite:1]{index=1}

## Results
- 9 docking poses were generated
- The best pose showed moderate binding affinity
- Docking results suggest Favipiravir may interact with the viral polymerase active site

## Conclusion
This study demonstrates the use of molecular docking for antiviral drug screening. Computational docking predicted a moderate interaction between Favipiravir and SARS-CoV-2 RdRp, supporting its potential role in antiviral drug discovery.

## Author
Siddiqa Rani  
BS Bioinformatics
