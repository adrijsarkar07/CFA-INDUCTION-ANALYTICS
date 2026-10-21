# Five induction reflections

## 1. Which variables or patterns were most associated with PM2.5?

Among individual numeric weather variables, cumulative wind had the strongest negative Pearson association (-0.264), while dew point had a positive association (+0.245). Group ablation identified temperature, dew point and estimated humidity as the most consequential retained group; removing it raised validation RMSE by 13.572 µg/m³. Calendar effects also mattered, but correlated inputs make standalone feature rankings difficult to interpret causally.

## 2. Which model performed best, and why was it selected?

The Random Forest with 200 trees, `max_features=0.5` and `min_samples_leaf=20` had the lowest 2013 validation RMSE, 71.889 µg/m³. It subsequently had the lowest 2014 test RMSE, 66.695 µg/m³, compared with 71.240 for clipped Linear Regression and 73.454 for the Decision Tree. Flexible interactions and averaging across trees are plausible explanations for the improvement, but a single validation year does not establish universal superiority.

## 3. What did residual analysis reveal?

Residuals are defined as actual minus predicted, so positive values indicate underprediction. Error spread increased at higher predicted concentrations, and hours with actual PM2.5 above 250 µg/m³ contributed 50.5% of test squared error despite representing only 7.7% of hours. The small overall mean residual of +1.61 hides substantial errors in opposite directions, including underprediction in February and overprediction in June.

## 4. How did missing values and outlier handling affect the analysis?

The 2,067 missing target observations were excluded instead of being replaced with artificial labels. Missingness varies by month, so results describe observed hours and may be affected by selection bias. IQR and Z-score rules flagged 797 and 422 training PM2.5 values respectively; plausible extremes were retained to avoid excluding severe episodes. Cumulative wind was log-transformed to compress its right tail. Input preprocessing was fitted only on training data; the supplied inputs themselves had no missing values.

## 5. What is a key limitation, and how could it be addressed?

Same-hour weather cannot fully describe unmeasured emissions or recent pollution accumulation, and the weather station differs from the pollution-monitoring location. A future experiment could add carefully aligned historical weather or pollution information, if available at prediction time, and assess it using multiple chronological folds plus a new untouched evaluation period. Such an extension must define its forecasting horizon explicitly and build lags on the complete hourly timeline rather than the target-filtered table.
