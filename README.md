# whoop

NYU Data Bootcamp Spring 2026 final project.

Eight months of my own WHOOP data, a few course-aligned models, and one honest forward-looking forecast at the end: what's tomorrow's Recovery going to be?

## what's in here

- `Onat_Whoop_EDA.ipynb` — exploratory data analysis: distributions, time series, ACF/PACF, day-of-week patterns, correlations.
- `Whoop_Modeling_Onat.ipynb` — the modeling: train/test split, baseline, AR(7), Ridge AR + exogenous, KNN, logistic regression, KMeans clustering, walk-forward forecast, and the next-day prediction.
- `Whoop_Final_Presentation.pptx` — 20-slide deck.
- `Whoop Write-Up (1).pdf` — executive summary write-up.
- `presentation video link` — file with the link to the recorded presentation.
- raw CSVs (`physiological_cycles`, `sleeps`, `workouts`, `journal_entries`) plus the joined `whoop_modeling_frame.csv`.

## how to run

Open either notebook in Google Colab, upload the four CSVs to `/content/data/`, run all cells. The setup cell will pip install statsmodels if needed. That's it.

## headline numbers

- Ridge AR + exogenous wins the regression task: RMSE 20.05, R^2 0.33 on a 46-day held-out test set.
- Walk-forward (retrain every day) bumps it to RMSE 19.26, R^2 0.38.
- Logistic regression on Recovery zones: 54% vs 41% always-Yellow baseline.
- Genuine next-day prediction for 2026-05-13: 58.4% Recovery, Yellow zone.
