# Model file

The backend loads `final_pm25_pipeline.joblib` from this folder at startup.

The file is ~840 MB, which is over GitHub's 100 MB limit, so it is **not stored in git**.
Download it from the repository's **Releases** page and place it here:

```text
backend/model/final_pm25_pipeline.joblib
```

The pipeline was saved with **scikit-learn 1.9.1** and imports `src.modeling_utils`,
so run the backend from the repository root with the pinned `requirements.txt` installed.
