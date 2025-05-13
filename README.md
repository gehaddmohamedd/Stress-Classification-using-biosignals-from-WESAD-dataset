# 🧠 Multimodal Stress Detection Using Physiological Signals (WESAD Dataset)

This project presents a machine learning pipeline for stress classification using three biosignals recorded from the chest:  
- **Electrodermal Activity (EDA)**  
- **Electrocardiogram (ECG)**  
- **Respiration (RESP)**  

Based on the WESAD dataset, the pipeline performs both **binary** (Non-stressed vs. stress)

## 🔁 Pipeline Steps (applied for each signal)

1. **Data Preparation**  
   - Load chest signals from the WESAD dataset  
   - Remove corrupted or incomplete subjects

2. **Signal Preprocessing**  
   - Apply filtering, normalization, and segmentation  
   - Sliding window segmentation with overlap

3. **Feature Engineering**  
   - Extract statistical, frequency-domain, and physiological features  
   - Create a clean, feature-rich dataset per signal

4. **Balancing & Selection**  
   - Address class imbalance using SMOTE or Tomek Links  
   - Optional: feature selection based on importance or correlation

5. **Modeling & Evaluation**  
   - Apply and tune models (Random Forest, XGBoost)  
   - Evaluate using:
     - Train/test split
     - K-fold cross-validation
     - Leave-One-Subject-Out (LOSO-CV)

---
