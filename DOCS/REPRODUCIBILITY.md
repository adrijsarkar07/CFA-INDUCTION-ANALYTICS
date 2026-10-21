# Reproduction and verification

## Run locally

Install Python 3 and open a terminal in the extracted repository folder. An isolated environment is optional but recommended.

```bash
python -m venv .venv
```

Windows PowerShell activation:

```powershell
.venv\Scripts\Activate.ps1
```

macOS / Linux activation:

```bash
source .venv/bin/activate
```

Then install and launch:

```bash
python -m pip install -r requirements.txt
jupyter lab aircast.ipynb
```

Restart the kernel and run all cells in order. Open the notebook from the repository root so its existing relative paths place figures and CSVs in the documented locations. The UCI download and first-cell package installation need network access.

## Google Colab

Upload `aircast.ipynb`, install missing dependencies using `requirements.txt` (or the same package names), and run all cells. Download the three output CSVs and the `figures` folder afterwards. Colab's housing, MNIST and Anscombe sample files are not project outputs.

## What has been checked in this package

- Latest notebook and AirCast CSV attachments match the earlier supplied versions.
- Notebook JSON structure and Python-cell syntax were checked. Executable cells, execution counts and outputs were preserved by the documentation edit.
- All four test rows agree between the all-splits and final comparison CSVs. Squared RMSE agrees with MSE within displayed rounding tolerance.
- Eight plots were recovered from saved notebook outputs. The PNGs preserve their embedded pixels and carry 150-dpi metadata; JPG copies are included for viewing. A rerun regenerates the notebook's original `savefig(..., dpi=150)` exports at their configured size.
- The report is based on supplied outputs; the documentation pass did not refit models or independently reproduce the scores.

## Remaining reproducibility limits

The original Python and package versions were not captured, and the dependencies are therefore unpinned. For a release that you have rerun successfully, record `python --version` and `python -m pip freeze` in an environment record; do not describe the present dependency list as a tested lockfile. No raw data snapshot is bundled; the current loader retrieves UCI ID 381 online. The report and Markdown summaries do not automatically refresh if you later rerun with changed models or data.

The three uploaded CSVs are rounded to three decimals. Very small differences on rerun can reflect software versions or numeric rounding. New performance changes after viewing 2014 results require a new untouched evaluation period rather than continued selection on the same test set.
