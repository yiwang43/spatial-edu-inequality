Page
# Project Title

---

# Project Description

## Summary

Provide a short description of the project (max ~500 words!). 
Consider using bullet points to improve readability

It should include:

- the **topic** of the project  
- the **research question(s)**  
- why the question **matters**

## Additional info

Add the following info:

**Total lines of code**: approximate total lines of code (raw count of executable code across scripts, you can use tools to make the count automatically)  
**Methods and Analysis**: state your focus area and anything else you find useful to share here (keep it to 2-3 sentences)
**Project strength**: decide and state ONE strength among data collected, cleaning/wrangling, visuals, designs, etc.

---

# Data

Provide a **bullet list or a table of all data sources used in the project**.

For each source include:

- link to retrieve the data (add the actual data to the repo only if small, see Github data size limits)
- collection method: download / scraping / API
- anything else you want to share

---

# Repository Structure

Include a **tree-style schema** similar to the example below. 
You do not have to use this same identical organization (do what makes sense for you and your project),
but you should use a tree-style schema. 

Example:

```
your-project-name/
├── data/
│   └── raw/
│       ├── source_1/
│       └── source_2/
│   └── clean/
│       ├── source_1/
│       └── source_2/
│
├── code/
│   ├── scraping/
│   │   ├── scrape_source_1.py
│   │   ├── scrape_source_2.py
│   │   └── utils.py
│   │
│   ├── cleaning/
│   │   ├── clean_data.py
│   │   └── merge_datasets.py
│   │
│   └── analysis/
│       ├── visualizations.ipynb
        ├── eda_analysis.py
│       └── network_analysis.py
│
├── docs/
│   ├── project_checkin_1_report.pdf
│   └── project_checkin_2_report.pdf
    └── any_additional_info.md
│
└── README.md
```

**Optional** (useful if there is a lot going on and the tree is not self-explanatory): 
provide a short explanation of each main folder.

Example:

- `data/` – raw and processed datasets  
- `scripts/` – scripts used for scraping, cleaning, and analysis  
- `notebooks/` – exploratory data analysis  
- `docs/` – project documentation, including reports from check-ins and slides  

---

# Libraries

Provide a **bullet list or a table of all libraries used in the project with their version numbers**.

Example (bullet list):

- pandas 2.2.0
- numpy 1.26.4
- matplotlib 3.8.2
- scikit-learn 1.4.1

Example (table):

| Library | Version |
|--------|--------|
| pandas | 2.2.0 |
| numpy | 1.26.4 |
| matplotlib | 3.8.2 |
| scikit-learn | 1.4.1 |

---

# Contributions

List the contribution of each team member (full name and tasks) as a list.
Should be specific (which data collected, which script, etc.)
Remember each script should have author, what it does, and AI disclosure.

---

# AI Usage Statement

List which (list them) and how (for each tool, explain) AI tools were used.
This is your work, and you are responsible for the accuracy and truthfulness of what you report.


---

# Project Links

Upload the following materials to the repo (or host them elsewhere if too large).
Include links to them below:

- **Slides used in the in-class presentation**
- **Updated final slides (full version)** 
- **Presentation video** (link only in the repo)
