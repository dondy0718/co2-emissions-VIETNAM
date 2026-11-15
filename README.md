# CO₂ Emissions Analysis: Vietnam

**Student:** [Enter your full name]  
**Country / ISO-3:** Vietnam / VNM  
**Study period:** 1990–2024  
**Date data accessed:** 15 November 2026  
**Declared to instructor on:** [Enter declaration date]

## Research question

How have annual CO₂ emissions and per-capita emissions changed in Vietnam from 1990 to 2024?

## Data source and definitions

This analysis uses the Our World in Data (OWID) CO₂ and Greenhouse Gas Emissions dataset, sourced from the Global Carbon Budget.

- Dataset page: https://github.com/owid/co2-data
- Direct full CSV: https://owid-public.owid.io/data/co2/owid-co2-data.csv
- OWID CO₂ data explainer: https://ourworldindata.org/co2-and-greenhouse-gas-emissions

The selected variables are `year`, `co2`, and `co2_per_capita`. The `co2` variable measures annual CO₂ emissions from fossil fuels and industrial processes in **million tonnes per year**. It excludes land-use change. The `co2_per_capita` variable measures **tonnes of CO₂ per person per year**. These indicators are not atmospheric CO₂ concentrations and do not represent all greenhouse gases.

## How to reproduce the analysis

1. Install R, RStudio, and Git.
2. Open `Vietnam_CO2_Emissions_Analysis.Rproj` in RStudio.
3. Make sure the project root is the working directory.
4. Run the following command in the RStudio Console:

   ```r
   source("scripts/analyze_co2.R")
   ```

5. The script downloads the full OWID CSV to `data/owid-co2-data.csv` if it is not already present, filters Vietnam (`VNM`) for 1990–2024, saves the country-only CSV, and recreates the figures and results.
6. Inspect the files in `data/`, `figures/`, and `results/`.

No additional R packages are required. The full multi-country source file is excluded from version control through `.gitignore`; do not upload it.

## Results

- **Earliest valid year:** 1990
- **Latest valid year:** 2024
- **Annual emissions in 1990:** 21.4855 million tonnes CO₂
- **Annual emissions in 2024:** 357.4511 million tonnes CO₂
- **Change from 1990 to 2024:** +1,563.7%
- **Peak annual emissions:** 2024, at 357.4511 million tonnes CO₂
- **Latest per-capita value (2024):** 3.5396 tonnes CO₂ per person
- **Highest per-capita value in the study period:** 2020, at 3.5453 tonnes per person

### Figures

![Vietnam annual CO2 emissions](figures/VNM_annual_co2.png)

![Vietnam CO2 emissions per capita](figures/VNM_per_capita.png)

![Vietnam annual percentage change](figures/VNM_annual_change.png)

## Interpretation (264 words)

From 1990 to 2024, Vietnam’s annual CO₂ emissions from fossil fuels and industry rose from 21.4855 million tonnes to 357.4511 million tonnes, an increase of 1,563.7%. The series shows a sustained upward trend, with particularly rapid growth after the mid-2000s and a sharp rise from 228.3345 million tonnes in 2017 to 339.3180 million tonnes in 2019. Annual emissions then reached 347.7221 million tonnes in 2020, declined to 323.3687 million tonnes in 2022, and rebounded to a new high of 357.4511 million tonnes in 2024. The largest annual total in the study period therefore occurred in 2024.

Absolute emissions and per-capita emissions describe different aspects of the pattern. Total emissions measure the country’s overall annual contribution, while per-capita emissions divide that total by population and indicate average emissions per person. Vietnam’s per-capita value increased from 0.3280 tonnes in 1990 to 3.5396 tonnes in 2024. However, the highest per-capita value in the selected period was 3.5453 tonnes in 2020, slightly above 2024’s value.

The 2024 rebound may be related in part to electricity generation. The OECD reports that coal supplied around half of Vietnam’s electricity and that coal-fired generation and emissions rose by 15% in 2024 compared with 2023. This provides context, but the time-series alone cannot prove that coal use caused the national increase. National emissions matter because fossil-fuel CO₂ contributes to global warming, which can affect ecosystems, habitats, biodiversity, and climate-related risks. These figures are territorial and exclude land-use change; they also do not assign emissions from imported goods to Vietnam. They therefore do not represent every climate impact or the full consumption footprint.

## Limitations

1. The dataset measures territorial emissions: it counts emissions produced within Vietnam’s borders and does not adjust for emissions embodied in imported or exported goods.
2. The `co2` indicator covers fossil fuels and industrial processes but excludes land-use change. It does not include all greenhouse gases, such as methane and nitrous oxide.
3. Country-level annual data can hide differences among provinces, industries, communities, and households.
4. A time-series can show patterns and associations, but it cannot by itself establish why emissions changed.
5. Missing values, if any, must remain missing; they must not be replaced with zero. The selected Vietnam series has valid annual observations for every year from 1990 through 2024.

## References

- Our World in Data. (2026). *CO₂ and Greenhouse Gas Emissions*. Global Carbon Budget data. https://ourworldindata.org/co2-and-greenhouse-gas-emissions
- Our World in Data. *CO₂ and Greenhouse Gas Emissions dataset*. https://github.com/owid/co2-data
- OECD. (2025). *OECD Economic Surveys: Viet Nam 2025 — Unlocking low-carbon economic growth*. https://www.oecd.org/en/publications/oecd-economic-surveys-viet-nam-2025_fb37254b-en/full-report/unlocking-low-carbon-economic-growth_d1fdfa53.html

## GitHub publication status

**Step 2 (creating a personal GitHub repository) was intentionally skipped as requested.** This folder is prepared as a local RStudio project. GitHub cloning, pushing, and submission of a public repository URL and latest commit URL remain incomplete because those steps require a GitHub repository.
