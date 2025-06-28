# Volatility–Spillover Project  
_Australia replication ➜ Portugal / France / Spain extension_

---

## Workflow (high-level)

| Step | What happens | Code status |
|------|--------------|-------------|
| **01  Create time-series** | Pull raw intraday prices → daily panel (`YYYY-MM-DD × contracts`). | `notebooks/01_create_time_series.ipynb` |
| **02  Realised vol + PIT** | Compute realised variances & covariances, run micro-structure tests, apply PIT transformation | `02_compute_realized_volatilities.ipynb` |
| **03  Spillovers – ReVar** | Static and rolling 365-day MHAR-ReVar (diagonal only) with LASSO | `03_volatility_spillovers_var.ipynb` |
| **04  Spillovers – ReCov** | Same but full vech| same module,  `04_volatility_spillovers_var_covar_MHAR.ipynb` |
| **05  Next: transformer-based transmission estimator** | Replace LASSO + linear Φ with a sequence-to-sequence **Transformer** | **to-do** – prototype in `transformer_gvd_estimator.ipynb`. |

---

[Francisco Rolotti](https://www.linkedin.com/in/francisco-rolotti/)
