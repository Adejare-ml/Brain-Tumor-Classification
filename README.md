# 🧠 Med-Brain Tumor Classification Benchmark
**Comparative Analysis of Vision Transformers (ViT) vs. DINOv2 with Grad-CAM Explainability**

[![PyTorch](https://img.shields.io/badge/ML-PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](https://pytorch.org/)
[![Scikit-Learn](https://img.shields.io/badge/Analysis-Scikit--Learn-F7B12F?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

## 🔬 Executive Summary
This repository presents a rigorous technical benchmark comparing the efficacy of standard Vision Transformers (ViT) against the self-supervised DINOv2 architecture for the classification of brain tumors from MRI scans. 

The primary objective is to determine if self-supervised pre-training on large-scale datasets (DINOv2) provides superior feature extraction capabilities in specialized medical domains compared to traditional supervised transformer baselines.

### 🏗️ Technical Core
- **Architecture Comparison:**
    - **ViT-B/32:** Baseline transformer model analyzing global image dependencies.
    - **DINOv2:** Leveraging emergent properties from self-supervised learning to extract robust, high-level anatomical features without requiring exhaustive medical labeling.
- **Explainability (XAI):** Integrated **Grad-CAM (Gradient-weighted Class Activation Mapping)** to visualize the model's "attention" regions, ensuring that classification decisions are based on actual tumor pathology rather than imaging artifacts.
- **Evaluation Metric:** Benchmarked using Accuracy, F1-Score, and a detailed Classification Report.

---

## 📂 Repository Engineering
The project is structured as a research benchmark suite to maximize reproducibility.

```text
├── research/               # Core Benchmark Analysis
│   ├── benchmark_comparison_main.ipynb # Final ViT vs DINOv2 comparison
│   ├── dinov2_implementation.ipynb     # DINOv2 pipeline & results
│   ├── vit_b32_baseline.ipynb          # Baseline transformer analysis
│   ├── rvit_analysis.ipynb              # Recursive ViT experiments
│   └── test_suite_prototype.ipynb      # Validation and sanity checks
├── data/                   # Dataset Artifacts
│   └── combined_dataset_v1.csv         # Normalized MRI metadata
├── results/                # Performance Metrics
│   └── classification_report.txt       # Final precision/recall/f1 metrics
├── model_weights/          # Serialized Model States
│   └── hornet_tiny_gf.pth              # Optimized weight checkpoints
└── assets/                     # Visualization & Explainability
```

---

## 🚀 Research Workflow

### 1. Environment Setup
```bash
git clone https://github.com/Adejare-ml/med-brain-tumor-classification.git
cd med-brain-tumor-classification
pip install torch torchvision torchaudio pandas matplotlib scikit-learn captum
```

### 2. Analysis Execution
The research is conducted primarily within the `research/` directory. To reproduce the benchmark results:
1. Run `vit_b32_baseline.ipynb` to establish the performance floor.
2. Run `dinov2_implementation.ipynb` to evaluate the self-supervised lift.
3. Refer to `benchmark_comparison_main.ipynb` for the aggregated synthesis.

---

## 🛠 Engineering Stack
| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Deep Learning** | PyTorch | Model implementation and training |
| **Vision Backbone** | ViT / DINOv2 | State-of-the-art feature extraction |
| **Explainability** | Grad-CAM / Captum | Visualizing model decision-making |
| **Analysis** | Pandas / NumPy | Data manipulation and metric calculation |
| **Visualization** | Matplotlib / Seaborn | Generating heatmaps and confusion matrices |

---
**Maintainer:** [Adelugba Adejare](https://github.com/Adejare-ml)
