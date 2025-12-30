Logistic Regression Notebook

Complete Workflow (14 cells)

1. Setup → Import libraries (sklearn, pandas, matplotlib, seaborn)

2. Load Data → Loads X_train, X_test, y_train, y_test from CSV files

3. Feature Scaling → StandardScaler (important for Logistic Regression)

4. Train Model → Logistic Regression with One-vs-Rest multi-class strategy

5. Make Predictions → Both predictions and probability scores

6. Evaluate Performance

Training accuracy

Test accuracy

Overfitting check

Full classification report (precision, recall, F1-score)

7. Confusion Matrix → Visual heatmap showing prediction errors

8. Feature Analysis

Coefficient values for each class

Top 10 most important features

Visualization of positive/negative influences

9. Save Results → CSV files with metrics and predictions

Key Features
✅ Proper scaling - Uses StandardScaler (required for Logistic Regression)
✅ Multi-class support - One-vs-Rest for 3 classes
✅ Interpretability - Shows which features influence each class
✅ Complete metrics - Accuracy, precision, recall, F1-score per class
✅ Visual outputs - Confusion matrix and coefficient plots
✅ Probability scores - Shows prediction confidence

Model Configuration
Algorithm: Logistic Regression (One-vs-Rest)

Solver: LBFGS (efficient for multi-class)

Max iterations: 1000

Random state: 42 (reproducible)

Scaling: StandardScaler (mean=0, std=1)

Output Files (4 total)
confusion_matrix_logistic_regression.png - Visual confusion matrix

feature_coefficients_logistic_regression.png - Top features per class

logistic_regression_results.csv - Performance summary

logistic_regression_predictions.csv - All predictions with probabilities

What You'll Learn
Which features increase/decrease each class probability

Model accuracy and per-class performance

Where the model makes mistakes (confusion matrix)

Prediction confidence (probability scores)


Run all cells → Get complete baseline results!

This gives us a solid baseline to compare Random Forest and XGBoost against.
