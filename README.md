# Fruit Type Classifier

## Project Description
This project is a comparative analysis between Logistic Regression and Decision Tree models applied to a classification task. The dataset used in this project was carefully preprocessed, and the models were trained, tested, and evaluated to determine their performance. Special attention was given to the impact of hyperparameter tuning on the Decision Tree model's effectiveness.


## Methodology

1. **Data Loading**: The dataset was loaded into a Pandas DataFrame for preprocessing and analysis.
2. **Data Cleaning**: The dataset checked for missing values and outliers.
3. **Feature Scaling**: The numerical features were scaled using `StandardScaler` to standardize the dataset, ensuring that all features contribute equally to the model training.
4. **Data Splitting**: The dataset was split into 75% training data and 25% test data to evaluate the models' performance on unseen data.
5. **Model Training**: The models were trained on the prepared dataset, and the results were calculated.

### Model Development
1. **Logistic Regression**:
   - A Logistic Regression model was trained using the scaled training data.
   - The model's performance was evaluated using accuracy and weighted F1-score, which considers both precision and recall across all classes, making it suitable for datasets with class imbalance.

2. **Decision Tree with Hyperparameter Tuning**:
   - A Decision Tree model was trained, and hyperparameters such as `criterion`, `max_depth`, `min_samples_split`, and `min_samples_leaf` were optimized using Grid Search with 5-fold cross-validation.
   - The optimized model was then evaluated on the test data using the same metrics as the Logistic Regression model.

## Results


Model Scores:

| Model | Test Accuracy | Score |
|----------|----------|----------|
| Logistic Regression | 0.78 | 0.78 |
| Decision Tree | 0.82 | 0.82 |

### Logistic Regression
The Logistic Regression model provided a balanced performance with a weighted F1-score indicating a reasonable balance between precision and recall across different classes.

### Decision Tree
- **Best Hyperparameters**:
  - `criterion`: 'entropy'
  - `max_depth`: 10
  - `min_samples_leaf`: 1
  - `min_samples_split`: 10

The Decision Tree model, after hyperparameter tuning, outperformed the Logistic Regression model in both accuracy and F1-score. This demonstrates the importance of hyperparameter tuning in enhancing model performance.

## Conclusion
It can be concluded that the limited amount of data (input features) provided restricts the ability to improve the accuracy of the models. With a larger volume of data, it may be possible to further optimize the model's performance.

This study reveals that while Logistic Regression offers a strong baseline performance, a Decision Tree model with optimized hyperparameters can achieve superior results. The study underscores the importance of hyperparameter tuning in machine learning models, particularly for decision trees.
