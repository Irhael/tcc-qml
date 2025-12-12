# Quantum vs. Classical Machine Learning: A Comparative Performance Analysis

This repository contains the source code, datasets, and experimental results for the Bachelor's Thesis submitted to the Institute of Computing at Fluminense Federal University (UFF).

## Overview

This research compares the performance of Classical Machine Learning algorithms against Quantum Machine Learning (QML) models in binary classification tasks. The study investigates the impact of dimensionality reduction techniques on quantum models using Quantum simulation.

**Author:** Irhael Sousa das Chagas
**Advisor:** Prof. Luis Antonio Kowada
*CoAdvisor:** Gabriela Pinheiro
**Institution:** Universidade Federal Fluminense (UFF)

## Datasets

Two datasets with distinct characteristics were selected to evaluate model robustness:

1.  **Breast Cancer Wisconsin (Diagnostic):** Represents a well-structured, balanced dataset with high linear separability.
2.  **Student Performance:** Represents a complex, noisy, and highly imbalanced dataset derived from social data.

## Methodology

### 1. Preprocessing
* **One-Hot Encoding:** Applied to categorical variables.
* **Normalization:** StandardScaler (fit on training set, applied to test set).
* **Data Balancing:** SMOTE (Synthetic Minority Over-sampling Technique) applied exclusively to the training set of the Student Performance dataset.

### 2. Dimensionality Reduction
Due to the computational cost of simulating quantum circuits (statevector simulation), the feature space was reduced to 5 dimensions using:
* **Correlation-based Feature Selection:** Selecting features with the highest Pearson correlation to the target.
* **Principal Component Analysis (PCA):** Extracting the top 5 orthogonal components.

### 3. Models Evaluated
**Classical Models:**
* Support Vector Machine (SVM) - RBF Kernel
* Random Forest (Ensemble)
* Multi-layer Perceptron (MLP)

**Quantum Models (Qiskit):**
* Quantum Support Vector Machine (QSVM) - using ZZFeatureMap
* Quantum Neural Network (QNN/VQC) - using RealAmplitudes Ansatz

## Installation and Usage

To reproduce the experiments, it is recommended to use a virtual environment.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Irhael/tcc-qml.git](https://github.com/Irhael/tcc-qml.git)
    cd tcc-qml
    ```

2.  **Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the experiments:**
    The experiments are structured as Jupyter Notebooks. Start the server with:
    ```bash
    jupyter notebook
    ```

## Key Technologies

* **Python 3.8+**
* **Qiskit & Qiskit Machine Learning:** For quantum circuit simulation and QML algorithms.
* **Scikit-learn:** For classical models, preprocessing, and metrics.
* **Pandas & NumPy:** For data manipulation.
* **Matplotlib & Seaborn:** For data visualization.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
* Quantum Neural Network (QNN/VQC) - using RealAmplitudes Ansatz


