# AI Resume Screening System — Week 4: Machine Learning Model Selection and Evaluation Plan

**Virtual Data Science Apprentice — Python Specialist Intern**
**Task period:** 10-Oct-2026 to 16-Oct-2026 (Week 4 of 4)
**Intern:** [Your Name]

## Overview

This repository/folder contains the Week 4 (final) deliverable for the **AI Resume Screening System** internship project: a machine learning model selection and evaluation plan for classifying resumes into job categories, completing the four-week workflow.

## Contents

| File | Description |
|------|-------------|
| `Week4_ML_Model_Selection_Evaluation.docx` | Full modeling plan (candidate models, evaluation metrics, selection process, cross-validation strategy, fairness review) |

## Modeling Problem

Multi-class text classification: predict a resume's job category from cleaned text (TF-IDF / embeddings) and engineered numeric features (from Weeks 2–3). Resume-to-job-description similarity scoring is treated as a secondary, unsupervised stretch goal using cosine similarity.

## Candidate Models Compared

| Model | Role |
|---|---|
| Logistic Regression (multinomial) | Fast, interpretable baseline |
| Linear SVM | Strong performer on sparse TF-IDF text |
| Random Forest | Captures non-linear interactions in engineered features |
| XGBoost / LightGBM | High-accuracy option combining text + numeric features |
| Sentence-embedding classifier | Semantic, stretch-goal comparison model |

## Evaluation Metrics

Accuracy, per-class & weighted Precision/Recall, F1-score (macro & weighted — primary metric), Confusion Matrix, ROC-AUC (one-vs-rest)

## Model Selection & Evaluation Process

```
Stratified Train/Test Split → Baseline Training (LogReg, SVM)
   → Feature-Augmented Training (RF, XGBoost) → Stretch Model (embeddings)
   → Hyperparameter Tuning (k-fold CV) → Model Comparison → Error Analysis
```

## Key Design Decisions

- Stratified 80/20 train/test split to preserve category proportions.
- 5-fold stratified cross-validation for tuning, with a held-out test set never used during tuning.
- Weighted F1-score used as the primary model-selection metric due to class imbalance.
- Explicit fairness review of whether misclassification or feature importance correlates with proxies for protected characteristics.

## Tools & Python Libraries

scikit-learn (Logistic Regression, SVM, Random Forest, `GridSearchCV`), XGBoost / LightGBM, sentence-transformers (stretch goal), pandas, numpy

## Estimated Effort

30–35 hours across literature review, model comparison framework design, evaluation/fairness documentation, and revision.

## Project Status

This completes the planning phase of the AI Resume Screening System across all four weeks (dataset scoping → cleaning → EDA → modeling plan). This is an educational prototype; further validation would be required before any real-world hiring use.

## Author

[Your Name] — Virtual Data Science Apprentice, Python Specialist Intern
