# Exoplanet Demographic Analysis

This repository contains the Jupyter notebook used to download, filter, and quality‑flag confirmed exoplanet data from the NASA Exoplanet Archive. The analysis is part of the paper *"A Self‑Directed Census: Analyzing 6,105 Confirmed Exoplanets from First Principles"* by Aradhya Haldikar.

## Overview

The notebook:
- Fetches data from the NASA Exoplanet Archive (Planetary Systems table, `default_flag=1`) using `astroquery`.
- Computes fractional uncertainties for planetary mass and radius.
- Flags planets with fractional uncertainty <30% as reliable.
- Exports a CSV file containing all original columns plus quality flags (`mass_quality`, `rade_quality`).

The resulting dataset is used for the demographic analysis presented in the paper.

## Requirements

- Python 3.8+
- Required packages: `astroquery`, `pandas`, `numpy`

Install dependencies with:
```bash
pip install astroquery pandas numpy
```

## Usage
Clone this repository:

bash
git clone https://github.com/YOUR_USERNAME/exoplanet-analysis.git
cd exoplanet-analysis
Open the notebook in Jupyter (or Google Colab):

```bash
jupyter notebook ExoplanetAnalysis.ipynb
```

(If using Colab, upload the notebook and run it there.)

Run all cells sequentially. The final cell will generate exoplanet_data_with_quality.csv and offer a download link.

## Data Source
All original data are from the NASA Exoplanet Archive:

Planetary Systems Table (ps) – DOI: 10.26133/NEA13

Accessed: March 2026

The filtered dataset with quality flags is archived at Harvard Dataverse:

DOI: 10.7910/DVN/WQGSNE

## Output
exoplanet_data_with_quality.csv – Contains 6,128 rows (one per confirmed planet) with the following added columns:

mass_frac_err : fractional mass uncertainty (NaN if errors missing)

rade_frac_err : fractional radius uncertainty (NaN if errors missing)

mass_quality : True if mass uncertainty <30% and errors present

rade_quality : True if radius uncertainty <30% and errors present

## Citation
If you use this notebook or the filtered dataset in your work, please cite:

Haldikar, A. (2026). Exoplanet Demographic Analysis [Computer software].
- GitHub. https://github.com/Dhpla12/exoplanet-analysis

Haldikar, A. (2026). The filtered dataset with quality flags is archived at **Harvard Dataverse**:
- DOI: [10.7910/DVN/WQGSNE](https://doi.org/10.7910/DVN/WQGSNE)

## License
This project is licensed under the MIT License – see the LICENSE file for details.
