## Diagnostic Fairness: Auditing Bias Origins via Group-Level Influence Functions

This repository contains the implementation, diagnostic framework, and experimental results for the paper: "Algorithmic fairness interventions often focus on quantifying and mitigating aggregate outcome disparities, yet they lack explanatory power for how these disparities arise..."

## 1. Abstract
Algorithmic fairness interventions often focus on quantifying and mitigating aggregate outcome disparities, yet they lack explanatory power for how these disparities arise during model training. This work bridges the gap between outcome-based fairness auditing and training-data-centric interpretability by introducing a diagnostic framework grounded in group-level influence functions.

We decompose total influence into two novel components:

Self-Influence (Intra-group): Assessing the impact of group-specific data on the group’s own predictions.

Between-Influence (Inter-group): Assessing the impact of disparate groups on one another.

## 2. Key Contributions
Novel Failure Modes: Identification of stereotyping (driven by inter-group influence) and under-learning (caused by insufficient self-influence).

Theoretical Linkage: Linking influence components to violations of standard group fairness criteria.

Diagnostic Pipeline: An end-to-end audit framework that moves beyond documenting what disparities exist to diagnosing how they emerge.

Empirical Validation: Case study on the COMPAS recidivism dataset, challenging conventional inter-group debiasing paradigms.

## 3. Repository Structure
/scripts: R implementation of the influence function decomposition and SHAP-based residual bias analysis.

/data: Pre-processed datasets (e.g., COMPAS) and experimental logs.

/results: Aggregated metrics and visualization outputs.

## 4. Quick Start
To replicate the diagnostic framework:

Dependencies: Ensure R is installed with tidyverse, SHAPforxgboost, and influenceR (or your relevant libraries).

Configuration: Set the data path in config.R.

Run Pipeline: Execute the primary audit script:

source("scripts/audit_pipeline.R")


## 5. Citation
If you find this research useful for your auditing work, please cite:
> [Awaiting DOI/Publication info]

## 6. License
This project is licensed under the MIT License.

