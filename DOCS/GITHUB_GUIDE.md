# Publish CFA-INDUCTION-ANALYTICS

## Repository details

Name: `CFA-INDUCTION-ANALYTICS`

Description: `AirCast: PM2.5 regression with chronological validation, feature engineering and error analysis | CFA Club, IIT Indore.`

Suggested topics: `air-quality`, `regression`, `random-forest`, `scikit-learn`, `data-analysis`, `jupyter-notebook`.

## Upload using the GitHub website

1. Extract the supplied ZIP. Open the inner `CFA-INDUCTION-ANALYTICS` folder; its top level contains `README.md` and `aircast.ipynb`.
2. On GitHub, choose **New repository**, enter the name above, and select visibility consistent with the submission instructions. A private repository needs reviewer access.
3. Create it without generating another README. The package already supplies its own README and `.gitignore`.
4. Use **uploading an existing file** on an empty repository, or **Add file → Upload files** on an existing one. Drag the contents of the extracted folder, preserving subfolders. Upload the contents, not only the ZIP and not an extra enclosing project folder.
5. Commit with `Add AirCast notebook, results and technical documentation`.
6. Check the README images and links, notebook rendering, three CSVs and six-page PDF. Confirm the submission reviewers can access the repository.

The browser supports up to 100 files at a time and 25 MiB per file; this package is within those limits. Never replace required PNGs with JPG copies alone.

## Folder structure

| Folder | Files |
|---|---|
| `/` | `README.md`, `aircast.ipynb`, `requirements.txt`, `.gitignore`, `model_comparison.csv`, `model_comparison_final.csv`, `ablation_validation.csv` |
| `/data/` | `README.md` (dataset source and dictionary) |
| `/docs/` | `METHODOLOGY.md`, `RESULTS.md`, `REFLECTIONS.md`, `REPRODUCIBILITY.md`, `SOURCES.md`, `DELIVERABLES.md`, `GITHUB_GUIDE.md` |
| `/reports/` | `AirCast_Technical_Report.pdf` |
| `/figures/` | `pm25_distribution.png`, `pm25_boxplot.png`, `pm25_over_time.png`, `correlation_heatmap.png`, `feature_scatterplots.png`, `actual_vs_predicted.png`, `residual_plot.png`, `permutation_importance.png` |
| `/figures/jpg/` | Same eight figure names with `.jpg` extensions |

Housing, MNIST, Anscombe and the sample-data README were intentionally excluded. They remain unrelated to the Beijing pollution analysis.

References: [Create a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository); [upload files](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository).
