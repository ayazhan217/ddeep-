# ddeep-
# Deep Learning — Homework 1
### Introduction, Optimization, and Convolutional Neural Networks

## Overview

This submission implements all required parts of Homework 1 using **PyTorch**:

- **Problem 1** — MLPs: flexible implementation, activation function comparison, XOR
- **Problem 2** — Optimization: optimizer comparison, vanishing-gradient analysis, regularization effects
- **Problem 3** — CNNs: CIFAR-10 classifier, architecture comparison, learned-feature visualization

Datasets: **MNIST** (Problems 1–2), **CIFAR-10** (Problem 3).
Random seed fixed at `42` throughout for reproducibility.

## Contents

| File | Description |
|---|---|
| `Deep_Learning_Homework_1_Solution.ipynb` | Full, runnable notebook with all code, training runs, and generated plots |
| `Deep_Learning_Homework_1_Report.docx` / `.pdf` | Written report: results, tables, plots, and brief analyses for every part |
| `requirements.txt` | Python dependencies |
| `README.md` | This file |

## Setup

```bash
pip install -r requirements.txt
```

MNIST and CIFAR-10 are downloaded automatically via `torchvision.datasets` on first run.

## Running

Open and run all cells in the notebook, top to bottom:

```bash
jupyter notebook Deep_Learning_Homework_1_Solution.ipynb
```

The notebook is organized to mirror the assignment structure (Problem 1 → 2 → 3, Parts A/B/C), and saves all generated figures as `.png` files in the working directory. Runtime is CPU-friendly, though a GPU will speed up Problem 3 (CIFAR-10 CNN training) considerably.

## Results Summary

| Task | Metric | Result |
|---|---|---|
| P1A — MLP (784→128→64→10) | Test accuracy | 97.67% |
| P1B — Best activation (Tanh) | Test accuracy | 97.77% |
| P1C — XOR MLP | Accuracy | 100% (4/4) |
| P2A — Best optimizer (SGD + Momentum) | Test accuracy | 98.14% |
| P2B — Vanishing gradients (Sigmoid vs. ReLU) | Grad(L1)/Grad(L8) at init | 1.37e-04 vs. 1.88e+00 |
| P2C — Best regularizer (Dropout, p=0.5) | Train–test gap | 0.67% |
| P3A — Basic CNN (CIFAR-10) | Test accuracy | 69.95% |
| P3B — Best architecture (deeper/wider) | Test accuracy | 73.02% |

Full tables, plots, and written analysis for each result are in the report.


