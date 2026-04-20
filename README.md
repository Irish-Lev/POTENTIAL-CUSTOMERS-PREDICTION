# Potential Customers Prediction

## 1. Project Title & Short Description

This project uses machine learning to predict which ExtraaLearn leads are most likely to convert into paid customers based on demographic, behavioral, and engagement features.

---

## 2. Dataset Description

### Dataset overview
- **Dataset name:** ExtraaLearn Customers Prediction
- **Records:** 4,612 rows
- **Features:** 15 columns
- **Target variable:** `status` (converted vs not converted)

### Key variables
The dataset includes:
- `age`
- `current_occupation`
- `first_interaction`
- `profile_completed`
- `website_visits`
- `time_spent_on_website`
- `page_views_per_visit`
- `last_activity`
- media/referral flags such as `digital_media`, `educational_channels`, and `referral`

### Data quality notes
- No missing values were identified.
- No duplicate rows were found.
- The target appears imbalanced, with roughly **30% converted** and **70% not converted**.

### Source / attribution
I was able to verify that this is a publicly referenced **ExtraaLearn lead-conversion case study** used in applied machine learning coursework and shared online in portfolio examples and notebooks.

A public reference to the case study appears here:
- [Kaggle notebook reference: Potential Customer Prediction - ExtraaLearn](https://www.kaggle.com/code/moinulhossaindhrubo/potential-customer-prediction-extraalearn)

> Note: I could not independently verify a definitive original public download page for the raw CSV beyond the ExtraaLearn case-study material, so this README states that transparently.

---

## 3. Research Goal / Question

The main objective of the project is to answer the following question:

**Which leads are most likely to convert into paying customers, and what factors drive that conversion?**

This project also explores:
- which channels are most effective,
- whether website engagement is linked to conversion,
- and which model performs best for lead prediction.

---

## 4. Steps Taken

### Data preparation
- Loaded and inspected the dataset
- Checked shape, data types, missing values, duplicates, and identifier columns
- Dropped the ID column because it does not contribute to prediction

### Exploratory Data Analysis
- Univariate analysis for numeric and categorical features
- Conversion-rate analysis by occupation, first interaction, last activity, and referral/media channels
- Visualizations for distributions, conversion patterns, and feature relationships

### Feature engineering and preprocessing
- Split variables into numeric and categorical groups
- Applied scaling and encoding using preprocessing tools
- Prepared training and testing datasets

### Modeling
Built and evaluated:
- Decision Tree Classifier
- Tuned Decision Tree using GridSearchCV
- Random Forest Classifier
- Tuned Random Forest using GridSearchCV

### Evaluation metrics
- Accuracy
- ROC-AUC
- Confusion Matrix
- Classification Report
- Feature Importance

---

## 5. Main Findings

### Key insights
- Only about **30% of leads convert**, confirming that lead prioritization is important.
- Leads with stronger engagement, especially higher **time spent on the website**, **website visits**, and **page views per visit**, are more likely to convert.
- **Referral-based leads** and leads with **higher profile completion** show stronger conversion potential.
- **Professionals** appear more likely to convert than other occupation groups in this dataset.

### Best model
The strongest model in the notebook is the **tuned Random Forest model**:
- **Accuracy:** 72.26%
- **ROC-AUC:** 70.90%

This outperformed the earlier Decision Tree runs and provided the most balanced predictive performance for this project.

---

## 6. How to Reproduce the Project

### Requirements
- Python 3.9+
- Jupyter Notebook
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

### Run steps
1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
3. Place the dataset file in the project folder.
4. Open and run the notebook:
   ```bash
   jupyter notebook Irish_Levi_Bawingan_Customers_Prediction.ipynb
   ```

---

## 7. Next Steps / Ideas for Improvement

- Improve recall for the converted class using class balancing or threshold tuning
- Test additional models such as XGBoost or Logistic Regression
- Build a dashboard for marketing or sales teams
- Deploy the model as a simple web application for lead scoring
- Add more business features such as campaign source, region, or follow-up timing

---

## 8. Repository Structure

```text
POTENTIAL_CUSTOMERS_PREDICTION_ELECTIVE/
├── Irish_Levi_Bawingan_Customers_Prediction.ipynb   # Most complete notebook for upload
├── Customers_Prediction.ipynb                       # Earlier/incomplete notebook draft
├── Irish_Levi_Bawingan_Customers_Prediction.html    # Exported notebook view
├── ExtraaLearn_Customers_Prediction.csv             # Local dataset used for analysis
└── README.md                                        # Project overview and documentation
```

---

## Recommendation for GitHub Upload

For a cleaner and more professional portfolio repository, the best notebook to upload is:

**`Irish_Levi_Bawingan_Customers_Prediction.ipynb`**

It is more complete because it contains:
- executed cells,
- visible outputs and charts,
- full EDA,
- model building,
- hyperparameter tuning,
- and final business recommendations.

The file `Customers_Prediction.ipynb` appears to be an earlier and less complete draft.
