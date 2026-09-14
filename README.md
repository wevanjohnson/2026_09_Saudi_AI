# AI Bootcamp in Biotechnology: Machine Learning and AI for Biomedical Research

Materials for the **Rutgers / KAIMRC Academy AI Bootcamp in Biotechnology**, hosted by
KAIMRC Academy in partnership with the Rutgers Center for Biomedical Informatics &
Health Artificial Intelligence (BMIHAI).

*Instructor: W. Evan Johnson, Ph.D.*

## When & where

* **Date:** Tuesday, September 15, 2026
* **Time:** 8:00 AM – 4:00 PM (8 hours)
* **Location:** KAIMRC Academy, Riyadh, Saudi Arabia
* **Format:** Short course, 20–25 participants

## Things you should know about this bootcamp

* Lots of diverse material and new concepts in a single day.
    + Programming and machine learning are __NOT__ spectator sports -- you need to practice these skills over and over again.
* Each lecture has a matching hands-on workshop to work through on your own.
* Materials are in R, but the concepts are language-agnostic -- every method shown here has a direct `scikit-learn` equivalent.
* Questions any time: <w.evan.johnson@rutgers.edu>
* Materials:
    + All materials are posted on GitHub: [https://github.com/wevanjohnson/2026_09_Saudi_AI](https://github.com/wevanjohnson/2026_09_Saudi_AI)
    + `session_1_*` and `session_2_*` hold the morning keynote decks.
    + `lecture_1_*` through `lecture_5_*` hold the afternoon applied-session decks (`.Rmd` source plus rendered `.pdf`), each with the figure directory it depends on, so every deck knits standalone.
    + `workshop_1` through `workshop_4` and `workshop_capstone` hold the hands-on materials (`.Rmd` source plus rendered `.html`). These are for working through on your own -- there is no lab time for them during the course.
    + Data files sit alongside the materials that use them.

## Setup

Helpful background:

* Introductory statistics and molecular biology
* Basic R programming: `tidyverse`, `ggplot2`, R Markdown

Please do the following before the bootcamp:

* **Bring a laptop.**
* **Install R and RStudio.**
* **Install the R packages** used in the slides and hands-on examples:

```r
install.packages(c(
  "tidyverse", "caret", "DT", "gridExtra", "kableExtra", "dslabs",
  "e1071", "rpart", "randomForest", "neuralnet", "nnet",
  "gbm", "glmnet", "pROC", "xgboost", "lime", "caretEnsemble",
  "kernlab", "mda", "umap", "gam"
))
```

The capstone workshop and the dimension-reduction workshop additionally use
Bioconductor packages:

```r
if (!require("BiocManager")) install.packages("BiocManager")
BiocManager::install(c("DESeq2", "edgeR", "limma", "sva",
                       "SummarizedExperiment", "ComplexHeatmap",
                       "TBSignatureProfiler", "enrichR"))
```

* The afternoon hands-on lab uses the **AiCCESS** platform — access details will be
  circulated by the KAIMRC Academy team before the course.

## Schedule

| Time | Session |
|------|---------|
| 8:00 – 8:10 | Welcome & opening remarks (Dr. Najwa Borkadi) |
| 8:10 – 9:10 | **Session 1** — The Center for Biomedical Informatics and Health AI at Rutgers Health: training, research, and collaborative opportunities |
| 9:10 – 9:30 | Q&A |
| 9:30 – 10:00 | **Session 2** — Introduction to Generative and Agentic AI: transformers, AI agents, AI tools, Model Context Protocol (MCP), research workflows |
| 10:00 – 10:10 | Q&A |
| 10:30 – 10:45 | Coffee break |
| 10:45 – 11:15 | **Session 3** — Leveraging clinical and research data for AI-driven healthcare innovation (Dr. Asma Alfayez) |
| 11:15 – 11:25 | Q&A |
| 11:25 – 12:30 | Lunch break |
| 12:30 – 1:00 | **Session 4** — Learning at the speed of intelligence: building a human-centered future for medical education (Dr. Mayur Narayan) |
| 1:00 – 1:10 | Q&A |

### Applied session: Machine Learning and AI for Biomedical Research — From Foundations to Frontier

*Instructors: Dr. Evan Johnson · Dr. Divya Kewalramani*

| Time | Session |
|------|---------|
| 1:10 – 1:30 | **The machine learning landscape** — choosing the right AI tool for your research question |
| 1:30 – 1:50 | **Classical machine learning** — support vector machines, random forests, XGBoost |
| 1:50 – 2:00 | Break |
| 2:00 – 2:20 | **Model evaluation and common pitfalls** — validation strategies, data leakage, reproducibility |
| 2:20 – 2:50 | **Neural networks** |
| 2:50 – 3:20 | **Large language models and generative AI** — conceptual foundations and biomedical applications |
| 3:20 – 4:30 | **Hands-on session** — Clinical AI development using AiCCESS: a longitudinal case study (Dr. Divya Kewalramani) |
| 4:30 – 4:50 | Closing remarks & Q&A |

## Repository contents

| Folder | Topic |
| :--- | :---- |
| `session_1_bmihai_center/` | The Rutgers BMIHAI Center: training, research, and collaboration |
| `session_2_genai_agentic/` | Generative and agentic AI — concepts, agents, tools, MCP, research workflows |
| `lecture_1_ml_landscape/` | Introduction to machine learning and data science; supervised vs. unsupervised learning; choosing a method |
| `lecture_2_classical_ml/` | Support vector machines and kernels; decision trees and random forests; boosting and XGBoost; LIME and SHAP |
| `lecture_3_model_evaluation/` | Training and test sets; confusion matrices, sensitivity and specificity; cross-validation and the bootstrap; bias-variance tradeoff; **data leakage**; **reproducibility** |
| `lecture_4_neural_networks/` | A short history of neural networks; multilayer perceptrons; recurrent and convolutional neural networks |
| `lecture_5_llm_genai/` | Attention and transformers; large language models; agentic workflows; biomedical applications |

### Hands-on workshops

Each workshop is a self-contained R Markdown document with a rendered HTML version.
Work through them at your own pace after the course. The workshops are written in R;
if you work in Python, the rendered HTML still reads as a walkthrough of the method,
and each step maps onto `scikit-learn`.

| Folder | Topic | Pairs with |
| :--- | :---- | :--- |
| `workshop_1/` | Dimension reduction: PCA, UMAP, and visualization with `ggplot2` | Lecture 1 |
| `workshop_2/` | Support vector machines, decision trees, and random forests | Lecture 2 |
| `workshop_3/` | Machine learning with `caret`: data partitioning, cross-validation, ROC and AUC across six algorithms; **a worked data-leakage demonstration**; regularization with `glmnet` | Lecture 3 |
| `workshop_4/` | Working with the TB NanoString data | Lecture 4 |
| `workshop_capstone/` | End-to-end applied analysis of RePORT India TB data: elastic net, SVM, and random forest compared | All lectures |

## Data

The classical machine learning and evaluation examples use **`TBnanostring.rds`** — a
NanoString gene expression dataset for tuberculosis classification — as a through-line, so
the same biomarker problem is carried across methods. The nonlinear SVM examples use
`ESL.mixture.rda` from *The Elements of Statistical Learning*.

## Acknowledgements

Portions of this material are adapted from the Rutgers courses *Machine Learning for
Biomedical Data* (GSND 4355Q) and the BMIHAI Summer Bootcamp series, and from:

1. *The Elements of Statistical Learning*, 2nd Edition, by Trevor Hastie, Robert Tibshirani, and Jerome Friedman: https://hastie.su.domains/ElemStatLearn/
2. *Introduction to Data Science: Data Analysis and Prediction Algorithms with R*, by Rafael A. Irizarry: https://rafalab.github.io/dsbook/
3. *Mathematical Foundations for Data Analysis*, by Jeff M. Phillips: https://mathfordata.github.io

The agentic AI material draws on slides by Xutao Wang.

## Questions / Inquiries

Please email <w.evan.johnson@rutgers.edu>.
