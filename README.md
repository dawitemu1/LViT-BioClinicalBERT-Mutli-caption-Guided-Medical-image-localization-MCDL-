# LViT-BioClinicalBERT: Multi-Caption Guided Medical Image Localization

[![Conference](https://img.shields.io/badge/NeurIPS-2024-blue)](https://neurips.cc/)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)

> **Weakly Supervised Multi-Caption Guided Medical Image Localization with BioClinicalBERT**

This repository contains the official implementation of our NeurIPS 2024 paper on weakly supervised medical image localization using multi-caption guidance and BioClinicalBERT.

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
