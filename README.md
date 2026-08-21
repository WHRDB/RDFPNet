# RDFPNet: A Reliability-Guided Dynamic Frequency Prototype Network for Semi-Supervised Cropland Change Detection

This repository contains the official implementation of the paper: "RDFPNet: A Reliability-Guided Dynamic Frequency Prototype Network for Semi-Supervised Cropland Change Detection", which has been submitted to *IEEE Transactions on Geoscience and Remote Sensing*.

**Authors:** Haoran Wang, Qihao Liu, Peng Wang, Jiaen Chen, Guoshun Zhang, Yuchen Zheng

## 📢 News

- **[2026-08-21]** The repository is created.
- **[Coming Soon]** Code and pretrained weights will be released upon acceptance.

## 📝 Abstract

Semi-supervised change detection reduces annotation costs by exploiting limited labeled data and abundant unlabeled data. However, it remains challenging in cropland environments, where changed regions are often sparse and seasonal transitions and crop growth stages may cause substantial spectral variations between bi-temporal images. These domain shifts can bias predictions toward the unchanged class, introduce noisy pseudo-labels, and weaken consistency learning.

To address these issues, we propose the **Reliability-Guided Dynamic Frequency Prototype Network (RDFPNet)**, a teacher-student framework for semi-supervised cropland change detection. First, the **Reliable Pseudo-Label Calibration (RPC)** module corrects class bias using labeled-data priors and teacher predictions. Class-adaptive thresholds and reliability weighting are then employed to generate calibrated pseudo-labels and soft reliability weights. Second, **Dynamic Fourier Consistency Learning (DFCL)** adaptively controls the exchange of low-frequency amplitude components according to bi-temporal spectral differences and the reliable background ratio. The resulting Fourier views are used for consistency learning to reduce sensitivity to seasonal and crop-growth-related variations. Finally, **Spatial Reliability Regularization (SRR)** enforces consistency under strong augmentation, applies reliability-guided ClassMix to strengthen supervision in changed regions, and aligns reliable background features with an exponential moving average prototype.

Extensive experiments on four benchmark datasets demonstrate that RDFPNet achieves competitive performance under different labeled-data ratios and maintains stable cross-domain generalization.

## ✨ Contributions

1. We propose RDFPNet to address unreliable pseudo-labels and bi-temporal domain shifts in semi-supervised cropland change detection. The RPC module corrects class bias and filters uncertain predictions.

2. We introduce DFCL to dynamically exchange low-frequency amplitude components between bi-temporal images and enforce prediction consistency. Meanwhile, SRR improves spatial consistency and reduces background feature variation.

3. Extensive experiments on four benchmark datasets show that RDFPNet achieves competitive performance compared with state-of-the-art semi-supervised methods and maintains stable performance in cross-domain tests.

## 🚀 Framework

## Overall Framework

<p align="center">
  <img src="Over_farmwork/overall_framework.jpg"
       alt="Overall framework of the proposed RDFPNet"
       width="900">
</p>

<p align="center">
  <em>Overall framework of the proposed RDFPNet.</em>
</p>

*The framework figure will be added soon.*

## 📂 Datasets

We evaluate RDFPNet on four representative cropland change detection datasets:

- **JLYHCD** — A high-resolution cropland change detection dataset based on Jilin-1 satellite imagery.
- **CLCD** — A fine-grained cropland change detection dataset with multiscale spatial and temporal variations.
- **PX-CLCD** — A high-resolution cultivated land change detection dataset.
- **Hi-CNA** — A benchmark dataset for high-resolution cropland change detection.

*Dataset download links and preparation instructions will be added soon.*

## ✒️ Citation

If you find this work useful, please consider citing:

```bibtex
@article{wang2026rdfpnet,
  title     = {RDFPNet: A Reliability-Guided Dynamic Frequency Prototype Network for Semi-Supervised Cropland Change Detection},
  author    = {[Authors]},
  journal   = {IEEE Transactions on Geoscience and Remote Sensing},
  year      = {2026}
}
