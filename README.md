# Diamond-Price-Prediction

## Project Overview

The **Diamond Price Prediction** project uses machine learning models to analyze a dataset of over 53,000 diamonds. The dataset contains features such as carat, cut, clarity, and color, which are used to build models to accurately predict the price of diamonds. 

### 1. **Data Cleaning and Preprocessing**
- Removed outliers based on `depth` and `table` measurements (7 records removed).
- Handled missing values and converted categorical variables (cut, color, clarity) into ordered variables.
- High correlations between physical dimensions (x, y, z) and carat were identified, leading to their removal to prevent multicollinearity issues.

### 2. **Exploratory Data Analysis (EDA)**
- **Univariate Analysis**: Analysis of individual features to understand their distribution (e.g., carat, cut, clarity).
- **Bivariate Analysis**: Examined relationships between features such as the strong positive correlation between carat weight and price.
- Identified `Ideal` cut, `G` color, and `SI1` clarity as the most frequent diamond attributes.

### 3. **Modeling and Results**
The dataset was split into 70% training and 30% testing. Several models were tested, including:

- **Random Forest Regressor**
- **Gradient Boosting Regressor**
- **XGBoost**
- **LightGBM** (Best-performing model)

**Performance Metrics**:
- Best model: **LightGBM**
  - Train R-squared: 98.58%
  - Test R-squared: 98.27%
  - Hyperparameters: `{'learning_rate': 0.1, 'max_depth': 6, 'n_estimators': 150, 'num_leaves': 63}`

### 4. **Business Insights**
- **Market Segmentation**: Identified distinct segments based on carat weight, cut, and clarity, helping with targeted pricing strategies.
- **Price Sensitivity**: Pricing strategies can be optimized by recognizing attributes that command higher premiums (e.g., carat).
- **Supply Chain Optimization**: Predicting price trends can help optimize the supply chain and streamline operations.

## Technologies Used
- **Languages**: Python
- **Libraries**:
  - `pandas`, `numpy` for data manipulation.
  - `matplotlib`, `seaborn` for visualization.
  - `sklearn`, `xgboost`, `lightgbm`, `catboost` for modeling.
  - `GridSearchCV` for hyperparameter tuning.

## Limitations and Future Work
- The dataset does not distinguish between natural and synthetic diamonds, affecting prediction accuracy.
- Absence of certification information (e.g., GIA, IGI), which could further refine pricing models.
- Future work could explore the impact of diamond origin and certification on pricing accuracy.
