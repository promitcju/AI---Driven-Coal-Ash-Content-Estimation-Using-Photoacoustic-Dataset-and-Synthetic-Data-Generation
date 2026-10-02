# AI-Driven Coal Ash Content Estimation Using Photoacoustic Signals

## Project Overview

This project presents an AI-driven approach for estimating coal ash
content using Photoacoustic (PA) sensing and machine learning.

The overall pipeline combines photoacoustic signal processing,
feature engineering, feature ranking, regression modelling, and
synthetic data generation using a Variational Autoencoder (VAE).

The objective is to develop a data-driven and deployable framework
for rapid estimation of coal quality parameters from PA signals.

## Project Pipeline

The project consists of two major components:

### 1. Coal Ash Content Prediction

- PA data acquisition
- Signal preprocessing and processing
- Feature extraction
- Feature ranking
- Regression model development
- Model evaluation
- ML model serialization
- Development of a deployable GUI pipeline

### 2. Synthetic Data Generation

- PA signal reconstruction using VAE
- Latent feature extraction
- Latent feature ranking
- Engineered feature extraction
- Hybrid feature fusion
- Decoder development
- Synthetic PA signal generation
- Evaluation of existing ML models using synthetic data

## Signal Processing

The PA signals are processed to obtain meaningful time-domain and
frequency-domain information before machine learning.

The processing pipeline includes:

- Signal preprocessing
- Signal denoising
- Feature extraction
- Frequency-domain analysis
- Feature ranking
- Regression-based prediction

A block-diagram representation of the proposed preprocessing,
feature extraction and ML-assisted analysis pipeline is included
in the project documentation.

## Machine Learning

Multiple regression models were investigated for predicting coal
ash content, including:

- XGBoost Regressor
- Extra Trees Regressor
- Gradient Boosting Regressor
- CatBoost Regressor
- Support Vector Regression (SVR-RBF)

Model performance was evaluated using cross-validation and testing
data.

## VAE-Based Synthetic Data Generation

A Variational Autoencoder (VAE) was developed for signal
reconstruction and latent feature extraction.

The latent representation was combined with engineered
photoacoustic signal features to form hybrid feature sets.

Different combinations of latent and engineered features were
investigated to study their effect on signal reconstruction.

## Hybrid Feature Representation

Hybrid feature sets were investigated by combining latent VAE
features with engineered signal features.

The study evaluated different combinations of latent and engineered
features and examined reconstruction correlation and reconstruction
loss.

## Synthetic Data Evaluation

The trained decoder was used to generate synthetic time-domain
photoacoustic signals from densified feature representations.

The generated synthetic data were subsequently evaluated using
existing machine learning models.

The synthetic-data experiments investigated prediction performance
for:

- Ash Content
- Carbon Content
- Ignition Temperature

## Results

For the original dataset, several regression models were evaluated
using cross-validation and testing data.

| Model | Mean CV | Testing Accuracy |
|---|---:|---:|
| XGBoost Regressor | 0.9086 ± 0.0300 | 88.81% |
| Extra Trees Regressor | 0.8898 ± 0.0157 | 89.41% |
| Gradient Boosting Regressor | 0.8935 ± 0.0226 | 90.21% |
| CatBoost Regressor | 0.8940 ± 0.0170 | 90.32% |
| SVR-RBF | 0.9051 ± 0.0036 | 89.35% |

The experimental dataset used in this study contained 900 PA signal
results from 13 unique coal samples, with 720 samples used for
training and 180 for testing. :chatgpt-content-reference{index="1"}

Synthetic-data experiments were also performed to evaluate the
effect of generated data on model performance. :chatgpt-content-reference{index="2"}

## Technologies Used

- Python
- NumPy
- Pandas
- SciPy
- Scikit-learn
- XGBoost
- CatBoost
- Matplotlib
- Machine Learning
- Deep Learning
- Variational Autoencoder (VAE)
- Signal Processing
- Feature Engineering

## Key Areas of Work

- Photoacoustic sensing
- Digital signal processing
- Feature engineering
- Statistical feature analysis
- Machine learning regression
- Model optimization
- VAE-based representation learning
- Synthetic data generation
- Data analysis and visualization

## Project Structure

```text
AI-Coal-Ash-Prediction-Photoacoustic/
│
├── README.md
│
├── src/
│   ├── preprocessing/
│   ├── feature_extraction/
│   ├── feature_selection/
│   ├── regression/
│   └── synthetic_data/
│
├── notebooks/
│
├── results/
│
├── documentation/
│   └── Project_Report.pdf
│
└── .gitignore
