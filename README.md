# MACS 30112 Final Project
## Group Member: Yi Wang, An Nisa Astuti

## Project Description

This project explores spatial inequality in Chicago by linking neighborhood socioeconomic conditions and city service responsiveness to school outcomes. We construct a community-area–level dataset covering all 77 Chicago community areas by merging four data sources: socioeconomic indicators from the American Community Survey (ACS), 311 service request metrics from the City of Chicago, and school-related measures from Chicago Public Schools (CPS) and the 5Essentials School Climate Survey.

**Research Questions:**
1. How does city service responsiveness vary across Chicago community areas?
2. How are neighborhood socioeconomic conditions associated with that variation in 311 responsiveness?
3. How do neighborhood conditions and 311 responsiveness jointly relate to school outcomes across community areas?

At the current stage, the repo includes completed data pipelines for ACS and 311 data, plus an EDA notebook with descriptive statistics and exploratory visualizations on the cleaned and merged dataset. Polished visuals and modeling will avaliable for final submission.


## Data

Link to retrive data on Onedrive: https://uchicagoedu-my.sharepoint.com/:f:/g/personal/ywang43_uchicago_edu/IgAhDqWs-A2xT7V2VShzdldrAXUrl4DsXYImh5FxN1RDwuw?e=bE9Cea

The above link contains the following data: 
- **ACS 5-Year Estimates, API**
- **Chicago 311 Service Requests City of Chicago Open Data, API**
- **Chicago Public Schools (CPS) Outcomes** **
- **5Essentials School Climate Survey** **

## Libraries

| pandas | 3.0.0 |
| numpy | 2.4.1 |
| matplotlib | 3.10.8 |
| requests | 2.32.5 |
| beautifulsoup4 (bs4) | 4.14.3 |
| geopandas | 1.1.2 |
| shapely | 2.1.2 |
| pyogrio | 0.12.1 |


## Repo Structure
```text
├── README.md
├── ACS_API.ipynb
├── api_311.ipynb
├── eda_analysis.ipynb
├── 5essentials_scraper_JSON.ipynb
└── MACS30112-Check-in-report_1.pdf
```

## Contributions

- **Yi Wang** 
1. Maintain 311 API extraction and raw monthly CSV outputs.
2. Cleaned 311 data and compute more responsiveness metrics.
3. Aggregate 311 measures to community area and produce the merge ready 311 metrics table.
4. Build the neighborhood disadvantage table aligned to community area , and produce a merge-ready disadvantage table.
5. EDA 


- **An Nisa Astuti**
1. Maintain 5Essentials web scraping and raw data outputs.
2. Cleaning each school data (5essentials, CPS community area, ISBE report card) and compute outcome metrics.
3. Aggregate school measures to community areas and produce the merge-ready school outcomes table.
4. Build visualization maps by community area both from school climate (5essentials and ISBE report card).
5. Merged 311, acs, and school data on community area.
6. EDA
