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

Sechaud V. et al., [Equivariance-based self-supervised learning for audio signal recovery from clipped measurements](https://arxiv.org/abs/2409.15283), 2024.

- Code tutorial: [Self-supervised learning with Equivariant Imaging for MRI | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_equivariant_imaging.html)
- Code tutorial: [Image transformations for Equivariant Imaging | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_ei_transforms.html)

### Multi-operator algorithms

- Yaman + example
- Millard & Chiew, Noise2Self, Noise2Inverse
- Noise2Inverse, Noise2Void, Noise2Self
- Artifact2Artifact, Phase2Phase + example
- AmbientDiffusion - refer to tutorial
- Tachella J. et al., [Unsupervised Learning From Incomplete Measurements for Inverse Problems](https://arxiv.org/abs/2201.12151)

- Code tutorial: [Self-supervised learning with measurement splitting | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_splitting_loss.html)
- Code tutorial: [Self-supervised MRI reconstruction with Artifact2Artifact | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_artifact2artifact.html)
- Code tutorial: [Self-supervised learning from incomplete measurements of multiple operators | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_multioperator_imaging.html)

#### Denoising algorithms

Le Montagner et al., [An Unbiased Risk Estimator for Image Denoising in the Presence of Mixed Poisson-Gaussian Noise](https://ieeexplore.ieee.org/abstract/document/6714502)

Tachella J. et al., [UNSURE: Unknown Noise level Stein's Unbiased Risk Estimator](https://arxiv.org/abs/2409.01985)

Eldar Y., [Generalized SURE for Exponential Families: Applications to Regularization](https://ieeexplore.ieee.org/document/4663926)

Lehtinen J. et al., [Noise2Noise: Learning Image Restoration without Clean Data](https://arxiv.org/abs/1803.04189)

Huang T. et al., [Neighbor2Neighbor: Self-Supervised Denoising from Single Noisy Images](https://arxiv.org/abs/2101.02824), 2021.

Pang T. et al., [Recorrupted-to-Recorrupted: Unsupervised Deep Learning for Image Denoising](https://openaccess.thecvf.com/content/CVPR2021/papers/Pang_Recorrupted-to-Recorrupted_Unsupervised_Deep_Learning_for_Image_Denoising_CVPR_2021_paper.pdf)

- Code tutorial: [Self-supervised denoising with the SURE loss | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_sure_denoising.html)
- Code tutorial: [Self-supervised denoising with the UNSURE loss | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_unsure.html)
- Code tutorial: [Self-supervised denoising with the Neighbor2Neighbor loss | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/self-supervised-learning/demo_n2n_denoising.html)

### Generative models

- Deep Image Prior
- CoIL, Ultra-NeRF

#### Generative adversarial models

Bora A. et al., [AmbientGAN: Generative models from lossy measurements](https://openreview.net/forum?id=Hy7fDog0b)

Pajot A. et al., [Unsupervised Adversarial Image Reconstruction](https://openreview.net/forum?id=BJg4Z3RqF7)

Li B. et al., [Progressive dual-domain-transfer cycleGAN for unsupervised MRI reconstruction](https://www.sciencedirect.com/science/article/abs/pii/S0925231223010573)

#### Diffusion models

Daras G. et al., [Ambient Diffusion: Learning Clean Distributions from Corrupted Data](https://arxiv.org/abs/2305.19256)

Kawar B. et al., [GSURE-Based Diffusion Model Training with Corrupted Data](https://arxiv.org/abs/2305.13128)

- Code tutorial: [Imaging inverse problems with adversarial networks | DeepInverse](https://deepinv.github.io/deepinv/auto_examples/adversarial-learning/demo_gan_imaging.html)

Aside: Deep model-based approaches (DMBA)

- Concise overview in [CoIL paper](https://arxiv.org/pdf/2102.05181 "https://arxiv.org/pdf/2102.05181") section 2
- [Kamilov 2022 DMBA Overview](https://arxiv.org/abs/2203.17061 "https://arxiv.org/abs/2203.17061")
- Inference-time optimisation procedures: (note these are not directly competitive with above frameworks, as these aren’t used to train the model - they assume a separately trained model, either sup or unsupervised)
    - PnP, RED, RARE
    - DRP
    - SelfDEQ?

- Architectures:
    - Deep unrolling/unfolding
    - Deep cascade

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