# Mycale grandis Substrate Association Analysis

## Project Overview

This project investigates whether the invasive sponge *Mycale grandis* shows a preferential association with *Porites compressa* coral beyond what would be expected based on substrate availability alone in Kāne'ohe Bay, O'ahu, Hawai'i.

---

## Research Question

Does *Mycale grandis* attach to *Porites compressa* simply because it's abundant, or does it show a true preference for this coral species?

---

## Background

*Mycale grandis* is an alien invasive sponge introduced to Hawaiian waters in the late 1990s, likely through ship hull biofouling. It has become the most aggressive invasive sponge on Hawaiian reefs, overgrowing native reef-building corals including *Montipora capitata* and *Porites compressa*.

---

## Methods

- **Data:** Sponge survey data from 10 sites across Kāne'ohe Bay
- **Analysis:** Beta-binomial regression to test relationship between *P. compressa* availability and *M. grandis* attachment
- **Visualization:** ggplot2 with colorblind-friendly palette

---

## Key Findings

- Highly significant positive relationship between *P. compressa* cover and *M. grandis* attachment (p < 0.001)
- R² = 0.873 indicates strong relationship
- *M. grandis* attachment largely tracks substrate availability rather than showing active preference
- Site-level variation suggests other environmental factors may influence settlement patterns

---

## Repository Structure
```
MBIO612_Final_Project/
│
├── data/
│   ├── permgsubassoc.csv      # M. grandis substrate associations
│   ├── fullsurvey.csv         # All sponge observations
│   └── transect_data.xlsx     # Benthic cover data
│
├── scripts/
│   └── mycale_analysis.qmd    # Main analysis document
│
├── output/
│   ├── plot1_all_sponges.png
│   ├── plot2_mg_substrate.png
│   ├── plot3_regression.png
│   └── Sponge_Reference_Table.png
│
├── data_dictionary.md         # Variable descriptions
├── README.md                  # This file
└── mycalearmata1.jpg          # M. grandis image
```

---

## Packages Used

- `tidyverse` - Data wrangling and visualization
- `readxl` - Reading Excel files
- `here` - Reproducible file paths
- `VGAM` - Beta-binomial regression
- `kableExtra` - Styled tables
- `ggrepel` - Clean plot labels
- `scales` - Axis formatting
- `patchwork` - Combining plots

---

## How to Run

1. Clone this repository
2. Open `scripts/mycale_analysis.qmd` in RStudio
3. Install required packages (see above)
4. Render the Quarto document

---

## Author

**Emily Rutkowski**  
University of Hawai'i at Mānoa  
OCN 682 - Data Science Fundamentals in R  
Fall 2025

---

## References

- Coles, S. L., Marchetti, J., Bolick, H., & Montgomery, A. (2007). Assessment of invasiveness of the Orange Keyhole Sponge *Mycale armata* in Kāne'ohe Bay, O'ahu, Hawai'i. Final Report, Year 2. Hawaii Coral Reef Initiative Research Program.

- Shih, J. L., & Popp, B. N. (2020). Assessment of an invasive tropical sponge on coral reefs in Hawai'i. *Pacific Science*, 74(2), 175-187.

- Vicente, J., Silbiger, N. J., Beckley, B. A., Raczkowski, C. W., & Hill, R. T. (2016). Impact of high pCO₂ and warmer temperatures on the process of silica biomineralization in the sponge *Mycale grandis*. *ICES Journal of Marine Science*, 73(3), 704-714.
