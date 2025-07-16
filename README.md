# Term Deposit Classifier

This project develops and compares multiple classification models to predict whether a bank client will subscribe to a term deposit product, using data from a Portuguese bank’s marketing campaigns.

## Objective

- Build accurate classification models to target high-probability clients
- Improve campaign efficiency and term deposit subscription rates

## Dataset

- Source: Portuguese bank direct marketing dataset (UCI)
- 45,211 observations, 16 predictors (10 categorical, 6 numeric)
- Target variable: `is_subscription` (binary)

## Data Processing

- Imputation for missing categorical values (mode)
- Yeo-Johnson transformations on numeric variables
- Day variable consolidated using profit-driven decision tree
- Variable importance assessed with t-/chi-square tests and ROC

## Models Compared

| Model                | F-Score | AUC    |
|----------------------|---------|--------|
| Decision Tree        | 0.536   | 0.875  |
| Logistic Regression  | 0.533   | 0.913  |
| Artificial Neural Net| 0.578   | 0.922  |
| Random Forest        | **0.580**   | **0.931**  |

Random Forest emerged as the best performer and was further enhanced with oversampling and hybrid balancing techniques.

## Best Performing Model

- **Random Forest with Both Oversampling**:
  - **F-Score:** 0.6055
  - **AUC:** 0.9284
  - Identified 89.92% of clients who subscribed
- **Top Features**: Duration of last call, Month contacted

## Skills Demonstrated

- R: `caret`, `randomForest`, `nnet`, `ROSE`
- Data wrangling, transformation, imputation
- Classification, model comparison, performance tuning
- Handling class imbalance (under/over/both/ROSE)
- ROC, AUC, F-score optimization

## Files

- `code/` – RMarkdown file with preprocessing, modeling, and evaluation
- `data/` – CSV data file
- `report/` – Final PDF summary report

## Future Considerations

- Hyperparameter tuning for Random Forest
- Explore SMOTE for categorical data
- Add interaction terms and ensemble blending

