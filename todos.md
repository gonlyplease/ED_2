# Experiment Design for Data Science – WS 2024/25 Exercise 2

## Task Overview

This project involves reproducing the experimental setup, experiments, and results as presented in the paper:

**Title:** Comparing Intrinsic and Extrinsic Evaluation of Sensitivity Classification  
**Authors:** Mahmoud F. Sayed, Nishanth Mallekav, and Douglas W. Oard  
**Conference:** Advances in Information Retrieval, ECIR 2022

The goals are:
1. **Reproduce Results:** Confirm the reported results or identify inconsistencies.
2. **Evaluate Experimental Design:** Assess the sufficiency of information in the paper and test the statistical significance of the results.
3. **Document Findings:** Provide a detailed report and machine-readable experiment descriptions.

## Step-by-Step Approach

### 1. Understand the Paper and Setup
- **Read and analyze** the methodology, experimental setup, datasets, and models used.
- Identify:
  - Datasets: OHSUMED and Avocado collections.
  - Models: Logistic Regression, DistilBERT, and a combined model.
  - Evaluation metrics: Precision, Recall, F1, F2, and nCS-DCG@10.
  - Methodologies: Intrinsic and extrinsic evaluations.

### 2. Gather Resources
- **Datasets:**
  - Obtain the OHSUMED and Avocado collections through authorized channels.
  - Ensure compliance with licensing and non-disclosure agreements for sensitive datasets.
- **Software and Libraries:**
  - Install necessary Python libraries, e.g., `scikit-learn`, `transformers`, and `pandas`.
  - Set up environments for machine learning models like HuggingFace's DistilBERT.
- **Infrastructure:**
  - Use platforms like Google Colaboratory or local GPU-based machines for experiments.

### 3. Reproduce Experimental Setup
- **Data Preprocessing:**
  - Follow the described preprocessing steps for OHSUMED and Avocado datasets.
  - For Avocado emails, segment texts into 500-token passages with a 220-token stride.
- **Model Training:**
  - Train Logistic Regression and DistilBERT models on the datasets.
  - Implement the combined model logic as described.
  - Perform cross-validation for Avocado and split OHSUMED into training, validation, and test sets.
- **Parameter Tuning:**
  - Use grid search to optimize thresholds for sensitivity classification.
  - Calibrate DistilBERT probabilities using linear transformation (similar to Platt scaling).

### 4. Conduct Experiments
- **Intrinsic Evaluation:**
  - Compute Precision, Recall, F1, F2, and Accuracy for each model on both datasets.
  - Compare results with the reported values in the paper.
- **Extrinsic Evaluation:**
  - Implement post-filtering and joint sensitivity-aware ranking approaches.
  - Use the Coordinate Ascent ranking algorithm and nCS-DCG@10 for evaluation.

### 5. Document Findings
- **Log Intermediate Results:**
  - Record all numerical results, parameter values, and deviations from the reported numbers.
- **Analyze Discrepancies:**
  - Identify potential causes of deviations (e.g., differences in dataset splits, implementation details).
  - Test the impact of these discrepancies on the results.

### 6. Statistical Testing
- **Significance Tests:**
  - Perform statistical tests (e.g., McNemar's test, t-tests) to assess significance in performance differences.
- **Variance Analysis:**
  - Check for stability across runs (e.g., different random seeds) and document variability.

### 7. Prepare the Report
- Format the report using the ACM Conference Proceedings single-column template.
- Include:
  - Experimental strategies.
  - Key findings and statistical analysis.
  - Deviations from the original results and their implications.
  - Conclusions about reproducibility and design flaws.

### 8. Submit Materials
- **Code and Documentation:**
  - Ensure code is well-documented and reproducible.
  - Provide machine-readable experiment descriptions.
- **Upload to Zenodo:**
  - Publish the report and scripts to the TU Wien ExDDS WS 2024/25 Zenodo community.
  - Make the submission open or embargoed until the exercise deadline.

### 9. Prepare Presentation
- Create a concise slide deck (4-5 slides) covering:
  - Group details and paper title.
  - Experimental strategies and challenges.
  - Key findings and conclusions.
  - Status of remaining work.
- Rehearse to ensure a 180-second time limit.

## Timeline
- **By Dec 19, 2024:** Confirm group and assigned presentation time slot.
- **Jan 09, 16, 23, 2025:** Present project status in class.
- **Feb 1, 2025:** Submit slides for presentation.
- **Feb 2, 2025:** Final submission to TUWEL and Zenodo.

---

