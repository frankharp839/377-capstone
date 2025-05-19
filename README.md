# Diabetes Risk prediction using Machine Learning 
*Francisco Montero* | *MATH 377: Applied Statistics and Probability* | *Spring / 2025*

---

## Table of Contents

1.	Project Overview
2.	Data Description
3.	Model Evaluation and Framework
4.	Results Summary
5.	Next Steps
6.	Installation & Setup
7.	Project Structure
8.	Project Flow
9.	Notebooks & Modules
10.	Usage
11.	Results & Deliverables
12.	Slide Deck
13.	Contributing
14.	License

---

## Project Overview  

**Problem Statement**  

The goal of the project is reducing the risk of diabetes by identifying factors that lead to the disease and use that information to formulate prevention methods. The project seeks to address the relationship between a patient’s biomarkers (e.g. blood pressure and glucose levels) and lifestyle habits that are considered unhealthy.  

**Proposed Solution**  

We aim to develop machine learning models to identify the risk of diabetes using:

1.	Logistic Regression
2.	Decision Trees
3.	Random Forests

These models will:

- Provide insight of what is influencing diabetes. 
- Identify strategies to manage the risk of the disease. 

**Impact** 

The potential impact of this project includes:

- Supporting and growing a healthier community.
- Better health education to any affected communities. 
- Healthcare workers can focus on developing resources for those who are at risk.

---

## Data Description  
- **Source:** Kaggle: https://www.kaggle.com/datasets/akshaydattatraykhare/diabetes-dataset
- **Raw Files:** Located under `data/raw/` (e.g., `transactions.csv`, `users.json`)  
- **Processed Files:** Produced by your cleaning pipeline in `data/processed/`

| File name | Description |
|-----------|-------------|
| `data/raw/dataset.csv` | Original full dataset |
| `data/processed/train.csv` | Cleaned & feature‑engineered training set |
| `data/processed/test.csv`  | Cleaned & feature‑engineered test set |

Our analysis utilizes a dataset of females from the Gila River Indian community in Arizona. The dataset includes:

1.	Age (int64), Pregnancies (int64), and Outcomes (int64) of getting diabetes or not.
2.	Biomarkers (Blood Pressure (float64), Glucose (float64), Insulin (float64), Body Mass Index (float64), Diabetes Pedigree Function (float64))


---

## Modeling and Evaluation Framework

1.	Data preprocessing.
2.	Implementation of Logistic Regression, Decision Trees and Random Forest.
3.	Implementation of hyperparameter tuning to boost performance for each model.
4.	Model evaluation using classification reports, feature importance, ROC AUC scoring and confusion matrices.

---

## Results Summary

All three models nearly have the same accuracy score with random forest being the highest. 

The logistic regression and random forest model nearly have the same ROC AUC score with decision trees having the lowest.

While the confusion matrix for the decision tree model 65% correctly predicts patients getting diabetes, it's not able to take features like Skin Thickness and Blood Pressure into consideration as seen from the feature importance table. 

Also, the classification report shows that the precision for both classes is imbalanced which is risky for diagnosing a disease. 

On the other hand, random forests take all features into consideration and its classification report shows that the precision for both classes are balanced.

Therefore, the best model to use is random forest as it's the highest in accuracy, ROC AUC score, and the precision for both classes are balanced.


## Next Steps

1.	Trying more data preprocessing techniques.
2.	Better handle class imbalance.
3.	Trying more model performance boosting methods.


## Project Structure  
    CapstoneProject/
    ├── README.md
    ├── .gitignore
    ├── requirements.txt
    │
    ├── data/
    │   ├── raw/                # Immutable source data
    │   └── processed/          # Cleaned, feature‑engineered data
    │
    ├── notebooks/              # Jupyter notebooks
    │   ├── 1_data_prep.ipynb
    │   ├── 2_eda.ipynb
    │   ├── 3_baseline_models.ipynb
    │   └── 4_final_modeling.ipynb
    │
    ├── src/ (OPTIONAL)         #  Reusable Python modules
    │   ├── __init__.py
    │   ├── preprocessing.py
    │   ├── features.py
    │   ├── modeling.py
    │   └── evaluation.py
    │
    ├── slides/                 # Slide deck PDF & source
    │   ├── Capstone_Final_Presentation.pdf
    │   └── Capstone_Final_Presentation.pptx
    │
    ├── outputs/                # Model artifacts & figures
    │   ├── models/
    │   └── figures/
    │
    └── tests/                  # (Optional) unit tests for src/

---

## Project Flow  

    Raw Data Ingestion  →  Data Cleaning  
    Data Cleaning       →  Feature Engineering  
    Feature Engineering →  Exploratory Data Analysis  
    EDA                 →  Baseline Modeling  
    Baseline Modeling   →  Advanced Modeling & Optimization  
    Advanced Modeling   →  Model Evaluation & Interpretation
    Evaluation          →  Deployment & Reporting  

1. **Raw Data Ingestion** – load source files and validate schema.  
2. **Data Cleaning** – handle missing values, remove duplicates, standardize formats.  
3. **Feature Engineering** – create new variables, encode categoricals, scale numerics.  
4. **Exploratory Data Analysis** – generate summary statistics and key visualizations (e.g. histograms, boxplots, scatterplots).  
5. **Baseline Modeling** – simple models (e.g., linear regression, logistic regression, decision tree, ARIMA) to set performance benchmarks.  
6. **Advanced Modeling & Optimization** – hyperparameter tuning, ensembles, or complex architectures (e.g. Random Forests, SARIMAX, Simple Neural Networks, LSTM, CNN, XGBoost etc.).  
7. **Model Evaluation & Interpretation** – compare metrics (e.g. MSE, MAE, Accuracy), confusion matrix, plot ROC / precision‑recall.  
8. **Deployment & Reporting** – save final model in `outputs/models/`, create figures in `outputs/figures/`, assemble slide deck.

---

## Notebooks & Modules  
| Path | Purpose |
|------|---------|
| `notebooks/1_data_prep.ipynb` | Data ingestion, cleaning, and saving processed files |
| `notebooks/2_eda.ipynb` | Visual and statistical exploration of cleaned data |
| `notebooks/3_baseline_models.ipynb` | Fit and evaluate initial benchmark models |
| `notebooks/4_final_modeling.ipynb` | Advanced modeling, optimization, and final evaluation |
| `src/preprocessing.py` | Functions for loading and cleaning data |
| `src/features.py` | Feature‑engineering utilities |
| `src/modeling.py` | Model training, tuning, and persistence |
| `src/evaluation.py` | Metric calculators and plotting helpers |

---

## Usage (OPTIONAL) 
1. **Activate your environment**  
    source .venv/bin/activate  

2. **Run notebooks in order** or convert them to scripts for automation.  

3. **Retrain final model**  
    python -c "from src.modeling import train_final; train_final()"  

4. **Generate evaluation plots**  
    python -c "from src.evaluation import plot_all; plot_all()"  

---

## Results & Deliverables  
- **Final Model** – stored at `outputs/models/best_model.pkl`  (OPTIONAL)
- **Key Figures** – located in `outputs/figures/` (e.g., feature importance, ROC curve)  
- **Metrics Summary** – documented in notebooks and slide deck  

---

## Slide Deck  
*Location:* `/slides/Capstone_Final_Presentation.pdf`  
Five slides covering: overview, data & preprocessing, key insights, model results, demo/design & next steps.

---

## Contributing (OPTIONAL) 
- Open issues for bugs or feature requests.  
- Follow code style in `src/` and add tests in `tests/` when applicable.  

---

## License  
This project is licensed under the **MIT License** – see `LICENSE` for details.
