# 🧠 Bearing Fault Diagnosis with CNN + Groq-Powered LLM (RAG-Enhanced)

A complete vibration-based bearing fault diagnosis system combining:  
- ✅ A deep learning-based CNN for accurate classification of bearing health using spectrograms.  
- 🤖 A Retrieval-Augmented Generation (RAG) system that uses Groq’s blazing fast LLM to explain or validate predictions using signal features based on ISO 13373-3.  
- 📊 Signal visualization, augmentation, and prediction history logging.

---

## 🚀 Key Features

- 🎯 **CNN Model** trained on spectrograms of segmented time-domain vibration signals.  
- 🔍 **Data Augmentations** including Gaussian noise, amplitude scaling, and frequency masking.  
- 💡 **Feature Extraction** (RMS, kurtosis, skewness, crest factor, dominant frequency) for knowledge-based reasoning.  
- 🤝 **Groq LLM Integration** for expert-like inference and diagnostic validation.  
- 🧠 **RAG Engine** built on Sentence Transformers + FAISS for semantically relevant retrieval.  
- 📈 **Interactive UI** using `ipywidgets` for user-friendly prediction interface.  
- 📝 **CSV Logging** of predictions and features for downstream analytics.

---

## ⚙️ Setup Instructions

1. **Clone this repository**

```bash
git clone https://github.com/sujith27pes/Bearing_health_deploy.git
cd bearing_health_deploy
```

2. **Install dependencies**

> Ensure you’re using Python 3.8+ and ideally a virtual environment.

```bash
pip install -r requirements.txt
```

3. **Insert your Groq API Key**



```python
groq_api_key = "gsk_..."  # Insert your Groq API Key here
```



4. **Run the notebook or script**

You can run it inside Jupyter/Colab/Kaggle or convert it into a CLI.

---

## 📊 Usage Example (Colab/Kaggle UI)

1. Upload your `.mat` file  
2. Select it via dropdown  
3. Click **“Run Prediction”**

You’ll see:
- 🔍 CNN and LLM predictions  
- 📊 Extracted signal features  
- 📈 Raw signal plot + spectrograms  
- ✅ Prediction logs saved in CSV

---

## 💡 Example Output

```
📂 Processing file: B021_2.mat

🧠 LLM (Groq) Prediction: OR  
🤖 CNN Prediction: OR (98.23%)  
📊 Extracted Features: {'rms': 0.8721, 'kurtosis': 3.92, ...}  
✅ Models agree.

📈 Segment plot and spectrograms displayed.
```

---

## 🧪 Training Notes

- Spectrograms generated with `nperseg=256`, `noverlap=128`  
- Data augmentations used during preprocessing  
- CNN trained using:  
  - `Adam` optimizer  
  - `sparse_categorical_crossentropy`  
  - EarlyStopping based on validation loss

---

## 📘 References

- CWRU Bearing Dataset  
- ISO 13373-3 Condition Monitoring Guidelines  
- [Groq](https://groq.com/) for blazing-fast inference  
- [Sentence Transformers](https://www.sbert.net/)  
- [FAISS](https://github.com/facebookresearch/faiss)

---

## 🤝 Contribution

Pull requests are welcome! Feel free to open issues for bug reports or feature suggestions.

---

## 📜 License

This project is licensed under the **MIT License**.

---

> Made with ❤️ for predictive maintenance enthusiasts.
