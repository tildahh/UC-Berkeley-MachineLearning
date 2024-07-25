# Wage Prediction Using Ensemble Regression Models

This project aims to predict the hourly wage of individuals using various regression models and an ensemble method. The dataset contains census information, and the primary goal is to compare the performance of individual regression models against an ensemble model.

## Dataset and Task

The dataset used in this project contains information on individuals and their hourly wages. Key features include education, experience, age, occupation, sector, and other demographic variables. The task is to predict the `WAGE` column using these features.

## Models Evaluated

1. **Linear Regression**
2. **Ridge Regression**
3. **K-Nearest Neighbors Regressor**
4. **Decision Tree Regressor**
5. **Support Vector Regressor (SVR)**
6. **Transformed Target Regressor (with Linear Regression)**
7. **Voting Regressor (Ensemble of the above models)**

## Results

The performance of each model was evaluated using Mean Squared Error (MSE) and R² Score. Here are the key findings:

- **Linear Regression** and **Ridge Regression** models performed the best with moderate MSE and R² scores, indicating they capture some patterns in the data but not all.
- **K-Nearest Neighbors Regressor** had a higher MSE and a lower R² score, suggesting it is less effective in predicting wages.
- **Decision Tree Regressor** performed poorly with the highest MSE and a negative R² score, likely due to overfitting.
- **Support Vector Regressor (SVR)** also showed high MSE and low R² scores, suggesting it is not well-suited for this dataset.
- **Transformed Target Regressor** performed similarly to Linear Regression, showing moderate effectiveness.
- **Voting Regressor (Ensemble Model)** showed a moderate improvement over individual models like K-Nearest Neighbors and Decision Tree but did not outperform Linear Regression or Ridge Regression.

### Mean Squared Error (MSE) and R² Score of Models

![MSE and R² Score of Models](https://github.com/tildahh/UC-Berkley-MachineLearning/blob/main/M21-Ensemble-Techniques/images/mse_r2_plot.png.png)

## Feature Importance

The feature importance from the Decision Tree Regressor highlighted the following key factors influencing wage predictions:

- **EXPERIENCE**: Most important feature, significantly impacting wage predictions.
- **EDUCATION**: Highly important, indicating education level is a key factor in wage determination.
- **AGE**: Another crucial feature, likely correlated with experience and overall career progression.

![Feature Importance](https://github.com/tildahh/UC-Berkley-MachineLearning/blob/main/M21-Ensemble-Techniques/images/feature_importance_plot.png)

## Conclusions

- The ensemble model (Voting Regressor) did not significantly outperform the best individual models (Linear Regression and Ridge Regression), suggesting that a simple linear approach is quite effective for this dataset.
- Key factors influencing wage predictions are experience, education, and age. These should be focused on when interpreting model results and making decisions based on these predictions.

## Next Steps

- Consider tuning hyperparameters of the models, especially the ensemble model, to potentially improve performance.
- Explore additional models or more advanced ensemble methods.
- Perform cross-validation to ensure the model results are consistent and not due to overfitting on the training data.

## Requirements

- Python 3.x
- numpy
- pandas
- matplotlib
- scikit-learn

## How to Run

1. Ensure all required packages are installed.
2. Load the dataset and preprocess it as described.
3. Run the notebook or script to train and evaluate the models.
4. Visualize the results to compare model performance and interpret feature importance.

