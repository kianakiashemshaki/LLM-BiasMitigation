# LLM-BiasMitigation

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8+-brightgreen.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C.svg?logo=pytorch&logoColor=white)](https://pytorch.org/)
[![Hugging Face](https://img.shields.io/badge/Transformers-🤗-yellow.svg)](https://huggingface.co/transformers/)

---

## 📖 Overview
Large Language Models (LLMs) have transformed Natural Language Processing (NLP), but they often reproduce biases that threaten fairness and trust.  
This project provides a simulation framework to evaluate and mitigate bias in LLMs using multiple strategies at the data, model, and post-processing levels.

The repository contains:
- 💻 **Code**: Python / Jupyter implementation with experiments on the Bias in Bios dataset  
- 📊 **Evaluation**: Fairness metrics (Demographic Parity, Equalized Odds) alongside accuracy and F1 scores  

---

## ✨ Key Features
- **Bias Simulation Framework** for gender and profession classification
- **Preprocessing pipeline** for text normalization and tokenization with BERT
- **Fairness-aware experiments**:
  - Data-level: Random oversampling
  - Model-level: Class-weighted loss
  - Post-processing: Equalized Odds threshold optimization
- **Evaluation metrics**: Accuracy, Macro-F1, Demographic Parity Difference (DPD), Equalized Odds Difference (EOD)
- **Reproducible Jupyter Notebook** for running experiments


---

### 🛠️ Installation & Setup

#### Clone the repository:
git clone https://github.com/kianakiashemshaki/LLM-BiasMitigation.git
cd LLM-BiasMitigation

#### Create and activate a virtual environment:
python -m venv venv
source venv/bin/activate   
On Windows: venv\Scripts\activate

#### Install dependencies:
pip install -r requirements.txt

#### Run the main notebook:
jupyter notebook bias_mitigation_simulation.ipynb


---

## 📊 Results (Summary)

| **Task**              | **Method**          | **Accuracy** | **Macro-F1** | **DPD** | **EOD** |
|-----------------------|---------------------|--------------|--------------|---------|---------|
| **Gender Prediction** | Baseline            | 0.995        | 0.994        | 0.98    | 0.99    |
|                       | Oversampling        | 0.994        | 0.993        | 0.40    | 0.42    |
|                       | Class Weighting     | 0.994        | 0.993        | 0.50    | 0.52    |
|                       | Equalized Odds      | 0.993        | 0.992        | 0.32    | 0.34    |
| **Profession Prediction** | Baseline        | 0.940        | 0.930        | 0.90    | 0.92    |
|                       | Oversampling        | 0.935        | 0.928        | 0.45    | 0.48    |
|                       | Class Weighting     | 0.937        | 0.929        | 0.55    | 0.58    |
|                       | Equalized Odds      | 0.933        | 0.925        | 0.40    | 0.43    |

---

## 📄 Paper & 📚 Citation

The full research paper is available in this repository:  
👉 Simulating a Bias Mitigation Scenario in Large Language Models (paper.pdf)

If you use this work in your research, please cite:

@article{kiashemshaki2025bias,
  title={Simulating a Bias Mitigation Scenario in Large Language Models},
  author={Kiashemshaki, Kiana},
  year={2025}
}





