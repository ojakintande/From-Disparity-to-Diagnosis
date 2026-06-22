# Diagnostic Fairness: Auditing Bias Origins via Group-Level Influence Functions

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Research Prototype](https://img.shields.io/badge/Status-Active%20Research-blue)](https://github.com/ojakintande/LLM_Who_Audit_Reviewers)

This repository provides the implementation of a novel diagnostic framework that bridges the gap between outcome-based fairness auditing and training-data-centric interpretability. By utilizing **group-level influence functions**, we move beyond documenting bias to diagnosing its origins.

---

## 1. Abstract
Algorithmic fairness interventions often focus on quantifying aggregate outcome disparities, yet they lack explanatory power regarding how these disparities emerge during model training. This work introduces a diagnostic framework that decomposes total model influence into two novel components:

*   **Self-Influence (Intra-group):** The impact of group-specific data on the group’s own predictions.
*   **Between-Influence (Inter-group):** The impact of disparate groups on one another.

This decomposition enables practitioners to move beyond treating symptoms to addressing the root causes of bias in high-stakes predictive systems.

## 2. Key Contributions
*   **Identification of Failure Modes:** We formally identify **Stereotyping** (driven by excessive inter-group influence) and **Under-learning** (caused by insufficient self-influence).
*   **Theoretical Grounding:** We establish a rigorous link between influence components and violations of standard group fairness criteria.
*   **End-to-End Diagnostic Pipeline:** A modular framework to audit model origins, followed by targeted data reweighting and SHAP-based residual bias explanation.
*   **Empirical Case Study:** We validate our approach using the **COMPAS recidivism dataset**, challenging conventional paradigms that rely solely on inter-group debiasing.

## 3. Repository Structure
*   `/scripts`: R scripts for influence function decomposition and SHAP-based residual analysis.
*   `/data`: Anonymized experimental logs and processed datasets.
*   `/results`: Aggregated performance metrics and visualization outputs.

## 4. Quick Start
To replicate the diagnostic framework:

1.  **Environment:** Ensure R (v4.x) is installed.
2.  **Dependencies:** Install the required ecosystem:
    ```r
    install.packages(c("tidyverse", "SHAPforxgboost", "influenceR"))
    ```
3.  **Setup:** Define your data paths within `config.R`.
4.  **Audit:** Run the primary diagnostic pipeline:
    ```r
    source("scripts/audit_pipeline.R")
    ```

## 5. Citation
If this framework contributes to your research, please cite our work:

## 6. License
This project is licensed under the **MIT License**. See the `LICENSE` file for more details.
