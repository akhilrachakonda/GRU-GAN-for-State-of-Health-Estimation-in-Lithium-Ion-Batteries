# 🔋 GRU-GAN for State of Health (SOH) Prediction in Lithium-Ion Batteries

This repository presents a research-based comparative study on predicting the **State of Health (SOH)** of lithium-ion batteries using a hybrid deep learning model: **GRU-GAN**. The approach combines Gated Recurrent Units (GRU) with Generative Adversarial Networks (GAN) to enhance prediction accuracy.

---

## 📘 Overview

Traditional machine learning and even some deep learning models often fail to capture the **complex degradation behavior** of lithium-ion batteries. This study investigates how integrating a GAN with a GRU model can improve prediction performance for battery SOH estimation.

- **Dataset**: NASA Battery Data Set (Battery #05 and #18)
- **Preprocessing**: MinMax normalization, time series sequence slicing
- **Models compared**:
  - GRU (baseline)
  - GRU-GAN (proposed hybrid model)
- **Metrics**: RMSE, MAE, R²

---

## 📊 Key Findings

| Model       | RMSE  | MAE   | R²    |
|-------------|-------|-------|-------|
| GRU         | 0.046 | 0.037 | 0.921 |
| **GRU-GAN** | **0.038** | **0.029** | **0.953** |

✅ **GRU-GAN significantly outperformed the baseline GRU**, especially on long-term predictions, thanks to the adversarial learning component.

> 🔍 **Note**: The above results are from the official project report. Due to slight variations in training randomness, hardware, and retraining parameters, the results from the latest Python implementation in this repo may differ slightly (e.g., RMSE ≈ 0.045–0.050). These deviations are expected and do not affect the model’s overall improvement trend.

---

## 🧪 Methodology

The workflow followed:

1. **Data Collection**: NASA battery dataset (Battery 05 and 18)
2. **Preprocessing**: Sequence slicing of battery capacity values over cycles, normalized using MinMaxScaler
3. **Modeling**:
   - GRU for temporal sequence modeling
   - GAN for refining and improving GRU predictions
   - Deepened generator and discriminator networks with dropout and residual connections
4. **Training**:
   - GRU: 100 epochs with early stopping
   - GAN: 3000 epochs with alternating training and manual learning rate scheduling
5. **Evaluation**:
   - RMSE, MAE, and R² on unseen test data
   - Comparative plots of predicted vs. true SOH

---

## 📁 Files in this Repository

- `gru_gan_soh_prediction.py`: Full GRU-GAN implementation including preprocessing, training, and evaluation
- `GRU-GAN for SOH prediction final.pdf`: Final research report detailing the project, experimental setup, and results
- `README.md`: Project documentation and explanation
- Dataset files (`B0005.mat`, `B0018.mat`): NASA battery data (not included in repo due to size—see NASA PHM Dataset)

---

## 📌 Future Scope

The report outlines potential improvements and research directions:

- Validate model on **real-world EV battery data**
- Integrate **impedance and temperature** features for higher robustness
- Apply **transfer learning** for generalized SOH estimation
- Add **attention mechanisms** to further enhance temporal sensitivity
- Use **Wasserstein GANs** or **relativistic loss** for better training stability
- Deploy for **real-time battery health monitoring**

---

## 👤 Author

**Akhil Goud Rachakonda**  
Master's in Computer Science, Sweden 🇸🇪 (Dual Degree, Graduation: June 2026)  
[Email](mailto:akra24@student.bth.se) • [LinkedIn](https://www.linkedin.com/in/akhil-rachakonda-a968a2214)

---

📌 For academic use or research extensions, please cite or acknowledge this repository. If you use the code or results, feel free to reach out!
