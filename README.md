# Netflix Titles: End-to-End Data Science Project

## Project Overview

This project presents an end-to-end data science workflow using the Netflix Titles dataset. It combines data preparation, exploratory data analysis (EDA), machine learning, and model evaluation to study patterns in Netflix movies and TV shows.

The project was completed as part of the SWYNEX Technologies Data Science Internship.

## Objectives

- Prepare and clean the Netflix dataset.
- Explore the distribution of movies and TV shows.
- Examine content attributes such as genre, country, rating, and release year.
- Build baseline machine learning models.
- Evaluate model performance and document limitations.

## Dataset

The dataset contains **8,807 records and 12 columns** describing Netflix titles.

Key attributes include:
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
- Inspected the dataset structure and missing values.
- Checked duplicate records and identifier uniqueness.
- Processed date fields and reviewed inconsistent or missing values.
- Saved the cleaned dataset for further analysis.

### 2. Exploratory Data Analysis (EDA)
- Examined the distribution of movies and TV shows.
- Investigated content attributes and catalog patterns.
- Used visualizations and summary statistics to understand the dataset.

### 3. Modeling and Evaluation
Baseline classification experiments were conducted to predict the content type (`Movie` or `TV Show`).

| Experiment | Accuracy | Macro F1-score |
|---|---:|---:|
| Dummy Classifier | 69.64% | 0.4105 |
| Logistic Regression without genre | 74.46% | 0.6582 |
| Logistic Regression with genre | 100.00% | 1.0000 |

**Important interpretation:** The perfect score obtained with genre-related information may reflect a strong association between the feature and the target rather than generalizable predictive performance. It should not be treated as proof of a perfect real-world model. The model without genre provides a more conservative comparison, although further validation is still required.

## Key Findings

- The dataset contains 8,807 Netflix titles.
- The target classes are not evenly distributed, making macro F1-score useful alongside accuracy.
- Removing genre-related information reduced model performance, suggesting that this feature carries a strong signal for content type.
- Results depend on feature selection and the evaluation setup.

## Limitations

- The data represents a particular catalog snapshot.
- The target classes are imbalanced.
- The experiments use a single stratified train/test split.
- Cross-validation and external validation have not been performed.
- Model performance does not establish business usefulness or future predictive accuracy.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook
- GitHub

## Repository Contents

- `modeling_evaluation.ipynb` — modeling experiments and evaluation
- `netflix_titles_cleaned.csv` — cleaned dataset
- `requirements.txt` — Python dependencies

## How to Run

1. Clone this repository.
2. Install the dependencies.
3. Open the notebook in Jupyter Notebook or VS Code.
4. Run the notebook cells in order.

```bash
git clone https://github.com/shashiranjantiwari548-creator/SWYNEX-Final-Data-Science-Project.git
cd SWYNEX-Final-Data-Science-Project
pip install -r requirements.txt
```

## Conclusion

This project demonstrates a complete introductory data science workflow, from data preparation and exploratory analysis to model evaluation. It also highlights why model metrics must be interpreted carefully and why additional validation is important before drawing real-world conclusions.

## Internship

Completed as part of the SWYNEX Technologies Data Science Internship.

**Author:** Shashiranjan Kumar Tiwari
