## Model Comparison & Evaluation Notebook

### Complete Workflow (12 cells)

**1. Setup** → Import metrics and visualization libraries

**2. Load Predictions** → Reads predictions from all 3 models (Logistic Regression, Random Forest, XGBoost)

**3. Calculate Classification Metrics**
   - **Accuracy** - Overall correctness
   - **Precision** - Positive prediction accuracy (Macro & Weighted)
   - **Recall** - True positive detection rate (Macro & Weighted)
   - **F1-Score** - Harmonic mean of precision/recall (Macro & Weighted)

**4. Comparison Table** → Side-by-side performance view with best model highlighted

**5. Per-Class Performance** → Breaks down metrics for each condition (Critical/Moderate/Normal)

**6. Bar Chart Visualization** → 4 subplots comparing Accuracy, Precision, Recall, F1

**7. Radar Chart** → Multi-dimensional performance visualization

**8. Save Results** → Export comparison tables

**9. Model Ranking** → Ranks models by each metric

**10. Key Insights** → Automated recommendations and analysis

### Classification Metrics Explained

**Accuracy:** (TP + TN) / Total
- Overall correctness percentage
- Good when classes are balanced

**Precision:** TP / (TP + FP)
- "When I predict Critical, how often am I right?"
- Important when false positives are costly

**Recall:** TP / (TP + FN)
- "Of all Critical pipelines, how many did I catch?"
- Important when missing positives is dangerous (safety-critical!)

**F1-Score:** 2 × (Precision × Recall) / (Precision + Recall)
- Balanced metric
- Best for imbalanced datasets

### Macro vs Weighted

**Macro:** Simple average across classes (treats all equal)
**Weighted:** Average weighted by class size (accounts for imbalance)

For pipeline safety, you care about **both** - missing a Critical pipeline is dangerous!

### Output Files (4 total)

1. **model_comparison_metrics.csv** - Complete metrics with macro/weighted
2. **model_comparison_summary.csv** - Clean summary table
3. **model_comparison_metrics.png** - 4 bar charts (Accuracy, Precision, Recall, F1)
4. **model_comparison_radar.png** - Spider/radar chart overlay

### What You'll Learn

✅ **Which model is best overall** (highest accuracy)
✅ **Which model is best per class** (Critical detection rate)
✅ **Performance improvement** (best vs worst model)
✅ **Trade-offs** (speed vs accuracy, simplicity vs performance)
✅ **Deployment recommendation** (which to use in production)

### Expected Results

Typical ranking (for your pipeline data):
1. **XGBoost** - Highest accuracy (90-95%)
2. **Random Forest** - Very close to XGBoost (88-93%)
3. **Logistic Regression** - Good baseline (80-85%)

### Key Features

✅ **Handles missing models** - Works if you only ran 1 or 2 models
✅ **Per-class breakdown** - Shows Critical vs Moderate vs Normal performance
✅ **Visual comparison** - Easy to see performance differences
✅ **Automated insights** - Provides recommendations
✅ **Ranking system** - Ranks models by different priorities

### Usage

```bash
jupyter notebook Model_Comparison.ipynb
```

**Run this AFTER running all 3 model notebooks** (Logistic Regression, Random Forest, XGBoost).
