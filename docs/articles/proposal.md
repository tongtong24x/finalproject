# BST260 Final Project Proposal

**To:** BST260 Teaching Team, Fall 2026  
**From:** Tongtong Gu  
**Subject:** Proposal for Two Public Health Data Analyses

## Project Overview

For my BST260 final project, I propose to develop an R package named
`finalproject` and a public website using `pkgdown`. The project will
include two reproducible Quarto vignettes that investigate distinct
public health questions using datasets introduced in class. The first
vignette will analyze the relationship between age and body mass index
(BMI) among U.S. adults using NHANES. The second will examine temporal
and geographic variation in homicide mortality rates using CDC data.
Both analyses will emphasize data provenance, descriptive statistics,
visualization, statistical modeling, and transparent discussion of
limitations.

## Vignette 1: Age and Body Mass Index Among U.S. Adults

**Research question:** How is age associated with BMI among U.S. adults,
and does this association differ by sex?

**Data source and provenance:** The `NHANES` dataset available through
the `NHANES` R package, based on the U.S. National Health and Nutrition
Examination Survey conducted by the National Center for Health
Statistics (NCHS), Centers for Disease Control and Prevention (CDC). I
will document the package version, source documentation, survey cycles
represented, and relevant measurement definitions in the finished
vignette.

**Population and unit of analysis:** Individual NHANES participants aged
20 years or older with eligible measurements. Each observation
represents one participant.

**Exposure:** Age in years, initially treated as a continuous variable.
I will consider flexible modeling of age if plots suggest a nonlinear
association.

**Outcome:** BMI in kg/m², treated as a continuous variable. BMI is a
descriptive anthropometric measure and is not interpreted as a direct
measurement of body fat.

**Prespecified covariates:** Sex and race/ethnicity, selected based on
their potential relationships with BMI and age distributions. Sex will
also be evaluated as an effect modifier through an age-by-sex
interaction. Missing values in the exposure, outcome, and covariates
will be tabulated; a complete-case analysis will be used initially, with
limitations of potential selection bias clearly stated.

**Planned analyses:** I will summarize participant characteristics, BMI
distributions, and missingness; produce histograms, boxplots, and
scatterplots or smoothed age–BMI curves; and fit linear regression
models with age, sex, and race/ethnicity, including an age-by-sex
interaction where appropriate. I will explore nonlinear associations if
supported by the data. I will inspect whether the available survey
design information permits design-appropriate weighted analysis;
otherwise, I will describe unweighted results as sample-level
exploratory findings, not nationally representative estimates.

**Expected limitations:** Cross-sectional data do not establish causal
effects of age. Cohort effects, selection and nonresponse, measurement
limitations, and potential confounding may affect interpretation.

## Vignette 2: Geographic and Temporal Patterns in U.S. Homicide Mortality

**Research question:** How have homicide mortality rates changed over
time across U.S. states, and how do these trends differ geographically?

**Data source and provenance:** The `cdcmurd` dataset provided in the
BST260 `finalproject` template. Its package documentation describes
homicide mortality rates by state and year for the 50 states and
Washington, D.C., and links to the CDC National Center for Health
Statistics state homicide statistics
(https://www.cdc.gov/nchs/state-stats/deaths/homicide.html). I will
verify the available years, rate definitions, units, data collection
methods, and any suppression or missing values before analysis.

**Population and unit of analysis:** State-year observations for the 50
U.S. states and Washington, D.C., within the years represented by
`cdcmurd`.

**Exposure:** Calendar year, modeled as a temporal variable. Geographic
variation will be assessed using state and, where appropriate, Census
region labels.

**Outcome:** State-level homicide mortality rate, treated as a
continuous measure after verifying the dataset’s definition and units.

**Prespecified covariates and comparisons:** State or region will be
considered to describe persistent geographic differences in rates. I
will examine whether the direction and magnitude of temporal patterns
vary by geographic area. Missing or suppressed state-year values will be
identified and reported rather than assumed to be zero.

**Planned analyses:** I will inspect the dataset structure and
completeness, summarize the distribution of rates across states and
years, visualize national and regional descriptive trends, and compare
state-specific trajectories. Subject to data coverage and variable
definitions, I will fit descriptive regression models with year and
state/region terms and consider interactions to explore geographic
differences in trends. If age adjustment or population weighting is not
supported by the available data, I will explicitly limit interpretation
accordingly.

**Expected limitations:** These are ecological observations and cannot
establish individual-level risk factors or causal effects. Trends can be
affected by coding changes, variation in population structure,
suppression, and the choice of mortality rate definition.

## Reproducibility, Deliverables, and Reporting

The repository at https://github.com/tongtong24x/finalproject will
contain a valid R package, two source Quarto vignettes, code used to
create descriptive statistics and visualizations, source citations, and
a `pkgdown` website published through GitHub Pages at
https://tongtong24x.github.io/finalproject/. I will check package
installation and site generation and document the steps needed to
reproduce the analyses.

Each vignette will include its investigative objectives, data provenance
and variable definitions, data-cleaning choices, descriptive findings,
visualizations and models, a scientific interpretation of results, and
limitations. I will write reusable R functions where they improve
consistency in data summaries and figures. The findings will be reported
only after the datasets have been examined; no results are assumed in
this proposal.

## References

- CDC/NCHS. National Health and Nutrition Examination Survey (NHANES):
  https://www.cdc.gov/nchs/nhanes/
- `NHANES` R package documentation:
  https://cran.r-project.org/package=NHANES
- CDC/NCHS. Homicide Mortality by State:
  https://www.cdc.gov/nchs/state-stats/deaths/homicide.html
- BST260 project template and dataset documentation:
  https://github.com/vjcitn/bst260project-template
