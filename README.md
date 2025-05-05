# 🛠️ Wi-Fi 7 Microstrip Patch Antenna Optimization with Machine Learning

## 📂 Dataset

**📁 Wi-Fi 7 Antenna Simulation Dataset**
Access the full dataset on Kaggle:
🔗 [Wi-Fi 7 Dataset on Kaggle](https://www.kaggle.com/datasets/shahriar26s/wifi-7-dataset/data)

## ⚙️ Tools & Technologies

* **CST Studio Suite** – Antenna design & EM simulation
* **Python (Pandas, Scikit-learn)** – Data processing & modeling
* **Matplotlib / Seaborn** – Data visualization
* **Kaggle** – Dataset hosting & modeling notebooks
* **GitHub** – Version control & documentation

### 📥 Dataset Overview:

* **Source:** CST Microwave Studio Simulations
* **Samples:** 3,003 data points
* **Inputs:**

  * Frequency (GHz)
  * Patch Length & Width (mm)
  * Substrate Thickness & Width (mm)
  * Slot Area (mm²)
  * Circular Slot Radius (mm)
* **Target:** S₁₁ (in dB)

---

## 🧹 Data Cleaning & Exploratory Analysis

* ✅ No missing values across all features.
* 📈 Pearson correlation matrix computed to detect collinearity.
* 🔍 Scatter plots and distribution analysis confirmed balanced feature ranges without extreme outliers.

---

## 🔄 Preprocessing Pipeline

* 📊 **Train/Test Split:** 80% training (2,402 samples), 20% testing (601 samples)
* 📏 **Standardization:** All inputs scaled using StandardScaler (mean = 0, std = 1)
* 📉 **PCA Applied:** Optional dimensionality reduction tested to examine variance retention
* 📌 **Correlation Plots:** Used to visualize feature interactions and validate model input stability

---

## 🤖 Regression Modeling

Five regression pipelines were evaluated:

| Model                       | Description                                        |
| --------------------------- | -------------------------------------------------- |
| Random Forest (default)     | 100 estimators, default parameters                 |
| RF (Hyper-tuned)            | Grid-searched `n_estimators`, `max_depth`          |
| Decision Tree (Tuned)       | Grid-searched `max_depth`, `min_samples_leaf`      |
| Stacking Ensemble (Default) | Ridge, Gradient Boost, RF base; Ridge meta-learner |
| Stacking (with tuned RF)    | Same ensemble with optimized RF base model         |

---

## 📊 Performance Metrics

| Model                 | MAE        | MSE        | RMSE       | R²         | MAPE (%) |
| --------------------- | ---------- | ---------- | ---------- | ---------- | -------- |
| RF (Default)          | 0.2481     | 0.7510     | 0.8664     | 0.9696     | 2.59     |
| Stacking (Default)    | 0.2601     | 0.7034     | 0.8387     | 0.9716     | 3.76     |
| **RF (Tuned)**        | **0.1580** | **0.2618** | **0.5117** | **0.9894** | **1.66** |
| Stacking (Tuned RF)   | 0.2442     | 0.7879     | 0.8877     | 0.9681     | 3.09     |
| Decision Tree (Tuned) | 0.2846     | 1.1947     | 1.0930     | 0.9517     | 2.83     |

---

## 💬 Discussion

* ✅ The **hyper-tuned Random Forest** achieved the best performance with the **lowest error** and highest **R² = 0.9894**, indicating excellent predictive capability.
* 📉 All models demonstrated strong regression ability with **R² > 0.95**, confirming that geometric design features alone are sufficient for accurate S₁₁ estimation.
* 🔁 Stacking models showed reliable generalization but slightly higher relative error (MAPE).
