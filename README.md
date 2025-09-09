Dynamic Factor Model using Recurrent Variational AutoEncoder (RVAE)
📌 Overview

This project implements a Dynamic Factor Model using a Recurrent Variational AutoEncoder (RVAE) to analyze stock market dependencies from time-series data. The model is designed to uncover latent market factors that drive stock co-movements, using deep learning techniques.

The project focuses on the NIFTY50 index constituents, leveraging 20 years of log-return data with a 16-year training window to capture temporal market dynamics.

⚡ Key Features

🔹 Built a Recurrent Variational AutoEncoder (RVAE) in PyTorch with LSTM cells for sequential modeling.

🔹 Configurable training via JSON-based hyperparameter setup.

🔹 Processed 20 years of daily stock log-returns from 25 NIFTY50 stocks.

🔹 Extracted 6 latent factors driving market behavior.

🔹 Validated latent factors using:

Kaiser-Meyer-Olkin (KMO) measure

Scree plot analysis

🛠️ Tech Stack

Language: Python

Frameworks/Libraries: PyTorch, NumPy, Pandas, Matplotlib, Scikit-learn

Deep Learning Model: Recurrent Variational AutoEncoder (RVAE) with LSTM

Data: Historical daily log-returns of 25 NIFTY50 stocks (20 years)

📊 Methodology

Data Preparation

Collected & preprocessed log-return data for selected NIFTY50 stocks.

Defined training (16 years) and validation/testing (4 years) splits.

Model Architecture

Encoder: LSTM layers → latent distribution (μ, σ).

Decoder: LSTM layers → reconstruct stock return sequences.

Loss: Reconstruction Loss + KL Divergence.

Latent Factor Extraction

Derived 6 latent dynamic factors from trained RVAE.

Applied KMO test and scree plot for dimensionality validation.

📈 Results

Extracted 6 latent factors explaining most of the variance in stock returns.

Demonstrated RVAE’s ability to capture temporal dependencies in financial time series.

Factors validated using statistical adequacy tests.
