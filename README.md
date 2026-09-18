# AI Resume Screening System — Week 3: Exploratory Data Analysis and Visualization Strategy

**Virtual Data Science Apprentice — Python Specialist Intern**
**Task period:** 03-Oct-2026 to 09-Oct-2026 (Week 3 of 4)
**Intern:** [Your Name]

## Overview

This repository/folder contains the Week 3 deliverable for the **AI Resume Screening System** internship project: an exploratory data analysis (EDA) and visualization strategy built on the cleaned resume dataset from Week 2, aimed at understanding class balance, vocabulary structure, and data quality before modeling.

## Contents

| File | Description |
|------|-------------|
| `Week3_EDA_Visualization_Strategy.docx` | Full EDA report (objectives, planned visualizations, workflow, expected insights, mock-up layout) |

## EDA Objectives

- Quantify class balance across job categories
- Identify the most frequent and most distinctive skills/keywords per category
- Characterize resume length and structural completeness
- Surface residual data-quality anomalies before modeling
- Translate every chart into a plain-language insight for a non-technical audience

## Planned Visualizations

| Visualization | Purpose |
|---|---|
| Bar chart of resumes per category | Reveal class imbalance |
| Histogram / KDE of word count | Show resume length distribution and outliers |
| Box plots by category | Compare length norms across categories |
| Word clouds (TF-IDF weighted) | Surface distinctive terms per category |
| Top-N TF-IDF term bar charts | Identify category-defining vocabulary |
| Skill co-occurrence heatmap | Reveal commonly paired skills |
| t-SNE / UMAP scatter plot | Visually assess category separability |
| Missing-data completeness chart | Confirm Week 2 cleaning improvements |

## EDA Workflow

```
Load Cleaned Data → Univariate Analysis → Category-Level Analysis
   → Text-Specific Analysis → Dimensionality Reduction → Insight Synthesis
```

## Tools & Python Libraries

pandas, matplotlib, seaborn, wordcloud, scikit-learn (`TfidfVectorizer`, `TSNE`), umap-learn

## Estimated Effort

30–35 hours across reviewing EDA best practices, drafting the visualization plan, writing chart rationale, and refinement.

## Next Steps

Week 4 will use these insights (class imbalance, category vocabulary overlap, length patterns) to guide feature engineering and model selection.

## Author

[Your Name] — Virtual Data Science Apprentice, Python Specialist Intern
