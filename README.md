# Spatial Inequality in Chicago: City Services, Neighborhood Conditions, and School Outcomes

---

# Project Description

## Summary

This project explores spatial inequality in Chicago by linking neighborhood socioeconomic conditions and city service responsiveness to school outcomes across all 77 community areas.

- **Topic**: Urban inequality: how neighborhood disadvantage and municipal service quality jointly shape educational outcomes at the community-area level
- **Research Questions**:
  1. How does city service responsiveness (via 311 requests) vary across Chicago community areas?
  2. How are neighborhood socioeconomic conditions associated with that variation in 311 responsiveness?
  3. How do neighborhood conditions and 311 responsiveness jointly relate to school outcomes across community areas?
- **Why it matters**: Understanding whether city services systematically underperform in disadvantaged neighborhoods, and whether that gap compounds worse school outcomes has direct implications for equity-focused urban policy and resource allocation.

## Additional Info

**Total lines of code**: *7871*

**Methods and Analysis**: The project constructs a community-area–level panel by merging ACS socioeconomic indicators, 311 service request metrics, CPS outcomes, and 5Essentials School Climate Survey data. Analysis includes descriptive spatial EDA, responsiveness metrics aggregated to community areas, and multivariate modeling of school outcomes.

**Project strength**: Data collection and wrangling — four heterogeneous administrative and survey sources were cleaned, harmonized, and merged at the community-area level across all 77 Chicago neighborhoods.

---

# Data

Due to github file size, all the raw data are in the OneDrive link.
All data are accessible via the project OneDrive: [https://uchicagoedu-my.sharepoint.com/:f:/g/personal/ywang43_uchicago_edu/IgAhDqWs-A2xT7V2VShzdldrAXUrl4DsXYImh5FxN1RDwuw?e=bE9Cea](https://uchicagoedu-my.sharepoint.com/:f:/g/personal/ywang43_uchicago_edu/IgAhDqWs-A2xT7V2VShzdldrAXUrl4DsXYImh5FxN1RDwuw?e=bE9Cea)

| Source | Collection Method | Notes |
|--------|------------------|-------|
| ACS 5-Year Estimates | API | Neighborhood socioeconomic indicators at the community-area level |
| Chicago 311 Service Requests (City of Chicago Open Data) | API | Used to compute responsiveness metrics aggregated by community area |
| Chicago Public Schools (CPS) Outcomes | Download | School-level outcomes aggregated to community areas |
| 5Essentials School Climate Survey | Web scraping | School climate measures scraped via JSON; aggregated to community areas |

---

# Repository Structure

```text
Spatial Inequality in Chicago/
├── data/
│   ├── raw
        └── https://uchicagoedu-my.sharepoint.com/my?id=%2Fpersonal%2Fywang43%5Fuchicago%5Fedu%2FDocuments%2Fspatial%5Fedu%5Finequality&ga=1          
│   └── clean/
│       └── final_merged_data.csv
│
├── code/
│   ├── scraping/
│   │   ├── 311_API.ipynb
│   │   ├── ACS_API.ipynb
│   │   └── 5essentials_scraper_JSON.ipynb
│   ├── cleaning/
│   │   └── crosswalk_and_merge.ipynb
│   └── analysis/
│       ├── eda_analysis.ipynb
│       └── maps_spatial_analysis.ipynb
│
├── docs/
│   ├── MACS30112-Check-in-report_1.pdf
│   └── MACS30112-Check-in-report_2.pdf
│
└── README.md
```

---

# Libraries

| Library | Version |
|---------|---------|
| pandas | 3.0.1 |
| numpy | 2.4.2 |
| matplotlib | 3.10.8 |
| seaborn | 0.13.2 |
| requests | 2.32.5 |
| beautifulsoup4 (bs4) | 4.14.3 |
| geopandas | 1.1.2 |
| geopy | 2.4.1 |
| statmodels | 0.14.6 |
| shapely | 2.1.2 |
| pyogrio | 0.12.1 |

---

# Contributions

- **Yi Wang**
  1. Maintained 311 API extraction and raw monthly CSV outputs (`api_311.ipynb`)
  2. Cleaned 311 data and computed responsiveness metrics
  3. Aggregated 311 measures to community area and produced the merge-ready 311 metrics table
  4. Built the neighborhood disadvantage table aligned to community area using ACS data (`ACS_API.ipynb`), producing a merge-ready disadvantage table
  5. Contributed to EDA (`eda_analysis.ipynb`)
  6. Building presentation slides
  7. Core focus area (`maps_spatial_analysis.ipynb`)

- **An Nisa Astuti**
  1. Maintained 5Essentials web scraping and raw data outputs (`5essentials_scraper_JSON.ipynb`)
  2. Cleaned school data (5Essentials, CPS community area) and computed outcome metrics
  3. Aggregated school measures to community areas and produced the merge-ready school outcomes table
  4. Built choropleth visualizations by community area for school climate measures
  5. Merged 311, ACS, and school data on community area
  6. Contributed to EDA (`eda_analysis.ipynb`)
  7. Statistical test on merged data
  8. Building presentation slides

---

# AI Disclosure

**Tools used:** ChatGPT (OpenAI)

| Notebook / Script | How AI Was Used |
|---|---|
| 311 Data Collection | Used ChatGPT to learn the Socrata API documentation, understand pseudo code for query construction, set pagination parameters, and troubleshoot HTTP/API errors. All final implementation written by author. |
| ACS API (2020–2024) | Used ChatGPT to learn the `geopandas` library, specifically CRS transformations, computing tract centroids, and performing spatial joins via `geopandas.sjoin` to map ACS tracts to Chicago community areas. All analytical decisions written by author. |
| 5Essentials Scraping | Used ChatGPT to explore Selenium-based scraping approaches after initial BeautifulSoup attempts returned empty results. AI helped identify that data was embedded as static JSON in `<script id="app_data">` tags; extraction logic was written by author. |
| EDA — Final Merged Dataset | Used AI to assist with visualization formatting, including figure sizing, color scale selection, and annotation formatting. All analytical decisions, interpretations, and code logic written by authors. |
| Spatial Analysis & Choropleth Maps | Used AI for visualization formatting and parameter tuning, and to learn `geopandas` library syntax. All analytical decisions, interpretations, and final code written by author. |

> AI was not used to make analytical or interpretive decisions in any notebook.

---

# Project Links

- **Slides used in the in-class presentation**:  *[https://docs.google.com/presentation/d/18Ybuan_dNogiu0-gnRP2WECu4tGWBRXt/edit?slide=id.p1#slide=id.p1]*
- **Updated final slides (full version)**: *[https://docs.google.com/presentation/d/1AdrIZwXAAbU1cmelk-YZXIAh82JaIZDfu79rKRBCtO4/edit?usp=sharing]*
- **Presentation video**: *[https://uchicagoedu-my.sharepoint.com/:f:/g/personal/ywang43_uchicago_edu/IgC7pfQWgkYXSIZmsERGgjxPARQKWJcO_chrW9xippm9-vk?e=DAP6ve]*
