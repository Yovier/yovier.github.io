# Healthcare Data Quality & Analytics

## Project Overview

This project analyzes 100,000 healthcare encounter records to assess data quality, explore clinical outcomes, and investigate 30-day readmission patterns.

The project is part of an end-to-end healthcare analytics workflow that combines SQL-based data preparation, a PostgreSQL data warehouse, Python exploratory analysis, and Power BI dashboards.

## Business Objectives

- Assess the completeness and consistency of healthcare encounter data.
- Identify potential data-quality and financial anomalies.
- Analyze clinical outcome distributions.
- Calculate and compare 30-day readmission rates by insurance type.
- Translate data findings into actionable recommendations for further investigation.

## Tools & Technologies

- **SQL** — Data querying and validation
- **PostgreSQL / Supabase** — Relational database and dimensional data warehouse
- **Python** — Exploratory data analysis and data-quality checks
- **Pandas and NumPy** — Data manipulation and analysis
- **Matplotlib** — Data visualization
- **Power BI and DAX** — Interactive dashboards and business metrics

## Key Data Quality Findings

The initial dataset contains 100,000 records and 15 columns.

The Python analysis identified:

- 0 duplicate encounter IDs
- 250 missing provider assignments
- 15 missing encounter dates
- 900 missing patient satisfaction scores
- 40 records with negative total costs requiring financial validation

Records with identified issues were retained for investigation rather than automatically removed.

## Preliminary Analytical Findings

### Clinical Outcomes

- Improved: 72.12%
- Stable: 21.78%
- Worsened: 6.09%

### Thirty-Day Readmissions

The overall 30-day readmission rate was 11.72%.

By insurance type, Self-Pay had the highest observed rate at 12.08%, while Medicare had the lowest at 11.62%.

These comparisons are descriptive and do not establish causation.

## Data Quality and Limitations

Missing values and negative cost entries require further investigation. The cause of the negative costs cannot be established from the available fields alone.

Readmission comparisons may also be influenced by patient characteristics, diagnoses, and other factors that have not been controlled for in this exploratory analysis.

## Project Workflow

1. Query and validate healthcare data using SQL.
2. Store and organize data in a PostgreSQL dimensional warehouse.
3. Perform data-quality checks and exploratory analysis in Python.
4. Visualize key findings using Matplotlib.
5. Present operational and clinical metrics in Power BI dashboards.

## Project Status

The initial Python exploratory analysis and data-quality review are complete. Further work can extend the investigation of financial anomalies and readmissions, and connect these findings to the Power BI reporting layer.

## Python Notebook

Explore the complete Python analysis, including data quality validation, exploratory analysis, clinical outcome metrics, readmission analysis, and visualizations.

**[View the Python Data Quality Analysis Notebook](./06_Healthcare_Data_Quality_Analysis.ipynb)**

## Power BI Dashboards

The Power BI report includes two interactive report pages designed to analyze healthcare performance, clinical outcomes, and operational indicators.

### 1. Executive Healthcare Overview

Provides a high-level overview of healthcare encounters, patient volume, total costs, average cost per encounter, and length of stay. Visualizations explore clinical outcome distribution, encounters by insurance type and region, and cost patterns by diagnosis.

### 2. Clinical & Operational Analysis

Examines 30-day readmission rates by insurance type, region, and diagnosis. Additional visualizations explore patient satisfaction by clinical outcome, average length of stay by region, and total healthcare costs by region.

### Power BI Report

[Download the Power BI Report (.pbix)](./Health_Analytics_BI_Portfolio.pbix)

**Tools:** Power BI Desktop, DAX, PostgreSQL, and Supabase.
