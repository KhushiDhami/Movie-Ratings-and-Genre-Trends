# Project Report: Movie Ratings and Genre Trends

### Project Details
* **Project Title:** Movie Ratings and Genre Trends
* **Project ID:** DA-012
* **Project Domain:** Entertainment & Media Analytics
* **Current Status:** Completed (Analysis, Visualizations & Insights Finalized)

---

## Project Description
This project looks at cinematic data to help media analysts and streaming platforms make smart choices. It focuses on three main areas:

* **Genre Popularity vs. Critical Acclaim:** Analyze the contrast between high-grossing commercial blockbusters (e.g., Action, Sci-Fi) and highly-rated critically acclaimed films (e.g., Drama, Documentaries).
* **Impact of Runtime on Ratings:** Evaluate whether movie duration influences viewer retention, engagement, and audience rating scores.
* **Rating & Genre Trends Over Time:** Track how movie ratings and release volumes have changed across release years and decades.

---

## Methodology & System Architecture

### 1. Step-by-Step Project Approach
To ensure our findings are reliable and reproducible, our team followed a practical 5-step pipeline:

```
[Raw Cinematic Data (IMDb / TMDB)] 
                 │
                 ▼
[Step 1: SQL Extraction & Ingestion] ─> Filter records by release year (1985–2024), join tables
                 │
                 ▼
[Step 2: Data Cleaning & Imputation] ─> Remove 50 duplicate titles, fill missing ratings/runtimes via genre medians
                 │
                 ▼
[Step 3: Metric Computation] ─────────> Calculate Box Office turnover, average ratings, runtime buckets
                 │
                 ▼
[Step 4: Visual Analytics] ───────────> Generate yearly trend lines, scatter bubble plots, horizontal bar charts
                 │
                 ▼
[Step 5: Streaming Insights] ─────────> Formulate catalog acquisition mix and runtime sweet spot guidelines
```

1. **Data Collection & Ingestion:** We extract cinematic metadata from relational databases using SQL queries and load records into Python using Pandas dataframes.
2. **Data Cleaning & Validation:** Raw records often contain duplicate entries from multi-database joins or missing values. We validate every column, remove duplicates, and impute missing ratings and runtimes using genre medians.
3. **Exploratory Data Analysis (EDA):** We group movies by genre, release year, and duration buckets to uncover patterns that are hidden in raw tables.
4. **Data Visualization:** We convert numbers into clean, intuitive visual charts (bubble plots, bar charts, trend lines, heatmaps) so streaming executives and media analysts can understand them immediately.
5. **Actionable Recommendations:** We conclude with clear suggestions, such as which runtime bracket maximizes viewer appreciation and how streaming catalogs should balance blockbusters with critically acclaimed dramas.

---

## Technology Used

| Technology / Tool | Type | Description |
| :--- | :--- | :--- |
| **SQL** | Database Query Language | Used for querying large relational datasets (IMDb/TMDB), joining tables, filtering records by release year, and aggregating ratings metrics efficiently. |
| **Python** | Programming Language | The core programming language that powers the entire data pipeline and handles code execution. |
| **Jupyter Notebook** | Interactive Environment | Primary interactive environment used for step-by-step data exploration, code documentation, and rapid prototyping. |
| **Google Colab** | Cloud Notebook Environment | A hosted Jupyter notebook service provided by Google that runs entirely in the cloud with free access to computing resources. |
| **Pandas** | Python Library | Used for loading, cleaning, and manipulating tabular movie data (similar to Excel spreadsheets). |
| **NumPy** | Python Library | Handles large numerical arrays and performs fast statistical computations behind the scenes. |
| **Matplotlib** | Visualization Library | Used to generate clean, high-resolution charts, graphs, and visual reports. |
| **Seaborn** | Visualization Library | Built on top of Matplotlib, used for aesthetic statistical visualizations, distributions, and heatmaps. |
| **CSV** | File Format | The raw data format used to store tabular text records before analysis. |

---

## Implementation & Repository Structure

### Repository Structure
```
Movie-Ratings-and-Genre-Trends/
│
├── data.csv                 
├── analysis.ipynb      
├── report.pdf
├── readme.md                       
└── requirment.txt            
```

### Execution & Data Processing Summary

| Pipeline Stage | Implementation Details | Status |
|---|---|---|
| **Data Ingestion** | Loaded 1,550 cinematic records from `data.csv` using Pandas. | **Completed** |
| **Data Cleaning** | Dropped 50 duplicate rows; imputed 45 missing ratings and 31 missing runtimes using genre median values. | **Completed** |
| **Field Engineering** | Added `Runtime_Bucket` duration categories (`<90 min`, `90-110 min`, `110-130 min`, `130-150 min`, `>150 min`). | **Completed** |
| **Core Visualizations** | Generated 6 essential charts: Yearly Trends, Acclaim vs Popularity, Genre Revenue, Runtime Impact, Catalog Share, Performance Heatmap. | **Completed** |

### Summary of Calculated Movie Metrics
* **Total Movies Analyzed:** 1,500 completed titles
* **Average Viewer Rating:** 6.96 / 10
* **Average Movie Duration:** 119.1 minutes
* **Total Tracked Box Office:** $347,824.67 Million ($347.82 Billion)
* **Average Box Office per Movie:** $231.88 Million
* **Total Audience Votes:** 695,089,068 votes
* **Highest Rated Genre:** Drama (7.73 / 10) & Documentary (7.72 / 10)
* **Highest Grossing Genre:** Action ($120.22 Billion) & Sci-Fi ($75.01 Billion)

---

## Key Findings & Business Recommendations

### 1. Key Analytical Findings
* **Genre Popularity vs. Critical Acclaim:** **Action** ($120.2B total, $541.5M avg) and **Sci-Fi** ($75.0B total, $528.2M avg) lead commercial box office and audience votes by a wide margin. In contrast, **Drama** (7.73 / 10), **Documentary** (7.72 / 10), and **Animation** (7.47 / 10) command the highest critical ratings despite lower box office budgets.
* **Impact of Runtime on Ratings:** Movies running between **110 and 130 minutes** hit the critical rating "sweet spot" with an average score of **7.16 / 10** across 496 films. Films under 90 minutes recorded the lowest average rating (**6.50 / 10**), showing that audience satisfaction rises when stories have sufficient time for character development.
* **Revenue Concentration:** Action, Sci-Fi, and Adventure together generate over **66%** of all tracked commercial revenue, proving that visual spectacle drives theatrical and commercial ticket sales.

### 2. Practical Business Recommendations
1. **Maintain a Balanced Catalog Mix (Acquisition vs. Retention):** Streaming platforms like Netflix, Prime Video, and Disney+ should use high-octane Action and Sci-Fi blockbusters to acquire new subscribers, while acquiring highly-rated Dramas and Documentaries to keep subscribers engaged over the long term.
2. **Target the Optimal Runtime Window (110–130 Minutes):** Content creators and streaming original productions should aim for the 110–130 minute window. Pacing a story under 90 minutes often leaves viewers feeling rushed, resulting in lower reviews.
3. **Invest in High-ROI Animation and Horror:** Animation earns strong commercial returns ($380.3M avg) with high critical approval (7.47 / 10). Horror offers unbeatable return on investment with modest budgets and passionate fanbases.

### 3. Project Conclusion
All project objectives for **DA-012** have been completed. Raw cinematic records were cleaned, key entertainment industry benchmarks were calculated, and the six essential visual charts were generated. The findings provide clear, practical guidance for streaming content acquisition, studio greenlighting, and film programming.

---

## Project Links

| Type | Link |
| :--- | :--- |
| **GitHub Repository** | [GitHub Repo](https://github.com/KhushiDhami/Movie-Ratings-and-Genre-Trends) |
| **Jupyter Notebook** | [analysis.ipynb](analysis.ipynb) |
| **Raw Dataset** | [data.csv](data.csv) |
| **Colab Notebook Link** | [Analysis Notebook](https://colab.research.google.com/drive/12BqXfVyb0z7fRTk13lmIBgGxwu7fU9jD?usp=sharing) |

---

## References 

| Technology | Reference |
| :--- | :--- |
| **SQL** | [W3Schools SQL Tutorial / PostgreSQL Docs](https://www.postgresql.org/docs/) |
| **Python** | [Python Official Documentation](https://docs.python.org/) |
| **Jupyter Notebook** | [Jupyter Documentation](https://docs.jupyter.org/) |
| **Google Colab** | [Google Colab Portal](https://developers.google.com/colab) |
| **Pandas** | [Pandas PyPI / Documentation](https://pypi.org/project/pandas/) |
| **NumPy** | [NumPy Documentation](https://numpy.org/doc/stable/) |
| **Matplotlib** | [Matplotlib Documentation](https://matplotlib.org/stable/index.html) |
| **Seaborn** | [Seaborn Documentation](https://seaborn.pydata.org/) |
| **IMDb / TMDB Datasets** | [IMDb Non-Commercial Datasets](https://developer.imdb.com/non-commercial-datasets/) |

---

## Project Members

| Name | ID |
| --- | --- |
| **ADITYA KUMAR** | BCAI2026238 |
| **VAISHNAVI SINGH** | BCAI2026243 |
| **DARSHIT RASTOGI** | BCAI2026249 |
| **KANIKA BISHT** | BCCC2026001 |
| **AMANDEEP** | BCCC2026003 |
| **KAVYA PATHAK** | BCCC2026004 |
| **ANJALI MOURYA** | BCCC2026005 |
| **ANJALI SHARMA** | BCCC2026006 |
| **SURAJ SINGH TOMAR** | BCCC2026007 |
| **KHUSHI DHAMI [Team Leader]** | BCCC2026010 |
