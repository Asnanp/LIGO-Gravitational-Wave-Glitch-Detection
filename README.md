# 🌌 LIGO Gravitational Wave Glitch Detection

This project builds an **ensemble machine learning model** to classify glitches in LIGO time-frequency data.  
Our goal: achieve **≥85% recall across all glitch classes**, including rare categories.

---

## 📊 Dataset
-[ **Source:** [Gravity Spy](https://www.zooniverse.org/projects/zooniverse/gravity-spy)  ](https://www.kaggle.com/datasets/tentotheminus9/gravity-spy-gravitational-waves)
- **Training samples:** 5587  
- **Validation samples:** 1200  
- **Test samples:** 1179  
- **Classes:** 22 glitch types  
- **Features used:** 24 (frequency, amplitude, SNR, duration, etc.)

---

## 🎯 Model
We trained an **ensemble classifier** combining:
- Random Forest  
- Gradient Boosting  
- Logistic Regression  
- Extra Trees (with **SMOTE** for class balancing)  

---

## 🏆 Results
- **Overall Accuracy (Test Set):** `90.84%`  
- **Average Recall:** `80.46%`  
- **15/22 classes ≥85% recall** 🎯  

⚠️ Classes needing improvement:  
*Chirp, Light Modulation, No Glitch, None of the Above, Paired Doves, Repeating Blips, Wandering Line*  

---

## 📈 Visualizations
Performance dashboard (Confusion matrix, per-class recall, feature importances):  

<img width="1590" height="1190" alt="download" src="https://github.com/user-attachments/assets/b178c5b2-c070-484f-8692-6bcfb96051c7" />


---

## 🔍 Feature Importances
Top predictive features:
1. Peak Frequency  
2. Peak Frequency Z-Score (H1, L1)  
3. Amplitude  
4. SNR-related features  
5. Duration  

---

## 💾 Model
Trained model is saved as:  
```bash
import joblib
model = joblib.load("ligo_ensemble_model.pkl")
```
<br><br>
🔗 Connect Author: Muhammed Asnan P

If you like this project, ⭐ the repo!
