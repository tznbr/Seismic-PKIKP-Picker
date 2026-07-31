# DSB 7500 Final Practicum Project: High-Efficiency Seismic Phase Picking
**Collaborators:** Momina Zain, Keerthana Reddy, & Taznen Al-Bari

## 🌍 Project Overview
This project optimizes the automatic detection of **PKIKP seismic waves**—critical signals that travel through the Earth’s inner core. While original research utilized a complex Convolutional Neural Network (CNN), our team benchmarked **XGBoost** and 9 other machine learning models to create a "lighter, faster, and more stable" alternative.

### 🎯 Objective
To prove that a feature-engineered Gradient Boosting model can match human-level precision while significantly reducing the computational resources required for deep-earth seismology.

## 🚀 Key Results
Our **Tuned XGBoost** model emerged as the scientific champion, outperforming the original research's deep learning baseline in stability and efficiency.

| Metric | Tuned XGBoost (Ours) | Original CNN (Benchmark) | Scientific Win |
| :--- | :--- | :--- | :--- |
| **MAE (Precision)** | **0.2256s** | 0.2280s | **Pinpoint Accuracy** |
| **RMSE (Stability)** | **0.3869** | 0.6027 | **35% More Stable** |
| **Training Speed** | **31.68s** | ~1200.00s | **38x Faster** |

## 🧠 Why It Works (The Physics)
Unlike "Black Box" deep learning, our model relies on engineered physical features that mimic human reasoning:
- **X_aic_t**: Statistical changes in signal character.
- **X_stalta_t**: Sudden jumps in seismic energy.
- **Robustness**: Our model maintains precision even in low Signal-to-Noise (SNR) environments, proving it is ready for real-world messy data.

## 📁 Repository Contents
- `Seismic_Profiling.ipynb`: Complete Google Colab pipeline including data cleaning, model tournament, and final benchmarking.
- `/data`: The training and testing datasets derived from 300,000 synthetic waveforms mixed with real-world ambient noise.
- `/paper`: The original JGR Solid Earth research paper that served as our benchmark.

## 🛠️ How to Run
1. Open the `Seismic_Profiling.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Upload the CSV files from the `/data` folder to your Colab session.
3. Run all cells to reproduce the Model Tournament and final benchmarking results.

## 📚 References
*Zhou, J., Phạm, T.‐S., & Tkalčić, H. (2024). Deep‐learning phase‐onset picker for deep Earth seismology: PKIKP waves. Journal of Geophysical Research: Solid Earth.*
