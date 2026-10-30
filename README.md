# ComAgent-Wireless-Optimization

Simulation-based wireless resource allocation research with reliability, throughput, and fairness evaluation, accompanied by an interactive web dashboard.

## Repository Structure

- `ComAgent_Wireless_Research.ipynb`: End-to-end Google Colab research simulation and analysis notebook.
- `index.html`: Responsive static dashboard for exploring wireless resource-allocation simulation results.
- `netlify.toml`: Configuration for static deployment (headers for CSV data, root publish directory).
- `data/`: Archived simulation results and statistical validation datasets:
  - `scenario_summary_mean_sd.csv`: Means and sample standard deviations across 10 seeds.
  - `v2_vs_equal_all_scenarios.csv`: V2 vs Equal allocation comparisons across 12 scenarios.
  - `robustness_raw_results.csv`: Raw per-seed evaluation records.
  - `table_10_users_target1_mean_sd.csv`: Target evaluation statistics for 10 users.
  - `constraint_validation.csv`: Validation metrics against operational constraints.
  - `paired_bootstrap_ci_v2_minus_equal.csv`: Bootstrap confidence intervals.
  - `original_paired_bootstrap_ci.csv`: Baseline bootstrap confidence intervals.
- `assets/`: Simulation architecture diagrams, workflow figures, and performance charts:
  - `fig5_architecture.png`: Simulation architecture overview.
  - `fig6_workflow.png`: Experimental workflow and methodology.
  - `fig_throughput_vs_users.png`: Throughput by user population.
  - `fig_reliability_delta_heatmap.png`: Reliability delta heatmaps.
  - Performance error bars (`fig_fairness_errorbars.png`, `fig_minrate_errorbars.png`, `fig_reliability_errorbars.png`, `fig_throughput_errorbars.png`).

---

## Running the Dashboard Locally

```bash
python3 -m http.server 8080
```
Then open [http://localhost:8080](http://localhost:8080) in your browser.

## Deploying to Netlify

This is a static site; no build command is required.
1. Connect this GitHub repository to [Netlify](https://app.netlify.com/).
2. Set Publish directory to `.`.
3. Alternatively, drag and drop the repository folder into [Netlify Drop](https://app.netlify.com/drop).

---

## Data and Interpretation Note

The dashboard visualizes the illustrative simulator's outputs. Programmed budget checks are not field or physical-layer validation.
