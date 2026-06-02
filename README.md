# CCNL_Symptoms_Neurotransmitters

## Symptom Dimension-Specific Neurotransmitter Correlates of Psychopathology and Cognition in Early Psychosis
##### This repository contains the analysis and visualization code for identifying dimension-specific brain signatures in an early psychosis cohort and characterizing their spatial correspondence with normative neurotransmitter receptor and transporter maps.

All code was written in Python. 

#### Prerequisites
Before you begin, ensure you have met the following requirements:

- Python 3.x installed
- Jupyter Notebook or JupyterLab installed

#### Libraries Used
This project depends on several Python libraries. Ensure you have the following installed:

NumPy: For numerical computing.
Pandas: For data manipulation and analysis.
Matplotlib: For creating static, interactive, and animated visualizations in Python.
SciPy: For scientific and technical computing.
Scikit-learn: For machine learning and data mining.
NiBabel: For reading and writing neuroimaging data.
Seaborn: For making statistical graphics.

You can install all dependencies by running:
pip install numpy pandas matplotlib scipy scikit-learn nibabel seaborn

### Repository Structure
##### The codebase is divided into two primary analytical steps: deriving the brain signatures via Partial Least Squares correlation (PLSc) and performing the spatial receptor annotation using the neuromaps toolbox (github.com/netneurolab/neuromaps).

#### Brain Signature Plotting (Latent Components)
These scripts visualize the PLSc-derived neural signatures associated with specific clinical dimensions (positive symptoms, negative symptoms, general psychopathology, and cognition).

- hcpep-rsfc-LC-plotting.ipynb: Generates the visualizations for the resting-state functional connectivity (RSFC) symptom models. This includes the scatterplots of composite scores, network-level correlation heatmaps, and circos plots representing stable within- and between-network RSFC loadings (Figure 1).

- cog-rsfc-LC-plotting.ipynb: Generates the equivalent RSFC visualizations specifically for the cognition dimension, including the composite score scatterplots, network matrices, and circos plots (Figure 1).

- hcpep-anat-LC-plotting.ipynb: Generates the visualizations for the anatomical PLS models (cortical thickness and subcortical volume). This includes the composite score scatterplots and the cortical surface / subcortical volume map renderings for positive symptoms, general psychopathology, and cognition (Figure 2).

- cog-anat-LC-plotting.ipynb: Generates the equivalent anatomical visualizations specifically for the cognition dimension, including the composite score scatterplots, network matrices, and circos plots (Figure 2).

#### Neurotransmitter Receptor Annotation Plotting
These scripts map the derived brain signatures against 21 PET-derived receptor and transporter density maps across 9 neurotransmitter systems.

- cog_ep-rsfc-receptor-plotting.ipynb: Consolidates the spatial correlation analyses for the RSFC modality across all dimensions (cognition + early psychosis symptoms). This generates the final matrices displaying Spearman ρ values, spin-permutation p-values, and FDR-corrected q-values (Figure 3).

- cog_ep-anat-receptor-plotting.ipynb: Consolidates the spatial correlation analyses for the anatomical modality across all dimensions. This generates the statistical heatmaps for the anatomical signatures against the receptor maps (Figure 3).

####  Data Availability
The neuroimaging and clinical data used in these analyses are available through the Human Connectome Project for Early Psychosis (HCP-EP Release 1.1) via the NIMH Data Archive. Normative PET maps were acquired via the neuromaps toolbox.
