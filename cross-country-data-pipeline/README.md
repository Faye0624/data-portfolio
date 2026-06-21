# Cross-country data pipeline & predictive modeling

An end-to-end pandas pipeline over four longitudinal global datasets — child
mortality, CO₂ per capita, GDP per capita, and inflation-adjusted daily income —
spanning 190+ countries from 1800 to 2020.

## What it does
- **Clean:** replace missing/invalid values (NaN, zero, negative) with the next
  valid year *within each country* (back-fill); drop countries absent from any
  dataset so the panel stays consistent across sources.
- **Join & analyse:** for each country, find the first year GDP recovered to 90%
  of its 2010 level, then report the cross-country mean.
- **Model:** train a per-country `LinearRegression` (every 5th year, 1800–2010)
  predicting child mortality from GDP; rank countries by 2020 prediction error.
- **Critique:** diagnose why some 2020 predictions go *negative* — GDP↔mortality
  is non-linear, so a straight line extrapolates the historical steep decline
  past zero. Proposed fix: log-transform GDP before fitting.

## Stack
Python, pandas, NumPy, scikit-learn.

## Files
- `cross_country_pipeline.ipynb` — the notebook (load → clean → join → model → critique).
