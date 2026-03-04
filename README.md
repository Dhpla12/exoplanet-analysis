# Exoplanet Demographic Analysis

This repository contains the Jupyter notebooks and analysis code used in the paper  
**"A Self‑Directed Census: Analyzing 6,105 Confirmed Exoplanets from First Principles"** by Aradhya Haldikar.

The notebooks download, filter, and quality‑flag confirmed exoplanet data from the NASA Exoplanet Archive, and reproduce all figures and tables from the paper.

## Repository Structure


exoplanet-analysis/
├── README.md                 # This file
├── requirements.txt          # Python dependencies
├── ExoplanetAnalysis.ipynb   # Python notebook to reproduce data with quality flags
├── Analysis/                 # All analysis notebooks
│   ├── MassRadiusRelation.ipynb
│   ├── NeptuneDesert.ipynb
│   ├── MetallicityDependence.ipynb
│   ├──PeriodValleyByPlanetSize.ipynb
|   └──README.md
└── LICENSE


## Requirements

- Python 3.8+
- Required packages: `astroquery`, `pandas`, `numpy`, `matplotlib`, `scipy`

Install all dependencies with:
```bash
pip install astroquery pandas numpy matplotlib scipy
```

## Usage

Each notebook is self‑contained and can be run independently:

1. Clone the repository:
   ```bash
   git clone https://github.com/Dhpla12/exoplanet-analysis.git
   cd exoplanet-analysis
   ```
2. Open a notebook (e.g., in Jupyter or upload to Google Colab).
3. Run all cells. The notebook will:
   - Fetch the latest data from the NASA Exoplanet Archive.
   - Apply the same 30% uncertainty quality cuts used in the paper.
   - Generate the corresponding figure and print key numerical results.

## Data

- **Original data:** NASA Exoplanet Archive Planetary Systems Table – DOI: [10.26133/NEA13](https://doi.org/10.26133/NEA13)
- **Filtered dataset with quality flags:** Harvard Dataverse – DOI: [10.7910/DVN/WQGSNE](https://doi.org/10.7910/DVN/WQGSNE)

The filtered dataset contains all confirmed planets with additional columns `mass_quality` and `rade_quality` indicating whether the planet passes the 30% uncertainty cut.

## Results Summary

The four analysis notebooks reproduce the following key findings from the paper:

| Analysis | File | Key Result |
|----------|------|------------|
| 1 | `MassRadiusRelation.ipynb` | RV and transit planets share slope α≈0.38; intercepts differ, revealing detection bias. |
| 2 | `NeptuneDesert.ipynb` | The Neptune desert (2–6 R⊕, flux 10–100) contains **zero** planets after quality cuts. |
| 3 | `MetallicityDependence,ipynb` | Giants orbit metal‑rich stars (mean [Fe/H]=+0.09); smaller planets show no metallicity bias. |
| 4 | `PeriodValleyByPlanetSize.ipynb` | Giants avoid 10–30 day periods (12.5%), sub‑Neptunes peak there (40.9%). |

## Citation

If you use this repository, the notebooks, or the filtered dataset in your work, please cite:

- Haldikar, A. (2026). *Exoplanet Demographic Analysis* [Computer software]. GitHub.  
  [https://github.com/Dhpla12/exoplanet-analysis](https://github.com/Dhpla12/exoplanet-analysis)
- Haldikar, A. (2026). *Filtered Exoplanet Dataset with Quality Flags* [Data set]. Harvard Dataverse.  
  [https://doi.org/10.7910/DVN/WQGSNE](https://doi.org/10.7910/DVN/WQGSNE)

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please open an issue in this repository.
```
