# 📊 Time Series Stock Price Prediction using Fuzzy-LSTM and Transfer Learning

This repository contains the code and methodology for a project completed as part of the **AI6124: Neuroevolution and Fuzzy Intelligence** course at **Nanyang Technological University (NTU), Singapore**.

We developed a hybrid **Fuzzy-LSTM** model for stock price forecasting, applied **transfer learning** across different financial assets, and evaluated performance using **RMSE** and **portfolio returns**.

---

## 🔍 Problem Statement

Stock price prediction is challenging due to:
- High volatility and noise
- Non-stationary data distributions
- Complex dependencies between economic and behavioral factors

Traditional approaches often ignore the **non-stationary** nature of stock data, resulting in poor predictive reliability.

---

## ✅ Our Contributions

1. **Stationary Transformation**:  
   Instead of predicting absolute prices, we used a **price differencing approach** to make the data stationary.

2. **Modeling Techniques**:
   - **Random Walk** (Baseline)
   - **LSTM** (Benchmark Deep Learning model)
   - **Fuzzy-LSTM**: Hybrid model incorporating fuzzy logic for uncertainty handling
   - **Transfer Learning**: Trained FLSTM on Autodesk (ADSK) and fine-tuned on NVIDIA (NVDA)

3. **Portfolio Return Calculation**:  
   Trading signals were derived using SMA crossover and evaluated using multiplicative portfolio returns.

---

## 📈 Results Summary

| Model               | RMSE   | Portfolio Returns |
|--------------------|--------|-------------------|
| Random Walk        | 7.50   | 1.0147            |
| LSTM               | 4.71   | 1.1843            |
| Fuzzy-LSTM         | 3.92   | 1.1983            |
| FLSTM + Transfer   | 3.89   | **1.1990**        |

- Transfer learning improved generalization and required minimal retraining.
- Fuzzy logic helped handle uncertainty in noisy market data.
- The hybrid model outperformed traditional baselines in both **accuracy** and **profitability**.

---

## 🧠 Model Architecture Overview

### 🔹 Fuzzy-LSTM:
- **Fuzzifier → Rule Base → Defuzzifier**
- **Strengthened Memory Layer** to enhance long-term dependency capture

### 🔹 Transfer Learning Strategy:
- Pretrain FLSTM on ADSK
- Replace output layer and fine-tune only selected layers on NVDA

---

## 🗃️ Dataset

- **Autodesk (ADSK)**: Used for pretraining
- **NVIDIA (NVDA)**: Used for fine-tuning and evaluation  
- Time range: October 2022 – September 2024  
- Data Source: Yahoo Finance

---

## 🧪 Evaluation Metrics

- **RMSE** (Root Mean Square Error) on predicted price
- **Multiplicative Portfolio Returns** from SMA trading strategy

---

## 🛠️ Setup Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/nkaps98/Stock-Price-Prediction.git
   cd Stock-Price-Prediction
   ```

2. Create and install dependencies in conda environment :
   ```bash
   conda env create -f environment.yml
   ```

4. Execute the cells in jupyter notebook for training and model evaluation:

---

## 🔮 Future Work

- Extend to **multi-stock modeling** for portfolio-level optimization
- Combine with **reinforcement learning** for adaptive trading strategies
- Integrate **sentiment analysis** from financial news and social media
- Explore **hierarchical hybrid architectures** with transformers or attention

---

## 👨‍💻 Authors

- **Nupur Kapur** – [LinkedIn](https://www.linkedin.com/in/nupurkapur)
---

## 📜 License

This project is for academic use only.

---

## ⚠️ Academic Integrity Disclaimer

> **====== I M P O R T A N T ======**

This repository is intended **solely for academic discussion, reference, and knowledge sharing**. The solutions and methods presented here are part of a completed coursework project from the **AI6124: Neuroevolution and Fuzzy Intelligence** module at NTU Singapore.

If you are a student working on a **similar assignment**, you may use this repository **only as a reference**. You must **cite this repository appropriately** in your report or code if any part of it influences your submission.

❗ Submitting any part of this project **without proper citation** may constitute **plagiarism**, and you may face consequences under your university's academic integrity policies.

The author of this repository **bear no responsibility** for any unauthorized or unethical use of its contents.

If you're enrolled in any related course (e.g., **AI6124** at NTU), please respect the academic policies of your institution. Refer to official academic integrity guidelines below:

- [NTU Academic Integrity Policy](https://ts.ntu.edu.sg/sites/intranet/dept/tlpd/ai/Pages/NTU-Academic-Integrity-Policy.aspx)
- [TLPD Academic Integrity Resources](https://ts.ntu.edu.sg/sites/intranet/dept/tlpd/ai/Pages/default.aspx)
- [Student Academic Integrity Policy PDF](https://ts.ntu.edu.sg/sites/policyportal/new/Documents/All%20including%20NIE%20staff%20and%20students/Student%20Academic%20Integrity%20Policy.pdf)

This repository should only be used for reasonable academic discussions. I, the owner of this repository, never and will never ALLOW another student to copy this assignment as their own. In such circumstances, I do not violate NTU's statement on academic integrity as of the time this repository is open (30/04/2025). I am not responsible for any future plagiarism using the content of this repository.