5-Fold Cross-Validation Notebook
Complete Workflow (15 cells)
1. Setup → Import CV libraries and models

2. Load Data → Combines train + test for proper cross-validation

3. Define Models → Initializes all 3 models (LR, RF, XGBoost)

4. Setup CV → Stratified K-Fold (5 splits, maintains class balance)

5. Perform Cross-Validation → Runs 5-fold CV for all models

6. Results Summary → Shows mean ± std for all metrics

7. Fold-by-Fold Details → Individual fold scores

8-10. Visualizations:

Box plots (distribution across folds)

Bar charts with error bars

Line plots (fold-by-fold trends)

11. Statistical Analysis → 95% confidence intervals

12. Save Results → Export comprehensive CSV files

13. Recommendations → Automated insights and next steps

Why Cross-Validation?
Problem with single train/test split:

Results depend on random split

May get lucky or unlucky with split

Not representative of true performance

5-Fold CV solution:

Uses ALL data for training and testing

Each sample tested exactly once

Average across 5 runs = robust estimate

Standard deviation shows stability

Stratified K-Fold
Maintains class distribution in each fold

If you have 40% Critical, 30% Moderate, 30% Normal overall

Each fold has same proportions

Important for imbalanced datasets

Metrics Calculated
For each model, each fold:

Accuracy

Precision (macro)

Recall (macro)

F1-Score (macro)

Summary statistics:

Mean (average across 5 folds)

Std (variance/stability)

95% Confidence Interval

Output Files (6 total)
cross_validation_results.csv - Summary (mean ± std)

cross_validation_folds.csv - Accuracy per fold

cross_validation_detailed.csv - All metrics, all folds

cross_validation_boxplots.png - Distribution visualization

cross_validation_comparison.png - Bar chart with error bars

cross_validation_folds.png - Line plot across folds

What You'll Learn
✅ True model performance (not just lucky split)
✅ Model stability (low std = consistent, high std = unstable)
✅ Statistical confidence (95% CI shows reliability)
✅ Best model (highest mean accuracy with low variance)
✅ Overfitting detection (high variance = overfitting)

Interpreting Results
Good result:

Mean accuracy: 0.92 ± 0.02

Interpretation: 92% accurate, very stable (±2%)

Concerning result:

Mean accuracy: 0.85 ± 0.12

Interpretation: 85% accurate but unstable (varies 73-97%)

Expected Rankings
Based on your pipeline data:

XGBoost: ~93% ± 0.02 (best + most stable)

Random Forest: ~91% ± 0.03 (very close)

Logistic Regression: ~84% ± 0.04 (good baseline)

Special Handling
Logistic Regression:

Uses Pipeline with StandardScaler

Scaling applied within each fold (prevents data leakage)

Random Forest & XGBoost:

No scaling needed (tree-based)

Direct cross-validation

Key Features
✅ No data leakage - Scaling/preprocessing done per fold
✅ Fair comparison - All models tested on same folds
✅ Comprehensive metrics - Multiple evaluation criteria
✅ Visual insights - Easy to spot differences
✅ Statistical rigor - Confidence intervals included
