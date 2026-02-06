MACS 30112 Final Project
Yi Wang, An Nisa Astuti
RQ: How do differences in Chicago 311 service responsiveness and neighborhood conditions relate to CPS school outcomes across Chicago community areas?

This repo contains data-collection pipelines. 
1) **CPS 5Essentials (school climate)**: scraping/collecting school-level measures (2022–2025) and aggregating to community areas for spatial analysis  
2) **Chicago 311 service requests**: pulling service-request records from 2021-2025 via the City of Chicago Socrata API, response-time / service-performance metrics

---

## Contents

- `5Essentials Data Collection and Processing`  
  Web scraping pipeline for CPS 5Essentials school climate measures.
- `Chicago 311 API pipeline`  
  API pipeline using `sodapy` / Socrata client for Chicago 311 service requests.
