# LLM-Assisted Intelligent Network Intrusion Detection System (IDS)

A hybrid **Machine Learning + Large Language Model (LLM)** based Network Intrusion Detection System designed to detect malicious network traffic and provide human-readable explanations of detected attacks.

## 📌 Project Overview

Traditional Intrusion Detection Systems can identify suspicious network traffic, but their outputs are often difficult for users to understand.

This project combines a **Random Forest machine learning classifier** with a **Large Language Model (LLM)** to provide both:

* Automated network attack detection
* Human-readable explanations of detected threats
* Attack severity assessment
* Recommended mitigation actions

The machine learning model performs the actual traffic classification, while the LLM converts the prediction and relevant network information into an understandable security explanation.

## 🏗️ System Architecture

```text
Network Traffic
      ↓
Data Preprocessing
      ↓
Feature Selection
      ↓
Random Forest Classifier
      ↓
Attack / Benign Prediction
      ↓
LLM Analysis
      ↓
Threat Explanation
      ↓
Severity + Recommended Action
```

## 🚀 Key Features

* Network intrusion detection using Machine Learning
* Random Forest based classification
* Binary traffic classification (Benign / Attack)
* Feature selection for efficient prediction
* Handling of imbalanced network traffic
* LLM-assisted threat explanation
* Attack severity assessment
* Recommended mitigation actions
* SHAP-based model explainability
* Confusion matrix and performance evaluation
* Model saving and loading using Joblib

## 🧠 Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Random Forest**
* **Joblib**
* **Ollama**
* **Jupyter Notebook**

## 📊 Dataset

The project uses the **CICIDS2017** dataset for network intrusion detection.

The dataset contains realistic network traffic with both benign and malicious activities.

The data is processed through:

1. Data cleaning
2. Duplicate removal
3. Label encoding
4. Feature selection
5. Train-test splitting
6. Model training
7. Performance evaluation

## 🔍 Machine Learning Model

A **Random Forest Classifier** is used as the primary intrusion detection model.

The model learns patterns from network traffic features and predicts whether the traffic is:

* **BENIGN**
* **ATTACK**

Selected network features include:

* Destination Port
* Average Packet Size
* Flow IAT Min
* Fwd IAT Min
* Bwd Packets/s
* Total Length of Fwd Packets
* Subflow Fwd Bytes
* Fwd Header Length
* Bwd Packet Length Std
* act_data_pkt_fwd

## 🤖 LLM Integration

After the machine learning model detects an attack, the prediction and relevant traffic information are provided to a locally running LLM using **Ollama**.

The LLM generates:

* Detected attack type
* Threat severity
* Explanation of the attack
* Possible security implications
* Recommended mitigation actions

### Example

```text
Prediction: Port Scan

Severity: Medium

Explanation:
The detected traffic pattern indicates scanning activity
where multiple ports may be probed to identify available
network services.

Recommended Action:
Monitor the source IP, restrict unnecessary exposed ports,
and investigate repeated scanning activity.
```

## 📈 Explainability

The project also explores model explainability using **SHAP (SHapley Additive exPlanations)**.

SHAP helps identify which network traffic features contributed most to the model's prediction.

This makes the IDS more transparent and easier to analyze.

## 📂 Project Structure

```text
LLM-with-IDS/
│
├── final_level.ipynb
├── final_level (8).ipynb
└── README.md
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/bprakhar428-source/LLM-with-IDS.git
```

Navigate to the project directory:

```bash
cd LLM-with-IDS
```

Install the required Python libraries:

```bash
pip install pandas numpy scikit-learn imbalanced-learn shap joblib
```

For LLM integration, install **Ollama** and download a supported local model.

## ▶️ Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
final_level.ipynb
```

Run the notebook cells sequentially to perform preprocessing, model training/evaluation, prediction, and LLM-based explanation.

## 📊 Evaluation

The system can be evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Feature Importance
* SHAP Explainability

## 🔮 Future Improvements

* Real-time network traffic monitoring
* Multi-class attack classification
* Integration with live packet capture
* Web-based security dashboard
* Automated alert generation
* Improved LLM-based threat analysis
* Integration with SIEM systems
* Deployment as a real-time security service

## 👨‍💻 Author
**Prakhar Bajpai**

# co-Author
**sudhanshu Dubey**

B.Tech — Computer Science & Engineering

---

## ⭐ Project Highlights

This project demonstrates the integration of **Machine Learning, Network Security, Explainable AI, and Large Language Models** to build a more understandable and intelligent Intrusion Detection System.
