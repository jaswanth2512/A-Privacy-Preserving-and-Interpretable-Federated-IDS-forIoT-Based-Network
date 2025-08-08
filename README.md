Yes, I remember your **Computer Security research paper** project (e.g., **"A Privacy-Preserving and Interpretable Federated IDS for IoT-Based Networks (XFedIDS+)"**) that involves:

* CNN-LSTM based Federated Intrusion Detection System
* FedAvg + FedProx optimization
* CRADS client selection
* SHAP & LIME explainability
* Raspberry Pi deployment
* IoT datasets (UNSW-NB15, IoT-23)
* Real-world testbed and Differential Privacy


---

````markdown
# XFedIDS+: A Privacy-Preserving and Interpretable Federated IDS for IoT-Based Networks

![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.10+-blue)
![Framework](https://img.shields.io/badge/framework-TensorFlow%20%7C%20FL%20Sim-yellow)

## 📌 Overview

**XFedIDS+** is a federated learning-based Intrusion Detection System (IDS) designed for **IoT-based networks**, providing:
- **High detection accuracy**
- **Privacy preservation** (via Federated Learning and Differential Privacy)
- **Model interpretability** (via SHAP and LIME)
- **Raspberry Pi testbed deployment**
- **Client selection optimization** (CRADS)
- **Multi-dataset evaluation** (UNSW-NB15 & IoT-23)

This repository contains full source code, training scripts, deployment pipeline, and SHAP/LIME visualizations for publication-ready research.

---

## 📂 Datasets Used

| Dataset     | Best Model | Accuracy | Notable Columns Used |
|-------------|------------|----------|-----------------------|
| UNSW-NB15   | CNN-LSTM   | 89.27%   | `srcip`, `dstip`, `proto`, `service`, `state`, `dbytes`, `sbytes`, `attack_cat` |
| IoT-23 (CICFlow) | CNN-LSTM | 87.11% | `Flow Duration`, `Total Fwd Packets`, `Fwd Packet Length Mean`, `Label` |

> ✅ All datasets were preprocessed to maintain balanced class distributions and federated client partitions.

---

## 🏗️ Architecture

- CNN-LSTM intrusion classifier  
- FedAvg + FedProx algorithm  
- CRADS (Client Ranking and Dynamic Selection)
- SHAP + LIME for explainability  
- Differential Privacy noise addition (ε-differential)

![Architecture Diagram](docs/xfedids_architecture.png)

---

## 🚀 Features

- ✅ Federated Learning with Proximal Loss  
- ✅ Real-world IoT deployment on Raspberry Pi  
- ✅ SHAP & LIME interpretability  
- ✅ Client dropout and CRADS selection  
- ✅ Performance metrics (Accuracy, Precision, Recall, F1, ROC-AUC)  
- ✅ Batch and Real-time Inference  

---

## ⚙️ Setup Instructions

```bash
# Clone the repo
git clone https://github.com/your-username/XFedIDS.git
cd XFedIDS

# Install dependencies
pip install -r requirements.txt
````

For Raspberry Pi deployment, follow the instructions in `deployment/raspberrypi_inference.py`.

---

## 📊 Evaluation Metrics

| Dataset   | Accuracy | Recall | F1 Score | ROC-AUC |
| --------- | -------- | ------ | -------- | ------- |
| UNSW-NB15 | 89.27%   | 96.21% | 91.75%   | 0.94    |
| IoT-23    | 87.11%   | 97.00% | 88.27%   | 0.92    |

---

## 📈 SHAP and LIME Interpretability

![SHAP Summary](docs/shap_summary_unsw.png)

> SHAP summary for UNSW-NB15 showing top features influencing predictions

![LIME Explanation](docs/lime_iot23.png)

> LIME local explanation on IoT-23 binary classification

---

## 🧪 Real-World Testbed

* 📍 **Device:** Raspberry Pi 4 Model B (4GB RAM)
* 📡 Connected via Ethernet to simulate IoT gateway
* 🧠 TFLite Model: `cnn_lstm_fp.tflite`
* ⏱️ Average Inference Latency: **27 ms**

---

## 🧾 File Structure

```
XFedIDS/
├── data/                   # Preprocessed dataset splits
├── models/                 # CNN-LSTM architectures
├── federated/              # FedAvg, FedProx, CRADS code
├── explainability/         # SHAP and LIME analysis
├── deployment/             # Raspberry Pi inference scripts
├── results/                # Evaluation results and plots
├── utils/                  # Helper functions
└── main.py                 # Main federated training script
```

---

## 📜 Citation

If you use this work, please cite the following paper:

```bibtex
@inproceedings{xfedids2025,
  title     = {A Privacy-Preserving and Interpretable Federated IDS for IoT-Based Networks},
  booktitle = {Proceedings of the ICCCNT 2025},
  year      = {2025}
}
```

---


## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

```

Let me know if you'd like a version with GitHub badges, links, images, or demo video integration. I can also generate `requirements.txt`, `architecture.png`, and actual SHAP plots if needed.
```
