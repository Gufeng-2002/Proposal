# Proposal for "Zoobenthic Community Indicators of Sediment Contamination"

## 📖 Repository Overview

This repository contains the thesis proposal for developing zoobenthic community indicators to assess sediment contamination in large river systems, with specific application to the Lake Huron-Lake Erie Corridor. The research employs advanced data science methods including Principal Component Analysis (PCA), quantile regression, and spatial analysis to create threshold-capable bioindicators.

**Author:** Feng Gu  
**Institution:** Thompson Rivers University  
**Program:** Master of Science in Data Science
**Email:** gfeng643@gmail.com

## 🏗️ Repository Structure

### 📁 `/proposal/` - Main Thesis Proposal Document
Contains the complete LaTeX source and compiled PDF of the thesis proposal.

- **`Feng's_Proposal.tex`** - Main LaTeX document
- **`Feng's_Proposal.pdf`** - Compiled proposal document
- **`sections/`** - Individual LaTeX sections:
  - `Introduction.tex` - Project introduction and background
  - `LiteratureReview.tex` - Comprehensive literature review
  - `ResearchObjectives.tex` - Research goals and objectives
  - `Methodology.tex` - Detailed analytical framework
  - `DataDescription.tex` - Dataset descriptions and variables
  - `PreliminaryResults.tex` - Initial analysis results
  - `Timeline.tex` - Project timeline and milestones
  - `Reference.bib` - Bibliography database
  - `Appendix.tex` - Additional supporting materials

### 💻 `/src/` - Analysis Code and Notebooks
Jupyter notebooks containing all data analysis, modeling, and visualization code.

- **`PreliminaryAnalysis.ipynb`** - Main analysis notebook with preliminary results
- **`PCAAssessment.ipynb`** - Principal Component Analysis for pollution assessment
- **`DataCleaning.ipynb`** - Data preprocessing and quality control
- **`CreateMaps.ipynb`** - Spatial visualization and mapping
- **`pcnm_simulation_notebook.ipynb`** - Principal Coordinates of Neighbour Matrices (PCNM) analysis

### 📊 `/data/` - Research Datasets
Contains raw and processed ecological and chemical data from the Lake Huron-Lake Erie Corridor.

#### Raw Data Files:
- **`chemecal_Jian's_Chemical_data_and_PCA_factors_May_11_2006(RelMax)_for_Feng.xlsx`** - Chemical contamination data
- **`environmental_Copy_of_RelMax_classification_with_clusters_and_REFsite_to_predict_test_sites.xlsx`** - Environmental variables
- **`invertbrates_5_PC_ORD_Matrices_with_best_and_worst_endpoints(invertebrates_for_Feng).xlsx`** - Taxonomic abundance data
- **`Explanation of Variables and cluster groups from Jian for Feng.xlsx`** - Data dictionary and metadata

#### Subdirectories:
- **`original_xls_format/`** - Original Excel format datasets
- **`processed_data/`** - Cleaned and processed datasets
- **`maps/`** - Geographic data and shapefiles

### 📈 `/results/` - Analysis Results and Visualizations
Generated figures, plots, and analysis outputs.

#### Key Result Files:
- **`workflow_of_general_workframe_part1.png`** & **`workflow_of_general_workframe_part2.png`** - Methodology workflow diagrams
- **`map_of_huron_erie_corridor.png`** - Study area map
- **`different_data_sampling_locations.png`** - Sampling location visualization
- **`selected_PCs_of_weights.png`** - PCA component analysis
- **Violin plots:** Various data distribution visualizations
  - `violin_plot_ori_taxa_data.png`
  - `violin_plot_log_transformed_taxa_data.png`
  - `violin_plot_standardized_metal_groups.png`
- **Quantile regression results:**
  - `quantile_regression_homoscedastic_taus_of_1000size.png`
  - `more_CIs_quantile_regression_heteroscedastic_taus_of_1000size.png`

#### Subdirectories:
- **`preliminary_results/`** - Early analysis outputs
- **`ideas_visualization/`** - Conceptual diagrams and visualizations

### 🎯 `/presentation/` - Presentation Materials
LaTeX Beamer presentation and supporting materials.

- **`presentation.tex`** - LaTeX Beamer source
- **`presentation.pdf`** - Compiled presentation slides
- **`figures/`** - Presentation-specific figures and diagrams

### 📋 `/templates/` - Document Templates
Reusable templates for reports and documentation.

## 🔬 Research Methodology

The project employs a comprehensive 6-step analytical framework:

1. **Dimension Reduction on Stressors** - PCA-based pollution scoring to reveal synthetic stressor gradients
2. **Reference Site Identification** - Counterfactual surface estimation for minimal pollution scenarios
3. **Taxa Variable Ordination** - Comprehensive zoobenthic community measurement construction
4. **Spatial Analysis** - Geographic heterogeneity testing with spatial eigenvectors (PCNM)
5. **Quantile Regression Modeling** - Threshold detection across different quantile levels
6. **Robustness Assessment** - Sample size and environmental distribution sensitivity analysis

## 📊 Key Datasets

### Environmental Variables (5 attributes):
- Temperature (°C)
- Dissolved oxygen concentration (mg/L)
- Water depth (m)
- Loss on ignition (%)
- Median particle size (phi-units)
- Water velocity (m/s) - Detroit River area only

### Taxonomic Variables (16 taxa):
Benthic invertebrates categorized by habitat preference:
- **Broad habitat:** Nematoda, Chironomidae, Ceratopogonidae, Amphipoda, Acari, Hydrozoa, Gastropoda
- **Depositional zone:** Oligochaeta, Hexagenia, Dreissena, Hirudinea, Turbellaria, Sphaeriidae
- **Erosional zone:** Caenis, Hydropsychidae, Other Trichoptera

### Stressor Variables (30 chemical elements):
- **Earth elements:** Al, Ca, Fe, K, Mg, Na
- **Trace metals:** As, Bi, Cd, Co, Cr, Cu, Hg, Mn, Ni, Pb, Sb, V, Zn
- **Organic carbon:** %OC
- **Organic contaminants:** PCBs, chlorinated compounds, pesticides

## 🚀 Getting Started

### Prerequisites
- **LaTeX Distribution:** TeXLive or MiKTeX for document compilation
- **Python 3.8+** with Jupyter Notebook support
- **Required Python packages:** pandas, numpy, matplotlib, seaborn, scikit-learn, scipy

### Compiling the Proposal
```bash
cd proposal/
pdflatex "Feng's_Proposal.tex"
bibtex "Feng's_Proposal"
pdflatex "Feng's_Proposal.tex"
pdflatex "Feng's_Proposal.tex"
```

### Running Analysis Code
```bash
cd src/
jupyter notebook
# Open and run the desired .ipynb files
```

## 📝 Key Research Contributions

1. **Novel ZCI Framework:** Development of a Zoobenthic Community Index (ZCI) using multivariate Gaussian modeling
2. **Spatial Adjustment:** Integration of PCNM spatial eigenvectors for controlling geographic autocorrelation
3. **Threshold Detection:** Piecewise quantile regression for identifying ecological breakpoints
4. **Methodological Innovation:** Data-driven approach avoiding reliance on background concentration estimates

## 📚 Citations and References

This work builds upon extensive literature in aquatic ecology, sediment contamination assessment, and quantile regression methods. The complete bibliography is maintained in `proposal/sections/Reference.bib`.

## 📄 License

This research proposal and associated code are part of an academic thesis project. Please contact the author for permission before using or redistributing any materials.

---

**Last Updated:** October 2025  
**Status:** Thesis Proposal Submitted
