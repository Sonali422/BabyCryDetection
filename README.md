# 👶 Baby Cry Detection System

A **Machine Learning-based Baby Cry Classification** web application built with Python, Streamlit, and Scikit-Learn. It analyzes audio files to automatically detect and classify the reason behind a baby's cry in real time.

---

## 🎯 Project Overview

This project uses audio feature extraction and machine learning to classify baby cry sounds into meaningful categories, helping parents and caregivers understand what their baby needs — whether it's food, comfort, rest, or something else.

> **B.Tech Mini / Major Project — Baby Cry Detection**

---

## 🚀 Features

- **🎤 Audio Upload** — Upload a `.wav` baby cry audio file for instant analysis
- **🤖 ML Classification** — Predicts cry type using a trained Random Forest model
- **📊 Feature Analysis** — Extracts MFCC, Spectral Centroid, Bandwidth, ZCR, and RMS features
- **🏷️ Smart Grouping** — Classifies cries into 3 intuitive categories:
  - 🍼 **Physical Need** — Hungry, belly pain, burping, discomfort, cold/hot
  - 💛 **Emotional Need** — Tired, lonely, scared
  - ✅ **Normal** — Laughter, silence
- **🌐 Live Web App** — Powered by Streamlit, runs directly in the browser

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| Language | Python 3 |
| Web App | Streamlit |
| ML Model | Random Forest + XGBoost |
| Audio Processing | Librosa |
| Feature Engineering | MFCC, Delta, Spectral Features |
| Class Balancing | SMOTE (imbalanced-learn) |
| Model Storage | Joblib (`.pkl` files) |

---

## 📁 Project Structure

```
BabyCryDetection/
├── streamlit_app.py          # Main web app UI
├── train_model.py            # Model training script (Random Forest + XGBoost)
├── feature_extraction.py     # Audio feature extraction (MFCC, spectral, etc.)
├── baby_cry_rf_model.pkl     # Trained Random Forest model
├── label_encoder.pkl         # Label Encoder for cry categories
├── scaler.pkl                # StandardScaler for feature normalization
├── requirements.txt          # Python dependencies
└── .streamlit/               # Streamlit configuration
```

---

## 🧠 How It Works

1. **Upload** a `.wav` audio file of a baby crying
2. The app **extracts audio features** using Librosa:
   - 40 MFCC coefficients (mean + std)
   - Delta and Delta-Delta MFCCs
   - Spectral Centroid, Bandwidth, ZCR, RMS Energy
3. Features are **normalized** using a pre-trained StandardScaler
4. The **Random Forest model** predicts the cry category
5. The result is displayed with a user-friendly label

---

## 🏷️ Cry Categories

| Category | Labels Included |
|----------|----------------|
| 🍼 Physical Need | Hungry, Belly Pain, Burping, Discomfort, Cold/Hot |
| 💛 Emotional Need | Tired, Lonely, Scared |
| ✅ Normal | Laugh, Silence |

---

## 💻 Running Locally

### Prerequisites
- Python 3.8+
- pip

### Steps
```bash
git clone https://github.com/Sonali422/BabyCryDetection.git
cd BabyCryDetection
pip install -r requirements.txt
streamlit run streamlit_app.py
```

Then open: **[http://localhost:8501](http://localhost:8501)**

---

## 🏋️ Training the Model (Optional)

If you want to retrain the model on your own dataset:

1. Create a folder called `Baby Crying Sounds/` with subfolders named after each cry type (e.g., `hungry/`, `tired/`, etc.)
2. Place `.wav` audio files inside each subfolder
3. Run:
```bash
python train_model.py
```
This will generate new `baby_cry_rf_model.pkl`, `label_encoder.pkl`, and `scaler.pkl` files.

---

## 📦 Dependencies

```
streamlit
numpy
librosa
scikit-learn
soundfile
pandas
joblib
```

---

## 📄 License

This project is open-source and created for educational and research purposes.

---

## 👩‍💻 Author

**Sonali Karella** — [github.com/Sonali422](https://github.com/Sonali422)

<!-- Contribution update -->
