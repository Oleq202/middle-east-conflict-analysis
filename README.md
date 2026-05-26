# Middle East Conflict Analysis

An exploratory data analysis of armed conflict events recorded across the Middle East from **2014 to early 2026**, rendered as an interactive HTML report and published via GitHub Pages.

🔗 **[View the report](https://Oleq202.github.io/middle-east-conflict-analysis/)**

---

## Overview

This report examines over a decade of weekly conflict records across 14 countries in the Middle East, sourced from aggregated ACLED-style data. The analysis covers:

- **Geographic distribution** of conflict events and population exposure
- **Event composition** by country and sub-event type (battles, explosions, protests, riots, etc.)
- **Casualty patterns** — civilian vs. non-civilian fatalities
- **Temporal trends** in total and civilian fatalities from 2014 to 2026

Key findings include the unprecedented spike in Palestinian civilian fatalities in 2024, the emergence of a large-scale conflict in Iran in early 2026, and a region-wide shift toward remote/technological warfare (air strikes, drone attacks, artillery).

---

## Repository Structure

```
middle-east-conflict-analysis/
├── index.html        # Rendered interactive report (GitHub Pages entry point)
├── analysis.Rmd      # R Markdown source
├── analysis.md       # Knitted markdown output
├── README.md
└── conflict data/    # Input datasets (see Data section below)
```

---

## Data

The analysis relies on three Excel datasets placed in the `conflict data/` directory:

| File | Description |
|------|-------------|
| `Middle-East_aggregated_data_up_to-2026-02-28.xlsx` | Weekly aggregated conflict events by country, event type, and location |
| `number_of_reported_fatalities_by_country-year_as-of-06Mar2026.xlsx` | Annual total fatalities per country |
| `number_of_reported_civilian_fatalities_by_country-year_as-of-06Mar2026.xlsx` | Annual civilian fatalities per country |

> The data files are not included in this repository. Place them in `conflict data/` before knitting the report.

---

## Reproducing the Report

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/middle-east-conflict-analysis.git
   cd middle-east-conflict-analysis
   ```

2. **Add the data files** to the `conflict data/` directory.

3. **Install R dependencies**
   ```r
   install.packages(c(
     "readxl", "dplyr", "ggplot2", "tidyverse",
     "arrow", "plotly", "scales", "rnaturalearth",
     "rnaturalearthdata", "sf", "htmltools"
   ))
   ```

4. **Knit the report** in RStudio or via the R console:
   ```r
   rmarkdown::render("analysis.Rmd", output_file = "index.html")
   ```

---

## GitHub Pages Setup

1. Go to **Settings → Pages** in your repository.
2. Under *Source*, select **Deploy from a branch**.
3. Choose `main` branch and `/ (root)` folder.
4. Save — the report will be live at `https://Oleq202.github.io/middle-east-conflict-analysis/`.

---

## Tools & Libraries

- **R** with `rmarkdown`, `ggplot2`, `plotly`, `dplyr`, `sf`, `rnaturalearth`
- **GitHub Pages** for hosting
