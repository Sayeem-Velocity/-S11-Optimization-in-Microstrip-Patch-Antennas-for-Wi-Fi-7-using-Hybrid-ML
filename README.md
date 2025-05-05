# 🛠️ Wi-Fi 7 Microstrip Patch Antenna Optimization with Machine Learning

## 🔍 Project Overview

This project presents the design and optimization of a **microstrip patch antenna** for **Wi-Fi 7 frequency bands**, combining electromagnetic simulations with machine learning. The primary objective is to **minimize the S11 parameter**, ensuring effective impedance matching and enhanced signal efficiency.

## 🚀 Optimization Pipeline

### 🎯 Antenna Simulation

Designed and simulated multiple antenna configurations in **CST Studio Suite**, covering the Wi-Fi 7 frequency spectrum.

### 📊 Data Collection

Exported key simulation parameters (S11, gain, bandwidth, radiation pattern) to Excel and created a **custom dataset** for ML training.

### 🤖 Machine Learning

Used regression-based ML models to **predict and optimize antenna performance**, with a focus on reducing S11.

### 📈 Evaluation Metrics

Model performance was evaluated using:

* **MAE** – Mean Absolute Error
* **MSE** – Mean Squared Error
* **RMSE** – Root Mean Squared Error
* **MAPE** – Mean Absolute Percentage Error

---

## 📂 Dataset

**📁 Wi-Fi 7 Antenna Simulation Dataset**
Access the full dataset on Kaggle:
🔗 [Wi-Fi 7 Dataset on Kaggle](https://www.kaggle.com/datasets/shahriar26s/wifi-7-dataset/data)

---

## ⚙️ Tools & Technologies

* **CST Studio Suite** – Antenna design & EM simulation
* **Python (Pandas, Scikit-learn)** – Data processing & modeling
* **Matplotlib / Seaborn** – Data visualization
* **Kaggle** – Dataset hosting & modeling notebooks
* **GitHub** – Version control & documentation

---

## ✅ Project Goals

* Design a compact, high-performance antenna for **Wi-Fi 7**
* Minimize **S11** for optimal efficiency
* Use machine learning to predict and enhance antenna characteristics from simulation data
