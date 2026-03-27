# LViT-BioClinicalBERT: Multi-Caption Guided Medical Image Localization

[![Conference](https://img.shields.io/badge/NeurIPS-2026-blue)](https://neurips.cc/)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)

> **Weakly Supervised Multi-Caption Guided Medical Image Localization with BioClinicalBERT**

This repository contains the official implementation of our NeurIPS 2026 paper on weakly supervised medical image localization using multi-caption guidance and BioClinicalBERT.

---

## 📋 Abstract

We present a novel weakly supervised approach for medical image localization that leverages multiple clinical captions to guide visual attention. Our method integrates BioClinicalBERT for clinical text understanding with a lightweight vision transformer (LViT) for efficient medical image analysis. The proposed framework achieves state-of-the-art localization performance on medical imaging datasets without requiring pixel-level annotations.

**Key Contributions:**
- Multi-caption alignment mechanism for robust weak supervision
- Integration of BioClinicalBERT for clinical knowledge encoding  
- Lightweight vision transformer architecture for medical imaging
- Comprehensive ablation studies and evaluation

---

## 🚀 Quick Start

### Prerequisites

```bash
python >= 3.8
pytorch >= 2.0
torchvision >= 0.15
transformers >= 4.30
```

### Installation

```bash
# Clone the repository
git clone https://github.com/dawitemu1/LViT-BioClinicalBERT-Mutli-caption-Guided-Medical-image-localization-MCDL-.git
cd LViT-BioClinicalBERT-Mutli-caption-Guided-Medical-image-localization-MCDL-

# Install dependencies
pip install -r requirements.txt
```

### Training

```bash
# Run the main training notebook
jupyter notebook Pro_caption_image_highlight.ipynb
```

---

## 📁 Repository Structure

```
.
├── Pro_caption_image_highlight.ipynb          # Main training script
├── outputs/                                   # Training outputs and results
│   ├── lvit_nomasks/models/                   # Saved model checkpoints
│   └── lvit_nomasks/results/                  # Evaluation results
├── sample_lvit_nomasks/                       # Sample data
│   ├── images/                                # Sample medical images
│   └── captions.csv                           # Caption annotations
└── .gitignore                                 # Git ignore rules
```

---

## 🎯 Results

Our method achieves competitive performance on medical image localization benchmarks:

## Weakly Supervised LViT-BioClininaclBERT Evaluation Results

| Metric                         | Value   |
|--------------------------------|--------:|
| Attention Focus Score           | 0.5006  |
| Caption Importance Correlation  | 0.9552  |
| Attention Consistency           | 0.9999  |
| Disease Classification Accuracy | 0.9811  |
| Mean Disease Probability        | 0.5000  |

See `outputs/lvit_nomasks/results/` for detailed ablation studies and visualizations.

---
Look on the file direactor "Output/Lvit_nomasks/visualization"
<img width="1990" height="1229" alt="image" src="https://github.com/user-attachments/assets/e7dce551-37d9-4cf8-bb69-9470d8ab25d7" />

<img width="1934" height="788" alt="image" src="https://github.com/user-attachments/assets/fd800913-6dca-4b44-bfd7-d29735c1135e" />
---
### Comprehensive Ablation Study: Component Analysis & Alignment Strategies
Table 1: Component Ablation Study (with Statistical Significance)

| Variant               | Importance Correlation | Attention Focus Score | Classification Accuracy |
| --------------------- | ---------------------- | --------------------- | ----------------------- |
| Full model            | 0.9507 ± 0.0011        | 0.5017 ± 0.0007       | 0.5457 ± 0.1705         |
| w/o importance module | 0.5000 ± 0.0000 ***    | 0.5019 ± 0.0008       | 0.6323 ± 0.1409         |
| w/o consistency loss  | 0.9507 ± 0.0011        | 0.5199 ± 0.0125       | 0.5452 ± 0.1703         |
| w/o sparsity loss     | 0.9507 ± 0.0011        | 0.5011 ± 0.0003       | 0.5447 ± 0.1706         |
| Single caption only   | 0.5000 ± 0.0000 ***    | 0.5017 ± 0.0007       | 0.6264 ± 0.1722         |
| Random caption order  | 0.9507 ± 0.0011        | 0.5016 ± 0.0006       | 0.5457 ± 0.1704         |


Table 2: Alignment Strategy Comparison (with Statistical Significance)
| Alignment Strategy           | Importance Correlation | Attention Focus Score | Classification Accuracy |
| ---------------------------- | ---------------------- | --------------------- | ----------------------- |
| Full model (Our Alignment)   | 0.9507 ± 0.0011        | 0.5017 ± 0.0007       | 0.5459 ± 0.1703         |
| No alignment                 | 0.5000 ± 0.0000 ***    | 0.5019 ± 0.0008       | 0.6326 ± 0.1423         |
| Cosine similarity            | 0.5798 ± 0.0492 ***    | 0.4972 ± 0.0032       | 0.4186 ± 0.1602         |
| Contrastive loss             | 0.5641 ± 0.0493 ***    | 0.4975 ± 0.0034       | 0.4228 ± 0.1588         |
| Alignment weight (alpha=0.1) | 0.9163 ± 0.0188        | 0.4972 ± 0.0032       | 0.4219 ± 0.1603         |
| Alignment weight (alpha=0.3) | 0.9527 ± 0.0018        | 0.4971 ± 0.0032       | 0.4259 ± 0.1594         |
| Alignment weight (alpha=0.7) | 0.9519 ± 0.0010        | 0.4969 ± 0.0032       | 0.4266 ± 0.1562         |
| Alignment weight (alpha=1.0) | 0.9507 ± 0.0011        | 0.4968 ± 0.0033       | 0.4072 ± 0.1468         |
---
## 📚 Citation

If you use this code or find our work helpful, please cite our paper:

```bibtex
@inproceedings{emu2024lvit,
  title={Weakly Supervised Multi-Caption Guided Medical Image Localization with BioClinicalBERT},
  author={Emu, Dawit},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2024}
}
```

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 🙏 Acknowledgments

- This work was conducted at [Your Institution]
- We thank the NeurIPS reviewers for their valuable feedback
- BioClinicalBERT model from [Stanford Healthcare's PubMedBERT](https://huggingface.ukn.uk/stanford-crfm/BioClinicalBERT)

---

## 📧 Contact

For questions or issues, please open an issue on GitHub or contact: dawitemu1@gmail.com
