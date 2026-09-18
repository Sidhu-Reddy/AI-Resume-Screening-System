# AI Resume Screening System — Week 2: Data Cleaning and Transformation Documentation

**Virtual Data Science Apprentice — Python Specialist Intern**
**Task period:** 26-Sep-2026 to 02-Oct-2026 (Week 2 of 4)
**Intern:** [Your Name]

## Overview

This repository/folder contains the Week 2 deliverable for the **AI Resume Screening System** internship project: a documented data cleaning and transformation strategy that converts the raw, inconsistent resume text (selected in Week 1) into a clean, structured, model-ready dataset.

## Contents

| File | Description |
|------|-------------|
| `Week2_Data_Cleaning_Transformation.docx` | Full cleaning & transformation report (data quality issues, cleaning pipeline, missing-value rules, deduplication, feature engineering, pseudo-code) |

## Data Quality Issues Addressed

- Duplicate / near-duplicate resumes
- Missing fields (blank category labels, missing sections)
- Inconsistent formatting from PDF extraction (bullets, whitespace, artifacts)
- Encoding issues (non-UTF-8 characters, smart quotes)
- Inconsistent skill/degree terminology (e.g., "ML" vs. "Machine Learning")
- Length outliers (extremely short or long resumes)
- Class imbalance across job categories

## Cleaning & Transformation Pipeline

```
Ingestion & Deduplication → Missing Value Handling → Text Normalization
   → Tokenization & Linguistic Cleaning → Entity & Skill Standardization
   → Outlier Treatment → Feature Scaling & Encoding
```

## Key Design Decisions

- Rows missing a category label or resume body text are dropped (required for supervised learning); other missing fields are imputed with explicit placeholders and an `was_imputed` flag.
- Duplicates are detected via exact-hash matching and near-duplicate detection using TF-IDF cosine similarity (≥0.95 threshold).
- Skills are standardized against an O*NET-informed synonym dictionary.
- Numeric features (years of experience, word count) are scaled with `StandardScaler` for distance-based models, left unscaled for tree-based models.
- Every cleaning action is logged to a `cleaning_log.csv` for auditability.

## Tools & Python Libraries

pandas, numpy, re (regex), NLTK, spaCy, scikit-learn (`TfidfVectorizer`, `StandardScaler`), fuzzywuzzy / difflib, langdetect

## Estimated Effort

30–35 hours across research, implementation of cleaning/transformation logic, documentation, and validation.

## Next Steps

Week 3 will perform exploratory data analysis on this cleaned dataset to inform feature selection and modeling decisions.

## Author

[Your Name] — Virtual Data Science Apprentice, Python Specialist Intern
