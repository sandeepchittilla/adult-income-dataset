# adult-income-dataset
ML Approach to identify characteristics associated with income level of people (those earning >$50,000 vs <$50,000).

# Data
We use the publicly available [Adult Income Dataset](https://drive.google.com/drive/folders/1Yvd_q0lF1W7zbFFwufq3isLUzdejYf1Y?usp=sharing) from the 1994 US Census Board Database for this task. The `census_income_metadata` file contains information on data/datatypes. We have ~200,000 records in training set and XXX in testing.

# Solution

The notebook `adult_income.ipynb` contains end-to-end code for
1. Programmatically load data and check sanity against metadata file
2. Exploratory Data Analysis
3. Feature Engineering and Feature Encoding
4. Model Comparison and Selection (ROC AUC, PR AUC etc.)
     1. Logistic Regression
     2. RandomForest Classifier
     3. XGBoost Classifier
     4. CatBoost Classifier
5. Hyperparameter Tuning and Model Validation (Precision, Recall, Accuracy etc.)

6. Model Interpretation (Feature Importances, SHAP scores, Partial Dependency Plots etc.)


7. Imputation Techniques to handle imbalanced dataset (SMOTE, Oversampling, Undersampling etc.)

All the analysis, observation and comments are documented within the Python notebook itself.

# Results

We observe that the top 8 most important characteristics associated with income are :

<img src="../results-images/screenshots/shap.png?raw=true" width="500" description="SHAP Importance Scores"/>

We then look at Partial Dependency plots for the top features.

### Weeks Worked in a Year

<img src="../results-images/screenshots/weeks%20pdp.png?raw=true" width="250"/>

### Age

<img src="../results-images/screenshots/age%20pdp.png?raw=true" width="250"/>

### Education

<img src="../results-images/screenshots/education%20pdp.png?raw=true" width="250"/>

### Sex

<img src="../results-images/screenshots/sex%20pdp.png?raw=true" width="250"/>

### Occupation

<img src="../results-images/screenshots/occupation%20pdp.png?raw=true" width="250"/>

