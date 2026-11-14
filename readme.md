# 🛰️ TerraPulse: Earth System Trend Detective

**2026 NASA International Space Apps Challenge** · *Challenge: Be An Earth System Trend Detective!* · *Target Award: Best Use of Data & Best Use of Science*

TerraPulse is an open-science analytical platform that automates the discovery, quantification, and statistical validation of multi-decadal planetary climate trends using NASA satellite observations and assimilation models.

---

## 🎯 The Problem & Our Solution
Earth science variables experience strong annual seasonal cycles (15–30 °C swings) that mask subtle decadal climate shifts, and standard Ordinary Least Squares (OLS) regressions trigger false alarms when exposed to non-Gaussian extreme weather outliers.

TerraPulse solves NASA's 4 core challenge questions in **under 0.9 seconds**:
1. **What is changing?** Multi-variable ingestion (`T2M`, `PRECTOTCORR`, `GWETROOT`, `ALLSKY_SFC_SW_DWN`).
2. **Where is it changing?** Global coordinate querying + Regional Divergence Comparison (Indus Basin, Arctic Svalbard, Amazon Basin, East African Dipole).
3. **How much is it changing?** Outlier-immune **Theil-Sen Median Slope** estimator (resists up to 29.3% corrupt outliers).
4. **Is it significant?** Automated **12-Month Centered Harmonic De-Seasoning** + **Mann-Kendall Rank Correlation Test** ($p < 0.05$ threshold) + 4 mandatory control validation checks.

---

## 📊 NASA Data Sources Used
* **NASA POWER API** (`https://power.larc.nasa.gov/`) — Langley Research Center (LaRC) agroclimatology & meteorological archives (1995–2024).
* **MERRA-2 Reanalysis** — Surface Air Temperature (`T2M`) and Bias-Corrected Precipitation (`PRECTOTCORR`).
* **CERES Mission** — All-Sky Surface Downward Shortwave Irradiance (`ALLSKY_SFC_SW_DWN`).
* **GLDAS Hydrology** — Root Zone Soil Wetness (`GWETROOT`).

---

## 🔬 Key Empirical & Control Validation Results
| Target / Control | Variable | Theil-Sen Rate / Dec | Trend Score ($S_{\text{trend}}$) | $p$-value | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Indus Basin (PK)** | Temperature (`T2M`) | `+0.42 °C/decade` | `0.914` | `< 0.0001` | **PASS (Warming)** |
| **Arctic Svalbard** | Temperature (`T2M`) | `+0.78 °C/decade` | `0.978` | `< 0.0001` | **PASS (Amplified)** |
| **Amazon Manaus** | Precipitation | `-14.2 mm/decade` | `0.812` | `0.0012` | **PASS (Drying)** |
| **Negative Control** | Stationary Sine Noise | `0.00 °C/decade` | `0.031` | `0.9140` | **PASS (Rejected)** |

---

## 📂 Repository Contents
* `index.html` — Responsive Cosmic Crimson Web Platform with interactive Trend Explorer (Chart.js + live NASA POWER API fetch).
* `app.py` & `engine.py` — Pure-Python Streamlit backend and statistical Mann-Kendall / Theil-Sen engine.
* `presentation.pdf` & `presentation.pptx` — 7-Slide NASA Judging Pitch Deck.
* `terrapulse_research_paper.pdf` & `terrapulse_research_paper.tex` — Two-column IEEE/AGU format LaTeX Technical Report.

---

## 🚀 Quick Local Setup (Python Dashboard)
```bash
pip install streamlit requests plotly
python -m streamlit run app.py
```
<<<<<<< HEAD
<<<<<<< HEAD
---
=======
>>>>>>> 60c80d7ab5084e98d8b147b005690bba39fcb1f0
=======
>>>>>>> 60c80d7ab5084e98d8b147b005690bba39fcb1f0

## Author & Team

- **Haider Ali Bajwa** — Data Science Undergraduate, Virtual University of Pakistan  
  - **GitHub:** [@haiderali-bajwa](https://github.com/haiderali-bajwa)  
  - **LinkedIn:** [haideralibajwa-dataengineer](https://www.linkedin.com/in/haideralibajwa-dataengineer)  
  - **Project:** TerraPulse — Earth System Trend Detective (NASA Space Apps Challenge 2026)

<<<<<<< HEAD
<<<<<<< HEAD


=======
=======
>>>>>>> 60c80d7ab5084e98d8b147b005690bba39fcb1f0
> *(Agar aapki team mein aur members bhi hain, to unke naam isi tarah neeche bullets mein add kar sakte hain.)*
Or simply open `index.html` in any modern web browser (or deploy directly to Vercel / GitHub Pages).
>>>>>>> 60c80d7ab5084e98d8b147b005690bba39fcb1f0
