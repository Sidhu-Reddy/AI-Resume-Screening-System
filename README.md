# AI Resume Screening System — Week 1: Project Planning and Dataset Scoping

**Virtual Data Science Apprentice — Python Specialist Intern**
**Task period:** 18-Sep-2026 to 25-Sep-2026 (Week 1 of 4)
**Intern:** [Your Name]

## Overview

This repository/folder contains the Week 1 deliverable for the **AI Resume Screening System** internship project: a project plan that defines the problem, objectives, scope, candidate datasets, and high-level workflow for building a Python-based system that automatically screens and ranks resumes against a job description.

## Contents

| File | Description |
|------|-------------|
| `Week1_Project_Planning_Dataset_Scoping.docx` | Full project plan report (objectives, scope, dataset comparison, workflow, tools, risks, effort estimate) |

## Problem Statement

Recruiters often receive hundreds of resumes per job opening, and manually screening each one for relevant skills and experience is slow and inconsistent. This project frames resume screening as a **text classification and similarity-ranking problem**: given a labeled corpus of resumes and a target job description, build a Python pipeline that predicts each resume's job category and a fit score relative to the job description.

## Project Objectives

- Build an end-to-end Python pipeline from raw resume text to a ranked candidate list.
- Establish a clean, labeled dataset suitable for supervised learning.
- Design a reproducible workflow: acquisition → cleaning → feature engineering → EDA → modeling → evaluation.
- Quantify model performance with metrics a non-technical recruiter can interpret.
- Document assumptions, limitations, and fairness considerations throughout.

## Candidate Datasets Evaluated

| Dataset | Source | Why it was considered |
|---|---|---|
| Resume Dataset | [Kaggle](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset) | ~2,400 resumes labeled across 24 job categories — **selected as the primary dataset** |
| Resume Entities for NER | Kaggle | Entity-level annotations useful for skill/degree extraction |
| LinkedIn Job Postings | [Kaggle](https://www.kaggle.com/datasets/arshkon/linkedin-job-postings) | Real job descriptions for resume-to-job similarity scoring |
| O*NET Database | [onetonline.org](https://www.onetonline.org/) | Standardized skill/occupation taxonomy for normalization |

## Planned High-Level Workflow

```
Data Acquisition → Data Cleaning → Text Preprocessing → Feature Engineering
       → Exploratory Data Analysis → Model Selection & Training → Evaluation & Reporting
```

## Tools & Python Libraries

pandas, numpy, nltk, spaCy, scikit-learn, XGBoost, matplotlib, seaborn, pdfplumber / PyPDF2, python-docx, Jupyter Notebook

## Estimated Effort

30–35 hours across background research, objective/scope definition, workflow and tool planning, drafting, and revision.

## Next Steps

Week 2 will use the dataset selected here to define and document a full data cleaning and transformation pipeline.

## Author

[Your Name] — Virtual Data Science Apprentice, Python Specialist Intern
