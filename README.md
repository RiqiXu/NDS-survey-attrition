# Modelling Survey Attrition in the 2023 National Dog Survey

This repository contains the analysis code, page-level metadata and aggregated outputs supporting an MSc Data Science dissertation at University College London.

The study conducted a secondary observational analysis of respondent-level data from the 2023 National Dog Survey, administered by Dogs Trust. It examined where survey breakoff occurred, how conditional breakoff risk varied across questionnaire routes, and which observable page characteristics were associated with respondents leaving the survey.

## Research questions

1. How does conditional breakoff risk vary across questionnaire progression and between the principal survey routes?
2. Which observable page characteristics are associated with conditional breakoff risk after accounting for progression and route?
3. Which questionnaire nodes produce more breakoff than expected after adjustment for the measured characteristics?

## Analytical overview

The original Qualtrics fields were consolidated into 141 page-level analytical nodes. Route-aware respondent trajectories were then reconstructed while distinguishing recorded exposure, structural missingness and terminal breakoff.

The analysis included:

* 369,071 survey records;
* 27,274 pre-survey bounces;
* 341,797 respondents with an identifiable questionnaire trajectory;
* 10,770,157 respondent-node exposures; and
* 95,034 locatable question-level breakoffs.

The principal methods included empirical hazard and survival analysis, grouped quasibinomial discrete-time hazard regression, route-specific sensitivity analysis and observed-versus-predicted residual diagnostics.

## Repository structure

* `Analysis Code/` — R Markdown analysis code and rendered analysis output.
* `metadata/` — field-to-node reconstruction information and coded page-level characteristics.
* `Outputs/` — aggregated tables, figures, model summaries and diagnostic outputs.
* `Reference/` — supporting materials used to interpret the questionnaire structure and coding.
* `README.md` — repository documentation.

## Main findings

Breakoff was concentrated at particular stages rather than increasing steadily with questionnaire length. The shorter non-owner route experienced greater attrition than the dog-owner route.

Long choice sets showed the most consistent positive association with breakoff across routes. Associations involving text entry, financial sensitivity, privacy and prompt length were more dependent on route and question context.

Residual diagnostics identified several individual questions where observed breakoff substantially exceeded model predictions, highlighting potential priorities for future questionnaire review.

These findings are observational and should not be interpreted as establishing that any page characteristic caused respondents to leave.

## Data availability

The original respondent-level National Dog Survey data are not included in this repository and are not available through this project because of data-sharing and confidentiality restrictions.

The repository contains analysis code, page-level metadata and aggregated outputs only. No raw respondent records or personally identifiable information are provided.

Consequently, the complete analysis cannot be reproduced without authorised access to the original dataset. Authorised users would need to supply the data locally and update the relevant input path in the R Markdown file.

## Dissertation and presentation

The dissertation manuscript and presentation slides are not included in this repository. This repository is intended to document the analytical workflow and provide the associated non-data outputs.

## Software

The analysis was conducted in R. Required packages are loaded within the R Markdown analysis file.

## Author

Riqi Xu
MSc Data Science
University College London
