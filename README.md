# Robust CCA: Social Media & Self-Esteem

> Outlier-resistant canonical correlation on survey data linking social media use and self-esteem.

## Overview

- Multivariate Statistics final project with two teammates: measure how social media engagement relates to self-esteem using real survey data.

## Data / Scope

- Survey of 24 Likert-scale items in Social Media and Self-Esteem blocks, with straight-lining and non-normal responses to handle.

## Workflow

- Checked item validity, reliability and roughly linear relationships between dimensions.
- Applied CCA with the Minimum Covariance Determinant estimator to down-weight outliers.
- Used bootstrap re-sampling for confidence ranges and compared 8 alternative CCA methods.

## Results

- Robust CCA gave more stable, outlier-resistant estimates than classical CCA.
- It held up best across the 8-method comparison.
- Covers a full multivariate study, explained in plain language.

## Tech Stack

Canonical Correlation, MCD estimator, Bootstrap, Reliability testing

## Repository Structure

```
code/               Code documentation (data cleaning and exploration; assumption checking and modelling)
data/               Anonymous Likert-scale questionnaire responses (items x1-x24)
report/             Final report (PDF)
```

## How to Run

The code is documented in Word files (`code/`) as exported from the analysis environment. Copy the code blocks into an R script or notebook, load `data/questionnaire_responses.csv`, and run cleaning first, then assumption checking and modelling.

## Team

Multivariate Statistics course project (team project).

## Notes

- Questionnaire data contains only anonymous numeric answers.
- Plagiarism-check results are intentionally not included.
- TODO: export the code from the Word files into runnable `.R` scripts.

## Author

Nadya Angelie Lislie, BINUS University (Computer Science and Statistics). [LinkedIn](https://www.linkedin.com/in/nadya-angelie-lislie/) | [GitHub](https://github.com/Nadya-AngelieLislie)

## Continuous Integration

GitHub Actions (`.github/workflows/ci.yml`) runs `ruff` and `pytest` repository-health checks on every push; run them locally with `make lint test`.
