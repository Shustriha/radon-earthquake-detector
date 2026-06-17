## Radon Earthquake Detector

Prototype pipeline for modeling normal radon behavior and investigating residual anomalies as possible earthquake precursors.

## Project idea

The long-term goal of this project is to build a radon time-series anomaly detection pipeline inspired by earthquake-precursor research.

The intended workflow is:

1. Load and clean radon time-series data.
2. Build time-series features from the radon signal and related variables.
3. Train a model to predict normal radon concentration.

4. Calculate residuals:

    residual = measured_radon - predicted_radon

5. Treat unusually large residuals as candidate radon anomalies.
6. Compare detected anomaly periods with earthquake catalogs.


## Current status

This repository currently contains the first stage of the pipeline: data loading, preprocessing, and time-series feature extraction.

Current components:

- Data loading from the source file
- Basic preprocessing and timestamp handling
- Time-series feature extraction
- Exploratory notebook for trend, seasonality, lag, and residual analysis

Feature groups currently explored:

- Lag features
- Rolling statistics
- Trend-related features
- Seasonality/Fourier-style features
- Residual/anomaly-related analysis in notebooks

## Data

This prototype uses a small open-source radon time-series dataset included in data/raw/.

## Next steps

- Add baseline model training for normal radon prediction
- Compute model residuals
- Add residual-based anomaly detection
- Add wavelet denoising
- Add ANN-based models
- Add earthquake catalog integration
- Validate detected anomalies against earthquake-event windows


## Disclaimer

This project does not claim deterministic earthquake prediction. The current goal is to model normal radon behavior and investigate whether residual radon anomalies may be associated with seismic activity.
