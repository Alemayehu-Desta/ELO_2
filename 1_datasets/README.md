# Datasets 

This folder contains all datasets used in the **FDI attraction** project.  
It documents the raw datasets, explains their sources and purposes, and provides background on dataset types to ensure full transparency and reproducibility.

Raw datasets in this folder are stored **exactly as downloaded**.  
All cleaning and transformation will be performed in the `2_data_preparation` folder.

---


---

## 📂 Folder Structure

```plaintext
1_datasets/
└── raw_data/
      ├── nations_netFDI.csv
      ├── country_GDP_size.csv
      ├── annual_GDP_growth.csv
      ├── trade_openness.csv
      ├── inflation.csv
      ├── corruption.csv
      ├── International_LPI.xlsx
      ├── electricity.csv
      ├── education.csv

```

# Dataset Documentation

Below is a detailed inventory of all raw datasets used in the project, describing their source, data type, and analytical purpose.

| File Name                  | Description                         | Source Link                                                                 | Years     | Purpose                              |
|---------------------------|--------------------------------------|------------------------------------------------------------------------------|-----------|---------------------------------------|
| **nations_netFDI.csv**     | Annual net inward FDI flows (USD)   | https://unctadstat.unctad.org                                               | 2010–2023 | **Target variable** for FDI modeling |
| **country_GDP_size.csv**   | GDP in current USD                  | https://data.worldbank.org/indicator/NY.GDP.MKTP.CD                         | 2010–2023 | Market size indicator                |
| **annual_GDP_growth.csv**  | GDP growth (% annual)               | https://data.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG                      | 2010–2023 | Economic dynamism                    |
| **trade_openness.csv**     | Trade (% of GDP)                    | https://data.worldbank.org/indicator/NE.TRD.GNFS.ZS                         | 2010–2023 | Openness & competitiveness           |
| **inflation.csv**          | Inflation, CPI (%)                  | https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG                         | 2010–2023 | Macroeconomic stability              |
| **corruption.csv**         | Corruption Perceptions Index        | https://www.transparency.org/en/cpi                                          | 2010–2023 | Governance quality                   |
| **International_LPI.xlsx** | Logistics Performance Index         | https://lpi.worldbank.org/                                                  | 2007–2018 | Infrastructure & logistics           |
| **electricity.csv**        | Electricity access (% population)   | https://data.worldbank.org/indicator/EG.ELC.ACCS.ZS                         | 2010–2023 | Infrastructure reliability           |
| **education.csv**          | Secondary & tertiary enrollment (%) | https://data.worldbank.org/indicator/SE.SEC.ENRR                            | 2010–2023 | Human capital readiness              |
