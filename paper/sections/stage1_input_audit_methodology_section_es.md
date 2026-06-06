# Stage 1 — Auditoría de entrada radiográfica y diseño de canales

Esta etapa no tiene como objetivo predecir ni explicar el ángulo de Cobb. Su propósito es caracterizar el espacio de entrada radiográfico mediante propiedades fotométricas, descriptores estructurales, contenido de alta frecuencia y perfiles de ruido. Esta caracterización permite guiar el preprocesamiento, la construcción de canales y el diseño de ablaciones antes del entrenamiento de modelos de segmentación.

Sea I_i una radiografía de entrada. Se define un vector de auditoría:

q_i = Q(I_i)

donde Q extrae descriptores fotométricos, estructurales, frecuenciales y de ruido. El objetivo no es clasificar clínicamente la imagen, sino caracterizar sus condiciones de entrada para definir transformaciones candidatas.

Debido a que los scores tienen escalas diferentes, se aplicó normalización z-score:

z = (x - μ) / σ

Esta transformación permite comparar métricas con unidades y rangos distintos. Por ejemplo, un score de ruido fractal puede tener valores alrededor de 2 o 3, mientras que un score de salt-and-pepper puede estar cerca de 0.001. Sin z-score, el valor más grande dominaría artificialmente la interpretación.

El mapa de correlación se utilizó para identificar bloques de métricas parcialmente redundantes. Posteriormente se aplicó PCA para resumir el espacio de entrada en componentes principales interpretables. Además, los perfiles de ruido normalizados se agruparon mediante K-Means para identificar patrones dominantes de degradación visual.

La salida de esta auditoría no es una predicción clínica, sino una política inicial de diseño de canales. Esta política define qué transformaciones deben evaluarse en la siguiente etapa: normalización robusta, CLAHE, Scharr/Sobel, mediana, bilateral, FFT/notch y canales ROI o anatómicos.
