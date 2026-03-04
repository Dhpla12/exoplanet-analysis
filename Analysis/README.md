# Analysis – Notebooks for Exoplanet Demographic Study

This folder contains the Jupyter notebooks used to generate the figures and tables in the paper:

**"A Self-Directed Census: Analyzing 6,105 Confirmed Exoplanets from First Principles" (Haldikar, 2026).**

Each notebook is fully self-contained and fetches the latest data directly from the NASA Exoplanet Archive, ensuring reproducibility.

---

## Notebooks

| # | File Name                         | Description                                                                                                                     |
| - | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 1 | `01_mass_radius_fit.ipynb`        | Mass–radius relation by discovery method; power-law fits for radial velocity, transit, and imaging planets (Figure 1, Table 3). |
| 2 | `02_neptune_desert.ipynb`         | Flux–radius diagram highlighting the Neptune desert; confirms zero planets in the desert region after quality cuts (Figure 2).  |
| 3 | `03_metallicity_dependence.ipynb` | Host star metallicity distributions for super-Earths, sub-Neptunes, and giants; Kolmogorov–Smirnov tests (Figure 3, Table 5).   |
| 4 | `04_period_valley.ipynb`          | Orbital period histograms for different planet sizes; quantifies the 10–30 day valley (Figure 4).                               |

---

## How to Run

### 1. Install dependencies (if not already present)

```bash
pip install astroquery pandas numpy matplotlib scipy
```

### 2. Open the notebook

Open any notebook in Jupyter Notebook, JupyterLab, or upload it to Google Colab.

### 3. Run all cells sequentially

Each notebook will:

* Query the NASA Exoplanet Archive
* Apply the same 30% uncertainty quality cuts used in the paper
* Generate the corresponding figure
* Print the key numerical results

---

## Data

Original data: NASA Exoplanet Archive Planetary Systems Table
DOI: 10.26133/NEA13

Filtered dataset with quality flags: Harvard Dataverse
DOI: 10.7910/DVN/WQGSNE

---

## Citation

If you use these notebooks or the filtered dataset, please cite:

Haldikar, A. (2026). *Exoplanet Demographic Analysis* [Computer software]. GitHub.
[https://github.com/Dhpla12/exoplanet-analysis](https://github.com/Dhpla12/exoplanet-analysis)

Haldikar, A. (2026). *Filtered Exoplanet Dataset with Quality Flags* [Data set]. Harvard Dataverse.
[https://doi.org/10.7910/DVN/WQGSNE](https://doi.org/10.7910/DVN/WQGSNE)

---

## Contact

For questions or feedback, open an issue on the main repository or contact the author via GitHub.
