# Post-Restructuring Talent Impact Simulator

A Python-based workforce planning tool that models the capability impact of
a corporate restructuring event and compares three recovery strategies:
full rehire, upskilling, and internal redistribution.

## What it does
- Calculates a Capability Loss Index (CLI) per department, identifying
  where critical/high-priority skills were disproportionately lost
- Maps at-risk skill exposure in the retained workforce using performance
  and tenure proxies
- Runs a cost-benefit comparison of three recovery strategies
- Outputs a Power BI dashboard and a consulting-style report

## Key finding
No department crossed the 30% high-loss threshold, but Product (27.2% CLI)
and Engineering (23.4% CLI) sustained moderate capability loss. A separate
risk signal — 42 at-risk active employees, concentrated in Finance and
Sales — does not track the same departments as the capability loss,
suggesting a second, independent exposure beyond the restructuring itself.

## Tools used
Python (pandas, numpy, matplotlib, seaborn, faker) · Jupyter Notebook ·
Power BI · HTML/PDF reporting

## How to run
1. Clone the repo
2. Open `notebooks/talent_simulator.ipynb` in Jupyter
3. Run all cells in order — this regenerates the dataset, all three charts,
   and the Excel export
4. Open `outputs/talent_simulator_output.xlsx` in Power BI, or open the
   provided `.pbix` directly

## Dataset
Synthetic — generated using Faker (seed 42) to reflect realistic HR
distributions across 5 departments, 300 employees, with a probabilistic
layoff rule weighted by performance and tenure.

## Report
See `report/Post-Restructuring_Talent_Impact_Assessment.pdf` for the full
5-page consulting-style writeup, including methodology, findings, and
prioritised recommendations.
