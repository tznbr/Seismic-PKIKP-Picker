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
- `Seismic_PKIKP_Picker.ipynb`: Complete Google Colab pipeline including data cleaning, model tournament, and final benchmarking.
- `Dropbox link`: The training and testing datasets derived from 300,000 synthetic waveforms mixed with real-world ambient noise.
- `JGR Solid Earth - 2024 - Zhou - Deep‐Learning Phase‐Onset Picker for Deep Earth Seismology PKIKP Waves.pdf`: The original JGR Solid Earth research paper that served as our benchmark.

## 🛠️ Tech Stack

### **Core Language & Environment**
- **Python 3.x**: The primary language used for data processing and model development.
- **Google Colab**: Cloud-based environment utilized for high-performance computation and collaborative development.

### **Machine Learning & Modeling**
- **XGBoost**: Our primary high-performance Gradient Boosting framework.
- **Scikit-Learn**: Used for model benchmarking (Linear Regression, Random Forest, etc.), data splitting, and evaluation metrics.
- **CatBoost & LightGBM**: Benchmarked as State-of-the-Art competitors in the model tournament.

### **Data Manipulation & Analysis**
- **Pandas**: Utilized for heavy-duty data cleaning, filtering, and CSV manipulation.
- **NumPy**: Used for efficient numerical arrays and mathematical operations.

### **Visualization & Reporting**
- **Matplotlib & Seaborn**: Used to create our scientific charts, including the Model Tournament results, Feature Importance, and Stability (KDE) plots.

### **Data Engineering**
- **Dropbox**: Utilized for remote large-scale data hosting and delivery.

## 📊 Datasets
Due to file size limits on GitHub, the datasets are hosted on Dropbox. 

1. **Download the data:** [Click here to download the datasets from Dropbox](https://www.dropbox.com/scl/fo/yhri09ycjr25qt3pwzu6x/AA3JLkJYQAA75-3xK9KlGXY?rlkey=79lx9675hjyu6cgr00qb494mr&st=f516xsfa&dl=0)
2. **Prepare for Colab:** Once downloaded, please upload `features.csv` and `test_split_with_cnn.csv` into the **Content** folder within the **Files** folder (the folder icon on the left sidebar) of the Google Colab environment before running the code.

## 🛠️ How to Run
1. Open the `Seismic_PKIKP_Picker.ipynb` in Google Colab.
2. Upload the CSV files from the `dropbox` link to your Colab session.
3. Run all cells to reproduce the Model Tournament and final benchmarking results.

## 📚 References
*Zhou, J., Phạm, T.‐S., & Tkalčić, H. (2024). Deep‐learning phase‐onset picker for deep Earth seismology: PKIKP waves. Journal of Geophysical Research: Solid Earth.*
