# Sources and assistance

## Data and domain references

1. Chen, S. (2015). *Beijing PM2.5*. UCI Machine Learning Repository. [DOI 10.24432/C5JS49](https://doi.org/10.24432/C5JS49). Dataset ID 381, CC BY 4.0.
2. Liang et al. (2015). *Assessing Beijing's PM2.5 pollution: severity, weather impact, APEC and winter heating*. Proceedings of the Royal Society A, 471, 20150257. [DOI 10.1098/rspa.2015.0257](https://doi.org/10.1098/rspa.2015.0257).
3. Alduchov and Eskridge (1996). *Improved Magnus Form Approximation of Saturation Vapor Pressure*. Journal of Applied Meteorology, 35, 601–609. The notebook uses constants 17.625 and 243.04 to construct an approximate humidity feature from temperature and dew point.

## Software documentation

- [Scikit-learn: Common pitfalls and recommended practices](https://scikit-learn.org/stable/common_pitfalls.html).
- [Scikit-learn: RandomForestRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html).
- [Scikit-learn: R² score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html).
- [Scikit-learn: Model evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html).

## Evidence for reported numbers

The supplied `aircast (1)(5).ipynb`, `model_comparison(2).csv`, `model_comparison_final(2).csv`, and `ablation_validation(2).csv` are the source of the numerical results. Their repository filenames are simplified; CSV contents are unchanged. Documentation corrections do not constitute an independent training rerun.

## AI assistance

The original notebook discloses Gemini assistance with pipeline structure, grouped permutation/ablation design and documentation formatting. ChatGPT assisted with coding discussions, interpretation, review of saved outputs, corrections to explanatory text and preparation of the README, report and repository documentation. No new fitted results were invented or presented as independently reproduced. The author is responsible for understanding the implementation, checking the analysis and completing the final reproducibility run.
