| family      | metric                       | definition                      | interpretation                                        |
|:------------|:-----------------------------|:--------------------------------|:------------------------------------------------------|
| Photometric | mean_intensity               | Average gray intensity          | Global brightness / exposure                          |
| Photometric | std_intensity                | Standard deviation of intensity | Global contrast                                       |
| Photometric | dynamic_range_p99_p1         | P99 - P1 intensity range        | Robust dynamic range                                  |
| Photometric | robust_range_p95_p5          | P95 - P5 intensity range        | Robust tonal spread                                   |
| Photometric | entropy                      | Intensity entropy               | Diversity of gray levels                              |
| Structural  | laplacian_var                | Variance of Laplacian           | Sharpness, abrupt transitions, noise-sensitive detail |
| Structural  | tenengrad                    | Sobel gradient energy           | Edge strength                                         |
| Structural  | scharr_mean                  | Mean Scharr gradient magnitude  | Fine edge structure                                   |
| Structural  | edge_density_canny           | Fraction of Canny edge pixels   | Edge density                                          |
| Structural  | hf_residual_std              | Std of high-frequency residual  | Fine texture or high-frequency noise                  |
| Frequency   | high_frequency_energy_ratio  | FFT high-frequency energy ratio | Frequency-domain detail                               |
| Background  | background_fraction          | Approximate background fraction | Field/collimation proxy                               |
| Background  | center_offset                | Visual center offset            | Input centering / positioning                         |
| Background  | border_artifact_score        | Edge activity near image border | Border artifact proxy                                 |
| Noise       | noise_gaussian_score         | High-frequency residual score   | Gaussian / white-like residual                        |
| Noise       | noise_poisson_score          | Local mean-variance association | Poisson / photon-like behavior                        |
| Noise       | noise_salt_pepper_score      | Extreme isolated pixels         | Impulse noise                                         |
| Noise       | noise_speckle_score          | Local coefficient of variation  | Multiplicative texture / speckle-like behavior        |
| Noise       | noise_periodic_score         | Dominant Fourier peaks          | Periodic noise                                        |
| Noise       | noise_structured_line_score  | Detected long line structures   | Structured-line artifacts                             |
| Noise       | noise_quantization_score     | Missing gray-level bins         | Quantization / banding                                |
| Noise       | noise_brownian_fractal_score | Spectral slope proxy            | Brownian / fractal-like behavior                      |