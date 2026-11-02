# 🧬 Fertility Data Mining – Weka Analysis

A data mining project that applies **Weka** to the **Fertility dataset** from the UCI Machine Learning Repository.  
The goal is to explore the factors associated with altered seminal quality using classification and regression techniques available in the Weka workbench.

> **Note:** This repository contains **data and a written report**, not executable code. The analysis is performed interactively in Weka.

---

## 📖 Overview

`FertilityDataMining` documents a Weka-based analysis of the Fertility dataset.  
The dataset was donated to UCI in 2013 and contains **100 instances** with **9 features** plus a **binary target variable** (`diagnosis`: `N` = normal, `O` = altered)[reference:1].  
The features cover socio-demographic, environmental, health, and lifestyle factors:

- **Season** in which the analysis was performed (winter, spring, summer, fall)
- **Age** at the time of analysis
- **Childish diseases** (chicken pox, measles, mumps, polio)
- **Accident or serious trauma**
- **Surgical intervention**
- **High fevers** in the last year
- **Alcohol consumption** frequency
- **Smoking habit**
- **Number of hours spent sitting per day**[reference:2]

The project demonstrates how Weka can be used for **data preprocessing, classification, regression, and exploratory analysis** on this dataset.

---

## 🗂️ Repository Contents

| File | Description |
|------|-------------|
| `README.me` | Original one-line note: *“fertility dataset datamining using Weka software”*[reference:3]. |
| `dataset.csv` | The Fertility dataset in CSV format (100 instances, 10 attributes including the target). |
| `report.docx` | A written report documenting the data mining process and findings. |

> **Suggestion:** Rename `README.me` to `README.md` so GitHub renders it as the project’s main documentation page.

---

## 🔬 Dataset Summary

- **Source:** UCI Machine Learning Repository – Fertility Data Set[reference:4].
- **Instances:** 100.
- **Attributes:** 10 (9 features + 1 target).
- **Task type:** Classification and regression (Weka supports both)[reference:5].
- **Missing values:** None[reference:6].
- **Target:** `diagnosis` – `N` (normal) or `O` (altered) seminal quality.
- **License:** CC BY 4.0 (as per UCI)[reference:7].

---

## 🛠️ Weka Workflow (Suggested)

The `report.docx` likely documents a workflow similar to the following.  
You can reproduce or extend it by opening `dataset.csv` in the **Weka Explorer**:

1. **Load the data**
   - Open Weka → Explorer → `Preprocess` tab.
   - Click `Open file…` and select `dataset.csv`.

2. **Preprocess**
   - Verify attribute types (e.g., `season` as numeric or nominal, `diagnosis` as nominal).
   - Optionally discretize or normalize features using Weka filters (`Discretize`, `Normalize`).

3. **Classify**
   - Go to the `Classify` tab.
   - Choose a classifier (e.g., `J48` decision tree, `NaiveBayes`, `IBk` k-NN, `SMO` SVM).
   - Set `Test options` to cross-validation (e.g., 10-fold) or percentage split.
   - Click `Start` and inspect the accuracy, confusion matrix, and detailed statistics.

4. **Regress** (if treating `diagnosis` numerically)
   - Use `LinearRegression`, `M5P`, or other regressors on a numeric version of the target.

5. **Cluster / Associate** (optional)
   - Use the `Cluster` tab (e.g., `SimpleKMeans`) or `Associate` tab (e.g., `Apriori`) for unsupervised exploration.

6. **Visualize**
   - Use the `Visualize` tab to plot feature distributions and class separation.
