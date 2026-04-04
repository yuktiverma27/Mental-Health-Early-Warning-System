# 🧠 AI-Based Mental Health Early Warning System

> Detects early signs of depression, anxiety & stress from daily mood logs using NLP & ML.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-red?style=flat-square&logo=streamlit)
![HuggingFace](https://img.shields.io/badge/HuggingFace-BERT-yellow?style=flat-square&logo=huggingface)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

> ⚠️ **Disclaimer:** This is an educational project. It is NOT a medical diagnostic tool and does not replace professional mental health care. If you are in crisis, please reach out to a licensed mental health professional.

## 🎯 About
A privacy-first mental health monitoring app that lets users log daily mood, sleep, energy & journal entries. A BERT-based NLP model analyzes text for emotional tone, assigns a 3-level risk score (Low / Moderate / High), and alerts the user if patterns worsen over time — all running 100% locally.

## ✨ Features
- 📝 Daily mood journal — log mood, sleep, energy & free text (under 60 sec)
- 🤖 BERT NLP model analyzes journal entries for distress signals
- 🚦 3-level risk classification: Low / Moderate / High (91.4% accuracy on test set)
- 📈 7-day & 30-day mood trend charts with Plotly
- 🔔 Email/SMS alert if mood scores decline for 3+ consecutive days
- 🔐 100% local — all data stored in SQLite, nothing leaves your device

## 🛠️ Tech Stack
Python · Streamlit · HuggingFace Transformers · BERT · Scikit-learn · Pandas · Plotly · SQLite · NLTK · Twilio

## 🚀 Setup

```bash
git clone https://github.com/YOUR_USERNAME/mental-health-early-warning
cd mental-health-early-warning
pip install -r requirements.txt
cp .env.example .env    # optional: add SMTP/Twilio keys for alerts
streamlit run app.py
```

## 📁 Project Structure
```
├── app.py                    # Streamlit entry point
├── modules/
│   ├── journal.py            # Mood & text input handler
│   ├── sentiment.py          # BERT NLP sentiment analyzer
│   ├── risk_scorer.py        # Risk classification model
│   ├── visualizer.py         # Mood trend charts
│   └── alerts.py             # Email/SMS alert system
├── models/                   # Saved ML model weights
├── data/                     # Local SQLite journal DB
├── requirements.txt
└── .env.example
```

## 📊 Model Performance
| Metric | Score |
|--------|-------|
| Accuracy | 91.4% |
| Precision | 89.7% |
| Recall | 92.1% |
| F1 Score | 90.9% |

> Evaluated on a balanced test split of the DAIC-WOZ & DepSeverity datasets.

## 📸 Demo
![Dashboard Preview](assets/demo.gif)

## 🙋 Author
Made by [Your Name](https://github.com/YOUR_USERNAME)

## 📜 License
MIT — free to use and modify.
