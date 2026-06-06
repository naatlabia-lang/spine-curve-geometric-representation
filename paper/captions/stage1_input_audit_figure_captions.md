# Stage 1 figure captions

## Figure 1. Input audit and channel design pipeline
Radiographic input audit pipeline. Each radiograph is analyzed through photometric, structural, frequency-domain, noise, and background descriptors. The resulting audit vector is used to guide channel construction, preprocessing selection, and ablation design before segmentation training.

## Figure 2. Input descriptor correlation heatmap
Spearman correlation heatmap across input-only descriptors. Block structures indicate partially redundant descriptor families, including photometric contrast, structural frequency, and noise-related features.

## Figure 3. PCA of input audit descriptors
PCA visualization of the input audit descriptors. Principal components summarize correlated metric families and provide a compact representation of radiographic input variability.

## Figure 4. Noise profile clusters in PCA space
K-Means clusters computed from standardized noise descriptors and projected into a two-dimensional PCA space. Clusters represent input degradation profiles rather than clinical severity classes.

## Figure 5. Standardized noise cluster centers
Heatmap of standardized cluster centers for noise descriptors. Positive z-scores indicate descriptors above the dataset average and are used to interpret the dominant degradation profile of each cluster.

## Figure 6. Hard cases by dominant noise z-score
Representative hard cases selected by the highest dominant standardized noise score. These cases are candidates for visual inspection, preprocessing stress tests, and hard-case fine-tuning.
