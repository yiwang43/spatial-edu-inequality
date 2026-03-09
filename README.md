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
- **Why it matters**: Understanding whether city services systematically underperform in disadvantaged neighborhoods — and whether that gap compounds worse school outcomes — has direct implications for equity-focused urban policy and resource allocation.

## Additional Info

**Total lines of code**: *[insert count — use `find . -name "*.py" -o -name "*.ipynb" | xargs wc -l`]*

**Methods and Analysis**: The project constructs a community-area–level panel by merging ACS socioeconomic indicators, 311 service request metrics, CPS outcomes, and 5Essentials School Climate Survey data. Analysis includes descriptive spatial EDA, responsiveness metrics aggregated to community areas, and multivariate modeling of school outcomes.

**Project strength**: Data collection and wrangling — four heterogeneous administrative and survey sources were cleaned, harmonized, and merged at the community-area level across all 77 Chicago neighborhoods.

---

# Data

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
├── README.md
├── ACS_API.ipynb
├── api_311.ipynb
├── eda_analysis.ipynb
├── 5essentials_scraper_JSON.ipynb
└── MACS30112-Check-in-report_1.pdf
```

*Full structure to be updated for final submission.*

---

# Libraries

| Library | Version |
|---------|---------|
| pandas | 3.0.0 |
| numpy | 2.4.1 |
| matplotlib | 3.10.8 |
| requests | 2.32.5 |
| beautifulsoup4 (bs4) | 4.14.3 |
| geopandas | 1.1.2 |
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

- **An Nisa Astuti**
  1. Maintained 5Essentials web scraping and raw data outputs (`5essentials_scraper_JSON.ipynb`)
  2. Cleaned school data (5Essentials, CPS community area, ISBE report card) and computed outcome metrics
  3. Aggregated school measures to community areas and produced the merge-ready school outcomes table
  4. Built choropleth visualizations by community area for school climate measures
  5. Merged 311, ACS, and school data on community area
  6. Contributed to EDA (`eda_analysis.ipynb`)

---

# AI Usage Statement

*[List which AI tools were used (e.g., ChatGPT, Claude, GitHub Copilot) and describe specifically how each was used — e.g., debugging, drafting docstrings, structuring code logic. Each script in the repo should also include an author note and AI disclosure at the top.]*

---

# Project Links

- **Slides used in the in-class presentation**: *[link]*
- **Updated final slides (full version)**: *[link]*
- **Presentation video**: *[link]*
