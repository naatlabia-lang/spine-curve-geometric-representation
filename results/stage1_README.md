# Stage 1 — Input Image Audit Results

This folder contains the tables, figures, and grids used to document the first methodology section: input radiograph audit and channel design.

## Scope

Cobb angle is not the target of this stage. It may remain as metadata, but the goal of Stage 1 is to characterize the input radiographs before model training.

## Tables

- `stage1_table_01_input_metric_dictionary.csv`
- `stage1_table_02_input_metric_summary.csv`
- `stage1_table_03_noise_metric_summary.csv`
- `stage1_table_04_channel_design_policy.csv`
- `stage1_table_05_recommended_ablation_plan.csv`
- `stage1_table_06_top_hard_cases_by_noise_zscore.csv`
- `stage1_table_09_noise_k_selection_silhouette.csv`
- `stage1_table_10_noise_cluster_centers_zscore.csv`
- `stage1_table_11_dominant_noise_counts.csv`

## Figures

- `stage1_fig_02_input_metric_correlation_heatmap.png`
- `stage1_fig_03_pca_input_descriptors.png`
- `stage1_fig_04_noise_profile_clusters_pca.png`
- `stage1_fig_05_noise_cluster_zscore_heatmap.png`
- `stage1_fig_06_input_pca_pc1_loadings.png`

## Grids

- `stage1_grid_top_hard_cases_by_dominant_noise_zscore.png`
- `stage1_grid_top_gaussian.png`
- `stage1_grid_top_poisson.png`
- `stage1_grid_top_salt_pepper.png`
- `stage1_grid_top_speckle.png`
- `stage1_grid_top_periodic.png`
- `stage1_grid_top_structured_line.png`
- `stage1_grid_top_quantization.png`
- `stage1_grid_top_brownian_fractal.png`

## Interpretation

The generated outputs support the transition to Stage 2: preprocessing and channel construction.
