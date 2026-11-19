# finalproject

## Public Health Data Analysis: BMI Patterns and Homicide Mortality in the United States

This repository contains the final project for **BST260 (Fall 2026)** at the Harvard T.H. Chan School of Public Health.

The project investigates two public health research questions using publicly available datasets from the National Health and Nutrition Examination Survey (NHANES) and the Centers for Disease Control and Prevention (CDC).

The project consists of two independent analyses focusing on individual-level health characteristics and state-level mortality patterns. Each analysis will be documented in a Quarto vignette and presented through a website generated using the `pkgdown` R package.

## Project Objectives

The main objectives of this project are:

- Investigate the association between age and body mass index (BMI) among U.S. adults.
- Examine whether the relationship between age and BMI differs by sex.
- Explore geographic and temporal patterns in homicide mortality rates across U.S. states.
- Apply descriptive statistics, data visualization, and statistical modeling to investigate public health questions.
- Assess data quality, missing values, potential confounding, and limitations of observational data.
- Develop reproducible analyses using R and communicate findings through a publicly accessible website.

## Datasets

### 1. National Health and Nutrition Examination Survey (NHANES)

The NHANES dataset contains demographic, anthropometric, and health-related measurements collected from participants in the United States.

**Research Question:**

How is age associated with BMI among U.S. adults, and does this association differ by sex?

**Variables of Interest:**

- Exposure: Age (years)
- Outcome: Body Mass Index (BMI, kg/m²)
- Covariates: Sex and race/ethnicity

**Planned Analysis:**

- Examine distributions of age and BMI.
- Calculate descriptive statistics across demographic groups.
- Visualize the relationship between age and BMI.
- Fit regression models to investigate associations between age and BMI.
- Examine potential differences in age-related BMI patterns between males and females.

### 2. CDC Homicide Mortality Dataset

The CDC homicide mortality dataset (`cdcmurd`) contains state-level homicide mortality information across multiple years.

The dataset is included in the `finalproject` R package.

**Research Question:**

How have homicide mortality rates changed over time across U.S. states?

**Variables of Interest:**

- Exposure: Calendar year
- Outcome: State-level homicide mortality rate
- Geographic variable: U.S. state

**Planned Analysis:**

- Summarize homicide mortality rates across states and years.
- Identify geographic differences in homicide mortality.
- Visualize temporal trends using line plots.
- Compare homicide mortality patterns across states and regions.
- Explore statistical models for evaluating temporal changes in mortality rates.

## Methods

All analyses will be conducted using R.

The analytical workflow will include:

1. Data loading and documentation of data provenance.
2. Data cleaning and assessment of missing values.
3. Exploratory data analysis and descriptive statistics.
4. Data visualization using appropriate graphical methods.
5. Statistical modeling to investigate the research questions.
6. Interpretation of findings, potential confounding, and study limitations.

Two Quarto vignettes will document the analyses separately:

- **Vignette 1:** Association Between Age and BMI Among U.S. Adults
- **Vignette 2:** Geographic and Temporal Patterns of Homicide Mortality in the United States

Each vignette will include its research objectives, dataset description, methods, results, and limitations.

## Expected Outcomes

The project aims to provide a better understanding of age-related BMI patterns among U.S. adults and geographic and temporal differences in homicide mortality across U.S. states.

The analyses will demonstrate the application of statistical programming, exploratory data analysis, regression modeling, and data visualization to public health research.

Because both datasets are observational, the findings will be interpreted as associations rather than causal relationships.

## Project Website

The final project will be developed as an R package and published using `pkgdown` and GitHub Pages.

**GitHub Repository:** https://github.com/tongtong24x/finalproject

**Project Website:** https://tongtong24x.github.io/finalproject/

## Author

Tongtong Gu

Harvard T.H. Chan School of Public Health

BST260 — Fall 2026

## References

- [BST260 Project Instructions](https://vjcitn.github.io/bst260project-template/articles/instructions.html)
- [BST260 Project Suggestions](https://vjcitn.github.io/bst260project-template/articles/stubs.html)
- [National Health and Nutrition Examination Survey (NHANES) — CDC](https://www.cdc.gov/nchs/nhanes/)
- [CDC Homicide Mortality Statistics](https://www.cdc.gov/nchs/state-stats/deaths/homicide.html)
