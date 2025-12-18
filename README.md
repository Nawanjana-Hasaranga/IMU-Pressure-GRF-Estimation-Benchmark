# Benchmarking Random Forest vs. Deep Learning for 3D GRF Estimation

## Project Overview
This project benchmarks a **Random Forest Regressor** against the complex **Dual-Stream Attention Network** proposed by Zhang et al. (2025) [cite_start]for estimating 3D Ground Reaction Forces (GRFs)[cite: 1538, 1545].

## Key Evidence
Using a multimodal sensor fusion approach (IMU + Pressure), I achieved the following results:
* **Zhang et al. (2025) [cite_start]Attention Model:** 4.16% NRMSE [cite: 445]
* **My Random Forest Implementation:** **3.30% NRMSE**
* **LSTM Model R² Score:** **0.9514**

## Methodology
1. [cite_start]**Data Fusion:** Combined 12-channel CapSense pressure data with 6-axis IMU data[cite: 142, 1553].
2. [cite_start]**Preprocessing:** Applied a moving average filter and Min-Max normalization[cite: 219, 220].
3. [cite_start]**Training:** Compared temporal deep learning (LSTM) against a flattened feature baseline (Random Forest).

## Visual Comparisons
### LSTM Prediction (Deep Learning)
![LSTM Result](download.png)

### Random Forest Prediction (Baseline)
![Random Forest Result](rf_result.png)
