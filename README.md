# Assignment 4 - Prognostics and Health Management
**Course:** Augmented Decision Making D7017B  

## Overview

Implementation of three steps of the PHM (Prognostics and Health Management) framework.

**Part I - Anomaly Detection**  
An autoencoder is trained on MNIST digits 0-8 (normal). Digit 9 is treated as the anomaly class. Images with reconstruction error above a threshold (mean + std of normal-only validation errors) are flagged as anomalies.

**Part II - Diagnosis**  
K-Means clustering on PCA-reduced MNIST features to group the 9 digit classes without using labels. Optimal k is selected using the elbow method and silhouette score.

**Part III - Prognosis**  
RUL (Remaining Useful Life) prediction on the NASA C-MAPSS FD001 turbofan dataset using SVR and an LSTM. Results are compared using MAE, RMSE, and R2.

## Files

- `Assignment 4.ipynb` - full implementation covering all three parts
- `data/CMAPSS/` - NASA C-MAPSS FD001 dataset (train, test, RUL files)
