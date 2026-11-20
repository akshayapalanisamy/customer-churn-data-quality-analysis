# Task 03 – Business KPI Dashboard (EdVyro Data Analytics)

Interactive dashboard for churn, retention, revenue at risk and tenure. Built with plain HTML, CSS and JavaScript (no libraries, no build step). This file is separate from the Task 02 `README.md`, which is left unchanged.

**Dashboard link (after you enable GitHub Pages):** `https://akshayapalanisamy.github.io/customer-churn-data-quality-analysis/`
This link will only work once the steps below are done. It has not been published yet.

## Data source
The dashboard reads **`cleaned_customer_churn.csv`**, the Task 02 cleaned dataset in the root of this repository, directly from the same folder as `index.html`. No second copy of the data exists, and no records are typed into the code. If you update the CSV, the dashboard follows automatically.

It needs these columns: `tenure_months`, `monthly_charges`, `contract_type`, `payment_method`, `churn` (values Yes/No). Header spelling is matched ignoring case, underscores and spaces. The other columns are ignored. If a column is missing or the file can't load, the page shows a clear message instead of a blank chart. A line under the filters reports how many records were loaded.

## KPI definitions
| KPI | Definition |
|---|---|
| Churn rate | Churned customers (churn = Yes) ÷ total customers × 100 |
| Retention rate | Retained customers (churn = No) ÷ total customers × 100 |
| Revenue at risk | Sum of `monthly_charges` where churn = Yes (monthly; no currency is specified in the data) |
| Average tenure | Mean of `tenure_months` for the selected customers |

All four recalculate when any filter changes.

## Features
- Filters: contract type, payment method, minimum and maximum tenure, plus **Reset filters**.
- Visuals, each with a written insight that updates with the filters: churn vs retention, revenue at risk by contract type, churn rate by payment method, tenure distribution.
- Accessible blue/orange palette with text labels, keyboard focus styles, responsive layout.

## Insights
Insights are generated from the filtered data, so they always match what is on screen. Your Task 02 README reports 15 records with 7 churned (46.7%), and all 7 Month-to-Month customers churned. Check that the dashboard's unfiltered view agrees with these. Treat all patterns as descriptive: a 15-record sample cannot represent a wider customer population, groups are very small, and contract type and payment method overlap, so differences are not proof of cause.

Practical actions suggested by the pattern: encourage Month-to-Month customers to move to longer contracts, focus onboarding and check-ins on the early months, and review support experience for customers with many tickets. Test these on larger data before acting.

## Run locally
Browsers block loading a CSV from a double-clicked HTML file. In the repo folder run `python3 -m http.server`, then open http://localhost:8000.

## Upload to your existing repository
1. Unzip the download. You get `index.html` and `README_TASK03.md`.
2. Open https://github.com/akshayapalanisamy/customer-churn-data-quality-analysis, then **Add file → Upload files**.
3. Drag in `index.html` and `README_TASK03.md` only. Do not upload a CSV or README.md: `cleaned_customer_churn.csv` and your Task 02 README are already there.
4. Choose "Commit directly to the main branch" and click **Commit changes**.

## Enable GitHub Pages
1. In the repo, open **Settings → Pages**.
2. Under "Build and deployment", set Source to **Deploy from a branch**, Branch **main**, folder **/ (root)**, then **Save**.
3. Wait 1–2 minutes and refresh. GitHub shows "Your site is live at …".
4. Open that link and confirm: the line under the filters says 15 records loaded, the KPI cards show values, and each filter and Reset change the charts.
5. Submit that link to EdVyro. The repo link also works, since this README explains the work.

## Requirement checklist
- [x] KPIs defined (on the dashboard and above)
- [x] Filters: contract, tenure, payment method, plus reset
- [x] Appropriate, labelled charts with accessible colours
- [x] Explanation in the same repository
- [x] Written insight beside every visual
- [ ] Published link: not done until you enable Pages and verify it
