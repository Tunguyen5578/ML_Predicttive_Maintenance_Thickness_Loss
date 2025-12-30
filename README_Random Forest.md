## Random Forest Notebook

### Complete Workflow (13 cells)

**1. Setup** → Import libraries (sklearn ensemble, metrics, visualization)

**2. Load Data** → Loads X_train, X_test, y_train, y_test from CSV files

**3. Train Model** → Random Forest with 100 trees, optimized settings

**4. Make Predictions** → Predictions + probability scores for all classes

**5. Evaluate Performance**
   - Training accuracy
   - Test accuracy
   - Overfitting check
   - Full classification report

**6. Confusion Matrix** → Green heatmap showing prediction patterns

**7. Feature Importance**
   - Ranks all features by importance
   - Shows top 15 most influential features
   - Visual bar chart (green gradient)
   - Saves full ranking to CSV

**8. Model Information** → Configuration details and parameters

**9. Save Results** → CSV files with metrics and predictions

### Key Advantages Over Logistic Regression

✅ **No scaling needed** - Tree-based models work with raw values
✅ **Better accuracy** - Usually outperforms linear models
✅ **Handles outliers** - Not sensitive to extreme values (you have 70 outliers!)
✅ **Non-linear relationships** - Captures complex patterns
✅ **Feature importance** - Shows which features matter most
✅ **Robust** - Works well with minimal tuning

### Model Configuration

- **Number of trees:** 100 (good balance of speed/accuracy)
- **Max depth:** None (trees grow until pure)
- **Min samples split:** 2 (default)
- **Random state:** 42 (reproducible)
- **Parallel processing:** Uses all CPU cores (n_jobs=-1)

### Output Files (5 total)

1. **confusion_matrix_random_forest.png** - Visual confusion matrix (green theme)
2. **feature_importance_plot_random_forest.png** - Top 15 features bar chart
3. **feature_importance_random_forest.csv** - Complete feature ranking
4. **random_forest_results.csv** - Performance summary
5. **random_forest_predictions.csv** - All predictions with probabilities

### Feature Importance Insights

You'll discover:
- Which engineered features are most valuable
- Whether rate features beat absolute values
- If ratios or interactions matter most
- Which original features still dominate

### Expected Performance

Random Forest typically achieves:
- **Higher accuracy** than Logistic Regression
- **Better recall** for minority classes (Critical/Moderate)
- **Less overfitting** than single decision trees
- **More stable predictions**

### Usage

```bash
jupyter notebook Random_Forest.ipynb
```


This should significantly outperform Logistic Regression on your pipeline data.

[1](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/144370361/a4cd1882-3337-4a86-82c5-a9f15ba45fa1/thickness_loss_dataset.csv)
