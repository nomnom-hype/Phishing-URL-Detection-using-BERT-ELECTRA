# 🔐 Phishing URL Detection using BERT & ELECTRA

Security-focused project for detecting malicious URLs (Phishing, Malware, Defacement) using Transformer-based models. This repository presents a **comparative analysis of BERT vs ELECTRA**, emphasizing **security-critical metrics** such as Recall and F1-score.

---

## 📌 Project Overview

Malicious URLs are a primary attack vector for phishing, malware distribution, and website defacement.  
Rule-based systems fail against obfuscation and evolving attack patterns.

This project applies **Transformer-based deep learning models** to classify URLs into four categories:

- Benign  
- Defacement  
- Malware  
- Phishing  

The study highlights why **ELECTRA** is better suited than **BERT** for security detection tasks.

---

## 🧠 Models Used

| Model | Description |
|------|-------------|
| **BERT (bert-base-cased)** | Baseline transformer using Masked Language Modeling |
| **ELECTRA (electra-base-discriminator)** | Discriminator-based transformer optimized for anomaly detection |

---

## 🧪 Dataset

- URL-based malicious dataset  
- Balanced across 4 classes  
- Tokenization performed directly on raw URLs  
- Preprocessed for transformer-based classification  

---

## 📊 Results & Performance

### 🔹 BERT Results
- **Best Epoch:** 4  
- **Accuracy:** ~97.8%  
- **Precision (weighted):** ~0.978  
- **Recall (weighted):** ~0.978  
- **F1-score (weighted):** ~0.978  

**Observation:**  
BERT provides strong baseline performance but shows early signs of overfitting and slightly lower recall for phishing and malware classes.

---

### 🔹 ELECTRA Results
- **Best Epoch:** 4  
- **Accuracy:** ~98.1%  
- **Precision (weighted):** ~0.979  
- **Recall (weighted):** ~0.979  
- **F1-score (weighted):** ~0.981  

**Observation:**  
ELECTRA consistently outperforms BERT, achieving higher F1-score and recall while converging faster and generalizing better.

---

### ⚖️ BERT vs ELECTRA (Final Comparison)

| Metric | BERT | ELECTRA |
|------|------|---------|
| Best Accuracy | ~97.8% | **~98.1%** |
| Best F1-score | ~0.978 | **~0.981** |
| Phishing Recall | Good | **Better** |
| Malware Recall | Good | **Better** |
| Convergence Speed | Slower | **Faster** |

> ✅ ELECTRA reduces **false negatives**, which is critical for real-world security systems.

---

## 🔍 Confusion Matrix Insights

- Both models show strong diagonal dominance  
- ELECTRA misclassifies fewer phishing URLs as benign  
- Improved malware detection with ELECTRA  

---

## 🛡️ Why ELECTRA for Security?

- Trained as a **token-level discriminator**
- Better at detecting:
  - Obfuscated URLs
  - Random / anomalous patterns
  - Typosquatting attacks
- More suitable for **cybersecurity classification tasks** than MLM-based models

---

## 📌 Future Enhancements

- Add DeBERTa for advanced comparison  
- Perform adversarial URL testing  
- Deploy as a REST API (FastAPI)  
- Integrate with SIEM / SOC pipelines  

---

## 👤 Author

**Om Balmukund Pardhi**  
AI Software Developer  

---

⭐ If you find this project useful, consider starring the repository.
