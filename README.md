# Predictive Modeling, Explainable AI, and Phenotypic Discovery for Long-Term Glycemic Control in New-Onset Diabetes

This repository contains the complete Jupyter Notebook for a comprehensive machine learning research project analyzing long-term glycemic control in patients with new-onset diabetes mellitus. The project demonstrates an end-to-end data science workflow, from initial data exploration to advanced predictive modeling, model interpretation, and unsupervised clinical discovery.

## Project Overview

Achieving long-term glycemic control is the cornerstone of diabetes management, but early identification of patients at high risk for future poor control remains a clinical challenge. This project leverages a large, real-world dataset of over 77,000 patients to build, interpret, and learn from machine learning models designed to tackle this problem. The analysis progresses through three distinct phases to provide a multi-layered, data-driven understanding of glycemic control.

## Research Questions

This project seeks to answer three primary questions:
1.  **Prediction:** Can we accurately predict a patient's 3-year glycemic control status using only data available within their first year of diagnosis?
2.  **Explanation:** What are the key clinical drivers behind the predictions of our best-performing model?
3.  **Discovery:** Can we identify novel, data-driven phenotypes of new-onset diabetes that exhibit different long-term prognoses?

## Methodology

The project is structured into a comprehensive three-phase analysis:

1.  **Phase 1: High-Performance Predictive Modeling**
    -   A suite of models (Logistic Regression, Random Forest, XGBoost, and a Neural Network) are systematically trained and evaluated.
    -   The Neural Network is selected as the champion model based on its superior performance on a held-out validation set.
    -   The champion model's final performance is confirmed on an unseen test set.

2.  **Phase 2: Explainable AI (XAI)**
    -   The state-of-the-art **SHAP (SHapley Additive exPlanations)** framework is used to interpret the "black box" Neural Network.
    -   **Global explanations** identify the most important predictive features across the entire patient population.
    -   **Local explanations** provide detailed "case studies" showing the specific factors contributing to the risk score for individual patients.

3.  **Phase 3: Phenotypic Discovery**
    -   Unsupervised learning techniques (**UMAP** for dimensionality reduction and **HDBSCAN** for clustering) are applied to the data.
    -   This data-driven approach identifies distinct patient subgroups (phenotypes) without any prior assumptions.
    -   The discovered phenotypes are then profiled and analyzed to understand their clinical characteristics and long-term outcomes.

## Key Findings

-   A Neural Network model was successfully developed to predict 3-year glycemic control with a high degree of accuracy (**AUROC of 0.892** on the test set).
-   Explainable AI revealed that the most critical predictors were **baseline HbA1c**, the **glycemic trajectory in the first year (`Hba1c_change`)**, and the **intensity of required medication** (a proxy for disease severity).
-   Unsupervised clustering discovered **22 distinct clinical phenotypes** of new-onset diabetes. These data-driven groups were shown to be highly statistically significant and demonstrated a dramatic risk gradient, with the rate of poor control ranging from **42%** in the lowest-risk group to **92%** in the highest-risk group.

## Technologies & Libraries

This project is implemented in Python 3 and leverages the following core data science libraries:
-   **Data Manipulation:** `pandas`, `numpy`
-   **Visualization:** `matplotlib`, `seaborn`
-   **Machine Learning:** `scikit-learn`
-   **Gradient Boosting:** `xgboost`
-   **Deep Learning:** `tensorflow`
-   **Explainable AI:** `shap`
-   **Unsupervised Learning:** `umap-learn`, `hdbscan`

All code is designed to be run in a standard environment like Google Colab or a local Jupyter instance.

## Running the Notebook

1.  **Environment:** It is recommended to use Google Colab for a seamless experience, as it has most dependencies pre-installed.
2.  **Dependencies:** The notebook includes cells to install the necessary libraries (`!pip install ...`). Simply run these cells if the libraries are not already in your environment.
3.  **Execution:** The notebook is structured to be run sequentially from top to bottom. Each section builds upon the results of the previous one.

## Dataset

The analysis uses a public dataset of 77,724 patients with newly diagnosed diabetes mellitus from Istanbul, Turkey. The data was compiled from the national electronic health record system, e-Nabız.

-   **Source:** Mendeley Data
-   **DOI:** [10.17632/rr4rzzrjfc.2](https://doi.org/10.17632/rr4rzzrjfc.2)

## Citation

If you use this work, please cite the original dataset providers:

> Gulkesen, Kemal Hakan; Ülgü, Mustafa Mahir; Mutlu, Begum; Akünal, Abdullah; Ayvalı, Mustafa Okan; Akyürek, Özen; Birinci, Şuayip; Balcı, Mustafa Kemal; Sezer, Ebru (2024), “Machine Learning for Prediction of Glycemic Control in Diabetes Mellitus”, Mendeley Data, V2, doi: 10.17632/rr4rzzrjfc.2
