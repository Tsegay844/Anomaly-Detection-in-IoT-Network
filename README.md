<div align="center">

# Machine Learning Techniques for Anomaly Detection in IoT

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-green.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-Academic-yellow.svg)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT)](https://github.com/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT/commits/main)
[![Repository Size](https://img.shields.io/github/repo-size/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT)](https://github.com/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT)

*Data Mining and Machine Learning Project @ University of Pisa*

[View Demo](https://github.com/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT) · [Report Bug](https://github.com/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT/issues) · [Request Feature](https://github.com/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT/issues)

</div>

---

## About The Project

This repository presents a comprehensive research project implementing **seven state-of-the-art machine learning algorithms** for anomaly detection in Internet of Things (IoT) environments. Developed as part of the Data Mining and Machine Learning curriculum at the University of Pisa, this project addresses the critical challenge of identifying anomalous patterns in IoT sensor data that may indicate security breaches, equipment failures, or system malfunctions.

### Key Objectives

- **Comparative Analysis**: Evaluate multiple ML algorithms for IoT anomaly detection
- **Data Preprocessing**: Implement advanced preprocessing techniques including SMOTE balancing
- **Performance Optimization**: Achieve optimal classification performance through feature engineering
- **Academic Excellence**: Demonstrate mastery of machine learning concepts and implementations

---

## Built With

This project leverages cutting-edge technologies and libraries:

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge)](https://matplotlib.org/)

### Core Dependencies

- **Python 3.8+**: Programming language
- **Jupyter Notebook**: Interactive development environment
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing foundation
- **Scikit-learn**: Machine learning algorithms and tools
- **Matplotlib & Seaborn**: Advanced data visualization
- **Imbalanced-learn**: SMOTE implementation for data balancing

---

## Getting Started

Follow these steps to get the project running on your local machine.

### Prerequisites

Ensure you have Python 3.8 or higher installed:

```bash
python --version
```

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Tsegay844/Machine-Learning-techniques-for-Anomaly-Detection-in-IoT.git
   cd Machine-Learning-techniques-for-Anomaly-Detection-in-IoT
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**
   ```bash
   # Windows
   venv\Scripts\activate
   
   # macOS/Linux
   source venv/bin/activate
   ```

4. **Install required packages**
   ```bash
   pip install jupyter pandas numpy scikit-learn matplotlib seaborn imbalanced-learn
   ```

5. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

---

## Usage

### Quick Start

1. **Start with the Table of Contents**
   ```bash
   jupyter notebook Table_of_contents.ipynb
   ```

2. **Follow the structured workflow:**
   - **Data Exploration**: Understand dataset characteristics
   - **Preprocessing**: Clean data and engineer features
   - **Model Training**: Train seven different algorithms
   - **Evaluation**: Analyze and compare performance



---

## 📁 Project Structure

```
📦 Machine-Learning-techniques-for-Anomaly-Detection-in-IoT/
├── 📄 README.md                          # Project documentation
├── 📄 Table_of_contents.ipynb           # Project navigation hub
├── 📁 dataset/                          # Processed datasets
│   ├── 📄 X_train_balanced.csv         # Balanced training features
│   ├── 📄 y_train_balanced.csv         # Balanced training labels
│   ├── 📄 X_test.csv                   # Test features
│   └── 📄 y_test.csv                   # Test labels
├── 📁 models/                           # Model development
│   └── 📄 Model-1-SMOTE&Outlier.ipynb  # Main modeling notebook
├── 📁 preprocesing/                     # Data preprocessing
│   └── 📄 Preprocessing.ipynb          # Data preparation pipeline
└── 📁 conf/                            # Configuration files
    ├── 📄 list_of_models.ipynb         # Model configurations
    └── 📄 list_of_performance_evaluations.ipynb
```
### Example Code

```python
# Quick model evaluation example
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report

# Load preprocessed data
X_train = pd.read_csv('dataset/X_train_balanced.csv')
y_train = pd.read_csv('dataset/y_train_balanced.csv')

# Train Random Forest
rf_model = RandomForestClassifier(random_state=42)
rf_model.fit(X_train, y_train)

# Evaluate performance
predictions = rf_model.predict(X_test)
print(classification_report(y_test, predictions))
```

---

## Machine Learning Models

### Model Performance Overview

| Model | Accuracy | Type | Key Features |
|-------|----------|------|--------------|
| **Decision Tree** | 100.0% | Tree-based | Interpretable rules |
| **Random Forest** | 100.0% | Ensemble | Multiple tree voting |
| **Gradient Boosting** | 100.0% | Ensemble | Sequential improvement |
| **Multi-Layer Perceptron** | 100.0% | Neural Network | Deep learning approach |
| **k-Nearest Neighbors** | 99.9% | Instance-based | Distance-based classification |
| **Naive Bayes** | 97.0% | Probabilistic | Feature independence assumption |
| **Rule-Based** | 100.0% | Logic-based | Expert system approach |

### Model Architectures

#### Multi-Layer Perceptron (MLP)
```python
MLPClassifier(
    hidden_layer_sizes=(100, 50, 25),
    max_iter=1000,
    random_state=42,
    learning_rate_init=0.001
)
```

#### Random Forest Configuration
```python
RandomForestClassifier(
    n_estimators=100,
    random_state=42,
    max_depth=None
)
```

---

## Performance Results

### Cross-Validation Results

<div align="center">

| Model | CV Accuracy | Precision | Recall | F1-Score |
|-------|-------------|-----------|--------|----------|
| Decision Tree | **100.0%** | 1.00 | 1.00 | 1.00 |
| Random Forest | **100.0%** | 1.00 | 1.00 | 1.00 |
| Gradient Boosting | **100.0%** | 1.00 | 1.00 | 1.00 |
| MLP Neural Network | **100.0%** | 1.00 | 1.00 | 1.00 |
| k-Nearest Neighbors | **99.9%** | 0.99 | 1.00 | 1.00 |
| Naive Bayes | **97.0%** | 0.69 | 0.99 | 0.81 |
| Rule-Based | **100.0%** | 1.00 | 1.00 | 1.00 |

</div>

### Key Achievements

-  **Perfect Classification**: 5 out of 7 models achieved 100% accuracy
-  **Robust Performance**: All models exceeded 97% accuracy
-  **Excellent Recall**: Superior anomaly detection capabilities
-  **Balanced Metrics**: High precision and recall across all models

---


This project is part of academic research conducted at the **University of Pisa**. 

-  **Course**: Data Mining and Machine Learning
-  **Institution**: University of Pisa
-  **Year**: 2024
-  **Program**: Artificial Inteligence and Data Engineering 

---

