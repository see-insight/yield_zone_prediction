# Yield Zone Prediction

## Project Overview

This repository supports research on satellite-based crop yield prediction and uncertainty quantification for major U.S. Midwest crops. The work centers on using Sentinel-1 SAR observations at native 10-meter resolution together with terrain, soil, and weather covariates to predict stable yield zones for corn, soybean, and winter wheat.

The goal is to move beyond single-point yield estimates by generating probabilistic, calibrated yield zone predictions and decomposing uncertainty into meaningful components that reflect both observable and unobservable sources of error.

## Motivation

Food production systems face rising economic and environmental pressures from climate variability, yield risk, and input price volatility. In the U.S. Midwest, fields exhibit sub-field heterogeneity that strongly influences the profitability and efficiency of farm management decisions.

This research is motivated by the need to support precision agriculture with models that: 

- identify stable low, medium, and high yield zones within fields
- quantify prediction confidence for individual locations
- capture uncertainty arising from satellite-derived inputs, farm-specific effects, and new-season generalization

## Key Contributions

1. Evaluation of 10-meter Sentinel-1 SAR-based models for recovering temporally stable yield zones across corn, winter wheat, and soybean.
2. Development of a crop-stratified hierarchical Bayesian residual correction model that learns structured prediction error from out-of-fold XGBoost predictions.
3. Decomposition of predictive uncertainty into epistemic, aleatoric, and farm-level components.
4. Sequential Bayesian updating of yield zone probabilities as new SAR acquisitions are added through the growing season.

## Repository Structure

- `corn.ipynb` — Notebook for corn yield modeling and analysis.
- `soybean.ipynb` — Notebook for soybean yield modeling and analysis.
- `wheat.ipynb` — Notebook for winter wheat yield modeling and analysis.
- `Hist Gradient Boosting Regression.ipynb` — A notebook exploring gradient boosted regression models and their performance.
- `hyperparameter tuning.ipynb` — Hyperparameter tuning experiments for model optimization.
- `LSTM.ipynb` — LSTM-based modeling experiments.
- `RNN.ipynb` — Recurrent neural network modeling experiments.
- `Transformer.ipynb` — Transformer-based modeling experiments.
- `plots.ipynb` — Visualization and plotting of results.
- `research.ipynb` — Research notes, conceptual development, and analysis summary.
- `Optimized Models/` — Directory containing model artifacts and optimized outputs.

## Data and Methods

The project emphasizes SAR-based crop monitoring using Sentinel-1, which enables cloud-penetrating, high-frequency observations of canopy structure, moisture, and surface conditions.

Methodological themes include:

- machine learning for yield prediction
- hierarchical Bayesian calibration of model residuals
- farm-level random effects and hierarchical uncertainty
- yield zone classification rather than only continuous regression
- probabilistic prediction maps and uncertainty-aware decision support

## Usage

This repository is organized as a research notebook collection. To explore the project:

1. Open the desired notebook in Jupyter or JupyterLab.
2. Run the cells sequentially to load data, train models, and analyze results.
3. Review `Optimized Models/` for saved model artifacts and outputs.

## Notes

- The repository currently contains Jupyter notebooks as the primary analysis artifacts.
- Data files are not included in the repo, so users will need access to the underlying datasets for full reproduction.

