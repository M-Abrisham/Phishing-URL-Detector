# 🎣 Phishing URL Detector

> 🛡️ A Machine Learning-powered scanner to detect phishing URLs and keep you safe online.

[![Python](https://img.shields.io/badge/Python-3.7+-blue?logo=python&logoColor=white)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## 📖 Overview

This detector uses a **RandomForestClassifier** model trained on the [Kaggle Phishing URL Dataset](https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset) to identify malicious URLs with **85.7% accuracy**.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔍 **URL Analysis** | Extracts 11 key features from URLs |
| 🤖 **ML Classification** | RandomForest model for accurate detection |
| ⚡ **Real-time Scanning** | Instantly check suspicious URLs |
| 📊 **Feature Importance** | Understand what makes a URL suspicious |

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/AI-Based-URL-phishing-detection.git

# Install dependencies
pip install -r requirements.txt

# Run the scanner
python phishing_scanner.py
```

---

## 🔬 How It Works

The model extracts these features from each URL:

| Feature | Importance | Description |
|---------|------------|-------------|
| `digit_count` | 22.88% | Number of digits in URL |
| `url_length` | 22.68% | Total length of URL |
| `slash_count` | 13.57% | Number of `/` characters |
| `has_suspicious_words` | 11.45% | Contains words like "login", "secure" |
| `dot_count` | 10.69% | Number of `.` characters |
| `dash_count` | 9.37% | Number of `-` characters |
| `subdomain_count` | 5.31% | Number of subdomains |
| `has_ip` | 1.98% | URL contains IP address |
| `risky_tld` | 1.71% | Uses suspicious TLD |
| `at_count` | 0.35% | Number of `@` characters |
| `is_https` | 0.00% | Uses HTTPS protocol |

---

## 📊 Model Performance

```
📈 Dataset Size: 549,346 URLs
├── Training: 439,476 samples
└── Testing:  109,870 samples

🎯 Overall Accuracy: 85.66%
```

### Confusion Matrix

| | Predicted Safe | Predicted Phishing |
|---|:---:|:---:|
| **Actually Safe** | ✅ 69,521 | ⚠️ 9,064 |
| **Actually Phishing** | ❌ 6,694 | 🎯 24,591 |

---

## 💻 Example Usage

```
Enter Suspicious URL: http://google.com.cust_login.ie

🚨 ALERT >> PHISHING URL DETECTED!
```

---

## ⚠️ Disclaimer

This tool is for educational purposes. While it achieves good accuracy, no detection system is 100% reliable. Always exercise caution with unfamiliar URLs.

---

## 📄 License

MIT License - feel free to use and modify!
