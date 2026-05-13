# BCCDC STBBI & TB Surveillance Dashboard

> **Note:** In compliance with BC public health data governance and privacy protection requirements under the *Freedom of Information and Protection of Privacy Act (FIPPA)*, source code and underlying data for this project cannot be publicly shared. This README documents the architecture, methodology, and analytical contributions to demonstrate technical scope and reproducible practices.

**Live Dashboard:** [https://bccdc.shinyapps.io/stbbi_tb_surveillance_report/](https://bccdc.shinyapps.io/stbbi_tb_surveillance_report/)  
**Organization:** BC Centre for Disease Control (BCCDC) — Communicable Disease Prevention and Control  
**Role:** Data Analyst  
**Stack:** R · R Shiny · tidyverse · ggplot2 · plotly · SQL

<img width="1469" height="830" alt="Screenshot 2026-05-12 at 7 57 41 PM" src="https://github.com/user-attachments/assets/03cb170e-5228-495e-a352-0edef5014734" />

---



## Overview

This project is an interactive, publicly accessible surveillance dashboard reporting on **Sexually Transmitted and Blood-Borne Infections (STBBI)** and **Tuberculosis (TB)** across British Columbia. It serves as the primary digital surveillance report for BCCDC, replacing static PDF reports with a dynamic, continuously updated platform.

The dashboard is cited in peer-reviewed publications, BC provincial health authority reports, and federal surveillance documents (Public Health Agency of Canada). It supports epidemiologists, clinicians, public health units, and policymakers across BC in monitoring disease trends and informing intervention planning.

---


## My Contributions

### 1. Integrated Data Pipeline Maintenance

- Maintained and updated the end-to-end ETL pipeline ingesting data from multiple source systems including BCCDC Public Health Laboratory (PHL), STI case reporting systems, and TB case management databases
- Implemented data validation routines to flag inconsistencies in demographics reporting across heterogeneous source systems — a known methodological challenge documented within the dashboard's data notes
- Managed periodic data refreshes to ensure the dashboard reflected the most current surveillance data for each reporting cycle
- Applied standardized case definitions per BCCDC surveillance protocols

### 2. Metric Development & Epidemiological Tracking

- Developed and maintained indicators across six STBBI/TB disease areas, translating clinical case definitions and testing episode rules into reproducible analytical code
- Built stratified analyses by **health authority**, **age group**, **sex/gender**, **geographic region**

### 3. R Shiny Application Development

- Built and maintained the full Shiny application, including UI layout, reactive server logic, and modular component architecture for scalability across disease areas
- Implemented interactive visualizations using **ggplot2** and **plotly** with drill-down capability by region, time period, and demographic group
- Transitioned reporting from static annual PDF formats to a dynamic, web-hosted dashboard — improving accessibility and enabling self-serve data exploration for public health practitioners
- Deployed and maintained the application via **shinyapps.io**, managing performance, session stability, and update cycles

### 4. Reporting Design & Stakeholder Communication

- Collaborated with epidemiologists and program leads to translate surveillance requirements into dashboard features
- Supported alignment of the dashboard's content with BCCDC's annual TB Report and other surveillance publications

---

## Technical Architecture

```
Data Sources
    ├── BCCDC Public Health Laboratory (HIV, HCV, Syphilis testing)
    ├── STI Case Reporting Systems (Gonorrhea, Chlamydia, Syphilis cases)
    ├── TB Case Management Database (Active TB, TBI treatment)
    └── BC Stats / PHAC (Population denominators, national benchmarks)
          │
          ▼
ETL & Data Processing (R / SQL)
    ├── Data ingestion & validation
    ├── Case definition application
    ├── Stratification & aggregation
    └── Suppression of small counts (privacy protection)
          │
          ▼
R Shiny Application
    ├── Reactive data layer (server.R)
    ├── Modular UI components (ui.R / modules)
    ├── ggplot2 static visualizations
    ├── plotly interactive charts
    └── Methodology & data notes documentation
          │
          ▼
Deployment
    └── shinyapps.io (public-facing, BCCDC-managed)
```


---


## Related Publications & Citations

This dashboard is cited in and supports the following BCCDC publications:

- BC Centre for Disease Control. *BC TB Annual Report 2024.* BCCDC, 2025.
    — *Contributing analyst. Named in acknowledgements/authorship.*
  [View Report (PDF)](https://www.bccdc.ca/resource-gallery/Documents/Statistics%20and%20Research/Statistics%20and%20Reports/TB/BCCDC_TB_Annual_Report_2025.pdf)
- BC Centre for Disease Control. *HIV Incidence and Prevalence Estimates for British Columbia, 2022.* BCCDC, 2025.
- Durigon et al. "Syphilis: Overview for BC health care providers." *BC Medical Journal,* 2024.
- BC Medical Journal. "Syphilis: Shifting trends in BC and new tools for clinical practice." 2026.

---

## Skills Demonstrated

`R` `R Shiny` `ggplot2` `plotly` `tidyverse` `SQL` `ETL pipeline design` `epidemiological surveillance` `KPI development` `data validation` `public health informatics` `shinyapps.io deployment` `data governance` `FIPPA compliance` `communicable disease reporting` `interactive data visualization` `multi-source data integration`

---

## Contact

For questions about this project's methodology or my analytical contributions, feel free to reach out via [LinkedIn](www.linkedin.com/in/sven-dong-67b6b31a7) or open a discussion in this repository.

---

*This repository contains no patient-level or restricted data. All referenced indicators are publicly reported through the live dashboard linked above.*
