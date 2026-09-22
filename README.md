# Quantum-Inspired Reservoir (QIR) for Quantum Network State Estimation

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

An advanced quantum-inspired machine learning framework for predicting dynamic non-linear noise and estimating entanglement fidelity in quantum network channels using **Orthogonal Unitary Reservoir Computing**.

---

## 📌 Interactive Notebooks (Run in Google Colab)

| Notebook | Description | Google Colab |
| :--- | :--- | :---: |
| **01. Data Generation** | Simulation of non-linear phase and amplitude damping noise. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AmirKabirian/quantum-network-reservoir-estimation/blob/main/notebooks/01_data_generation.ipynb) |
| **02. QIR Architecture** | Implementation of PyTorch Orthogonal Unitary Reservoir Layer. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AmirKabirian/quantum-network-reservoir-estimation/blob/main/notebooks/02_qir_architecture.ipynb) |
| **03. State Estimation Demo** | End-to-end training and evaluation pipeline for fidelity estimation. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AmirKabirian/quantum-network-reservoir-estimation/blob/main/notebooks/03_state_estimation_demo.ipynb) |

---

## 🧬 Theoretical Overview

The core architecture utilizes **orthogonal matrix decomposition** ($U^\dagger U = I$) to enforce unitary dynamics inside the reservoir state transitions:

$$h_t = (1 - \alpha) h_{t-1} + \alpha \tanh(W_{in} x_t + W_{res} h_{t-1})$$

Where $W_{res}$ is generated using Haar-random orthogonal matrices, preventing vanishing gradients and preserving temporal quantum sequence memory efficiently without full quantum gate simulation overhead.

---

## 🛠 Repository Structure

```text
quantum-network-reservoir-estimation/
│
├── notebooks/
│   ├── 01_data_generation.ipynb       # Quantum noise simulation
│   ├── 02_qir_architecture.ipynb     # QIR PyTorch layer implementation
│   └── 03_state_estimation_demo.ipynb # Full pipeline & evaluation
│
├── .gitignore
├── LICENSE                            # MIT License
├── README.md                          # Project Documentation
└── requirements.txt                   # Dependency list
