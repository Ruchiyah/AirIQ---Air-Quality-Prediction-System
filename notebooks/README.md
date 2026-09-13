# Notebooks — Data-Mining Pipeline (Phases 00–12)

These notebooks rebuild the AirIQ model from the original UCI dataset in
[`../PRSA_Data_20130301-20170228/`](../PRSA_Data_20130301-20170228/).

## Setup

From the repository root:

```bash
source .venv/bin/activate          # Windows: .venv\Scripts\Activate.ps1
pip install -r requirements.txt jupyter matplotlib
jupyter notebook notebooks/
```

Run the notebooks **in order** (`00` → `12`); each one reads the previous phase's output.
Paths come from [`../src/project_config.py`](../src/project_config.py), and the
project root is detected automatically.

## Outputs

All generated files go to `data/` at the repository root, which is git-ignored:

| Folder | Contents |
|---|---|
| `data/raw`, `data/interim` | Integrated dataset, dataset with next-hour target |
| `data/processed`, `data/features` | Preprocessing stages, engineered features |
| `data/splits` | Walk-forward folds + 2017 final test set |
| `data/eda`, `data/audit`, `data/results` | Summaries, model results, final model |

Notebook 12 saves the trained pipeline to `data/results/final_pm25_pipeline.joblib`.
Copy it to `backend/model/` to use it in the app.

> `00_dataset_integration.ipynb` was reconstructed for this repository; the original
> was not included in the submission. Its outputs were verified to be byte-identical to
> the team's original Phase 0 outputs.
