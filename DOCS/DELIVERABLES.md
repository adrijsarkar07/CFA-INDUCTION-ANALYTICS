# Induction deliverables

| Deliverable | Location | Status / scope |
|---|---|---|
| D1: single notebook | `aircast.ipynb` | Code, saved outputs and corrected explanations included; clean-kernel rerun remains to be confirmed |
| D2: saved PNG visualisations | `figures/` | Seven required plots plus permutation importance; JPG viewing copies in `figures/jpg/` |
| D3: model comparison | `model_comparison_final.csv` and report | Linear Regression, Decision Tree, Random Forest and mean baseline |
| D4: feature engineering | Notebook and `docs/METHODOLOGY.md` | Seven engineered columns across five feature groups |
| D5: five reflections | Notebook and `docs/REFLECTIONS.md` | Associations, model choice, residuals, missingness/outliers and limitations |
| D6: analysis report | `reports/AirCast_Technical_Report.pdf` | Six pages with selected plots and comparison table |

The project also includes manual validation-based hyperparameter comparisons, grouped permutation importance, feature-group ablation, and high-pollution error analysis. It does not claim rolling cross-validation, GridSearchCV, Ridge/Lasso or tested lagged features.

## Correction record

The documented minimum hourly mean is 15:00 (84.9), not 16:00 (85.0). The 980 µg/m³ event is at 2010-02-14 01:00; 02:00 is missing. Explanations of outages, measurement inconsistencies and atmospheric mechanisms are treated as hypotheses. Raw versus clipped Linear Regression scores, the R² baseline, model input columns, and the test-specific prediction maximum are clarified. The missing-values/outliers reflection and assistance disclosure are explicit.
