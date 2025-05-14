# 🔋 GRU-GAN for State of Health (SOH) Prediction in Lithium-Ion Batteries

This repository presents a research-based comparative study on predicting the **State of Health (SOH)** of lithium-ion batteries using a hybrid deep learning model: **GRU-GAN**. The approach combines Gated Recurrent Units (GRU) with Generative Adversarial Networks (GAN) to enhance prediction accuracy.

---

## 📘 Overview

Traditional machine learning and even some deep learning models often fail to capture the **complex degradation behavior** of lithium-ion batteries. This study investigates how integrating a GAN with a GRU model can improve prediction performance for battery SOH estimation.

- **Dataset**: NASA Battery Data Set
- **Preprocessing**: MinMax normalization, time series sequence slicing
- **Models compared**:
  - GRU (baseline)
  - GRU-GAN (proposed)
- **Metrics**: RMSE, MAE, R²

---

## 📊 Key Findings

| Model       | RMSE  | MAE   | R²    |
|-------------|-------|-------|-------|
| GRU         | 0.046 | 0.037 | 0.921 |
| **GRU-GAN** | **0.038** | **0.029** | **0.953** |

✅ **GRU-GAN significantly outperformed the baseline GRU**, especially on long-term predictions, thanks to the adversarial learning component.

---

## 🧪 Methodology

The workflow followed:
1. **Data Collection**: NASA battery dataset (Battery 05 and 18)
2. **Preprocessing**: Sequence slicing of battery capacity values over cycles
3. **Modeling**:
   - GRU for sequence learning
   - GAN for refining the predictions
4. **Training**:
   - 100 epochs for both GRU and GAN
   - Early stopping and checkpointing
5. **Evaluation**:
   - RMSE, MAE, and R² on unseen test data

---

## 📁 Files in this Repository

- `GRU-GAN for SOH prediction final.pdf`: Full comparative analysis report, including methodology, results, and future work.

---

## 📌 Future Scope

The report also outlines potential improvements:
- Test on **real-world EV battery data**
- Use **transfer learning** for better generalization
- Integrate **attention mechanisms**
- Deploy for **real-time battery monitoring**

---

## 👤 Author

**Akhil Goud Rachakonda**  
Master's in Computer Science, Sweden 🇸🇪 (Dual Degree, Graduation: June 2026)  
[Email](mailto:akra24@student.bth.se) • [LinkedIn](www.linkedin.com/in/akhil-rachakonda-a968a2214)

---

> This repository serves as a research portfolio item. No implementation code is provided.
