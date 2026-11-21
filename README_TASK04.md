# EdVyro Task 04 — Segmentation and Recommendation Model

## Deliverables
- `task04_segmentation_analysis.ipynb` — analysis, scoring, descriptive validation, chart and edge-case tests.
- `customer_churn_sample.csv` — supplied dataset.
- `customer_segments_and_risk_scores.csv` — customer score, segment, point breakdown and explanation.
- `segment_summary.csv` — segment-level metrics.
- `risk_tier_validation.csv` — descriptive comparison with observed churn.
- `edge_case_validation.csv` — boundary and invalid-input tests.
- `recommendation_memo.md` and `recommendation_memo.pdf` — business memo.

## Rules
Month-to-Month contract +3; tenure <=12 months +2; support tickets >=4 +2; monthly charges >= INR 80 +1. Maximum 8. Low 0–2, Medium 3–4, High 5–8.

The `Churn` label is excluded from score calculation. This is a prioritisation heuristic, not a trained model or probability.

## Run
Keep the notebook and CSV together. Install `pandas`, `numpy`, `matplotlib`, and `jupyter`; open the notebook in Jupyter or Google Colab and run all cells.

## Limitations
Only 15 synthetic records. Weights are heuristic and observed alignment is in-sample. Do not claim general predictive accuracy or causation.
