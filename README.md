# Netflix Titles: End-to-End Data Science Project

## Project Overview

This project demonstrates an end-to-end data science workflow using the Netflix Titles dataset. It covers data preparation, exploratory data analysis (EDA), machine learning, model evaluation, and interpretation of results.

The project was completed as part of the **SWYNEX Technologies Data Science Internship**.

## Objectives

- Clean and prepare the Netflix Titles dataset.
- Explore movies, TV shows, ratings, genres, countries, and release years.
- Identify patterns through visualizations and summary statistics.
- Build baseline machine learning classification models.
- Evaluate model performance using accuracy and macro F1-score.
- Document findings, limitations, and opportunities for improvement.

## Dataset

The dataset contains **8,807 records and 12 columns** describing Netflix titles.

The main features include:

- `show_id`
- `type`
- `title`
- `director`
- `cast`
- `country`
- `date_added`
- `release_year`
- `rating`
- `duration`
- `listed_in`
- `description`

The dataset represents a catalog snapshot and may not reflect the current Netflix catalog.

## Project Workflow

### 1. Data Preparation

The data preparation process included:

- Inspecting the dataset structure and data types.
- Identifying missing values.
- Checking duplicate records and identifier uniqueness.
- Processing date fields and reviewing inconsistent or missing values.
- Saving the cleaned dataset for analysis and modeling.

### 2. Exploratory Data Analysis (EDA)

The EDA stage explored the Netflix catalog through summary statistics and visualizations.

Areas examined included:

- Movie and TV show distribution.
- Ratings distribution.
- Content added over time.
- Movie duration and TV show seasons.
- Countries represented in the dataset.
- Common genres and content categories.
- Data quality and missing-value patterns.

### 3. Modeling and Evaluation

Baseline classification experiments were conducted to predict the content type (`Movie` or `TV Show`).

| Experiment | Accuracy | Macro F1-score |
|---|---:|---:|
| Dummy Classifier | 69.64% | 0.4105 |
| Logistic Regression without genre | 74.46% | 0.6582 |
| Logistic Regression with genre | 100.00% | 1.0000 |

**Interpreting the results**

The model using genre-related information achieved a perfect score in this evaluation. However, this result may reflect a strong association between genre information and the target label rather than generalizable predictive performance.

Therefore, the perfect score should not be interpreted as proof of a perfect real-world model. The model without genre provides a more conservative comparison, but it also requires further validation.

## Key Findings

- The dataset contains 8,807 Netflix titles.
- Movies account for 6,131 titles (69.62%), while TV Shows account for 2,676 titles (30.38%).
- The target classes are imbalanced, making macro F1-score useful alongside accuracy.
- Removing genre-related information reduced model performance.
- Model results depend on feature selection and the evaluation setup.
- Further validation is required before drawing real-world conclusions.

## Limitations

- The dataset represents a particular catalog snapshot.
- The target classes are imbalanced.
- The experiments use a single stratified train/test split.
- Cross-validation and external validation have not been performed.
- Feature relationships may influence the observed model performance.
- Model performance alone does not establish business usefulness or future predictive accuracy.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git and GitHub

## Repository Contents

- `eda_analysis.ipynb` — exploratory data analysis, visualizations, and findings.
- `modeling_evaluation.ipynb` — classification experiments and model evaluation.
- `netflix_titles_cleaned.csv` — cleaned Netflix Titles dataset.
- `requirements.txt` — Python dependencies.

## Related Task Repositories

The following repositories contain the work completed in the earlier internship tasks:

- **Task 1 — Data Preparation:** [SWYNEX Data Preparation](https://github.com/shashiranjantiwari548-creator/SWYNEX-Data-Preparation)
- **Task 2 — Exploratory Data Analysis:** [SWYNEX Exploratory Data Analysis](https://github.com/shashiranjantiwari548-creator/SWYNEX-Exploratory-Data-Analysis)
- **Task 3 — Modeling and Evaluation:** [SWYNEX Modeling and Evaluation](https://github.com/shashiranjantiwari548-creator/SWYNEX-Modeling-and-Evaluation)

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/shashiranjantiwari548-creator/SWYNEX-Final-Data-Science-Project.git
cd SWYNEX-Final-Data-Science-Project
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebooks

Open the repository in Jupyter Notebook or VS Code and run the notebook cells in order.

Run `eda_analysis.ipynb` for exploratory analysis and `modeling_evaluation.ipynb` for the modeling experiments.

## Conclusion

This project demonstrates an introductory end-to-end data science workflow, from preparing a dataset and exploring its characteristics to training baseline classification models and evaluating their results.

It also highlights the importance of feature selection, suitable evaluation metrics, and careful interpretation of model performance.

## Internship

Completed as part of the **SWYNEX Technologies Data Science Internship**.

**Author:** Shashiranjan Kumar Tiwari
