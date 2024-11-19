# Awesome Unsupervised Imaging
A collection of papers, tutorials and software for solving imaging inverse problems using deep learning **without ground truth**.

The focus is learning frameworks (e.g. losses, training methods) and applications, but not specific architectures.

Contents
1. [Overviews](#overviews)
2. [Frameworks](#frameworks)
3. [Metrics](#metrics)
4. [Applications](#applications)
5. [Foundations](#foundations)

## Overviews

Tachella J., Davies M., [Tutorial: self-supervised learning for imaging](https://tachella.github.io/blog/selfsuptutorial/), 2024.
- A good overview of current methods and theory of self-supervised learning from incomplete data.

Ongie G. et al., [Deep learning techniques for inverse problems in imaging](https://arxiv.org/abs/2005.06001), 2020.
- A 2020 taxonomy of supervised and unsupervised methods.

Chen D., [Imaging with equivariant deep learning: from unrolled network design to fully unsupervised learning](https://ieeexplore.ieee.org/document/10004796), 2023, section _Computational imaging, equivariance, and deep learning_
- A brief timeline of classical methods to deep learning.

## Frameworks

### Equivariant imaging

Chen D. et al., [Equivariant Imaging: Learning Beyond the Range Space](https://arxiv.org/abs/2103.14756), 2021.

Chen D. et al., [Robust Equivariant Imaging: a fully unsupervised framework for learning to image from noisy and partial measurements](http://arxiv.org/abs/2111.12855), 2022.

Tachella J., [Sensing Theorems for Unsupervised Learning in Linear Inverse Problems](http://arxiv.org/abs/2203.12513), 2023.

Wang A. et al., [Perspective-Equivariance for Unsupervised Imaging with Camera Geometry](https://arxiv.org/abs/2403.09327), 2024.

Wang A. et al., [Fully Unsupervised Dynamic MRI Reconstruction via Diffeo-Temporal Equivariance](https://arxiv.org/abs/2410.08646), 2024.

Scanvic J. et al., [Self-Supervised Learning for Image Super-Resolution and Deblurring](https://arxiv.org/abs/2312.11232), 2024.

+ DeepInverse examples

### Measurement subsampling

- Yaman + example
- Millard & Chiew, Noise2Self, Noise2Inverse
- Noise2Noise
- Artifact2Artifact, Phase2Phase + example
- AmbientDiffusion - refer to tutorial

### Generative models

- AmbientGAN, UAIR, CycleGAN + GAN example
- Deep Image Prior
- CoIL, Ultra-NeRF
- Ground-truth-free diffusion: AmbientDiffusion, GSURE-Diffusion etc.

## Metrics

- [Perceptual-distortion trade-off](https://openaccess.thecvf.com/content_cvpr_2018/papers/Blau_The_Perception-Distortion_Tradeoff_CVPR_2018_paper.pdf "https://openaccess.thecvf.com/content_cvpr_2018/papers/Blau_The_Perception-Distortion_Tradeoff_CVPR_2018_paper.pdf") [video](https://www.youtube.com/watch?v=3Oetx8DCUCA "https://www.youtube.com/watch?v=3Oetx8DCUCA")

## Applications

### Magnetic Resonance Imaging

- Find a good paper introducing the physics etc.
- Good supervised/unsupervised/classical overview tutorial

### Computed Tomography

### Remote sensingg

- Pan sharpening: structural measurement consistency, PanGan, QNR


## Foundations

### Linear algebra

### Group theory

- [Introduction to Groups, Representations, Equivariance and Geometric Deep Learning](https://geometricdeeplearning.com/slides/Cambridge_1_Introduction_to_Groups_and_Representations.pdf "https://geometricdeeplearning.com/slides/Cambridge_1_Introduction_to_Groups_and_Representations.pdf")
- Chua lecture notes: [Group Theory](https://dec41.user.srcf.net/notes/IA_M/groups.pdf "https://dec41.user.srcf.net/notes/IA_M/groups.pdf"), [Group representation theory](https://dec41.user.srcf.net/notes/II_L/representation_theory.pdf "https://dec41.user.srcf.net/notes/II_L/representation_theory.pdf")