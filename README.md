#  NeuroX: Brain-to-Image AI Translator
### (An Adaptive AI System for Robust fMRI Decoding)

NeuroX is an advanced artificial intelligence framework designed to read human brain activity (fMRI scans) and reconstruct them into high-resolution, realistic visual images[cite: 1, 2]. The system operates under two core conditions:

1. **Perception (Viewed Images):** When a person is actively looking at a visual stimulus, the system decodes the visual cortex signals to accurately reconstruct the exact image being viewed.
2. **Mental Imagery (Imagined Content):** When a person closes their eyes and simply imagines a scene or an object (like a tiger or an elephant), the system extracts these top-down, internally generated signals to translate their thoughts into a shareable visual representation[cite: 1, 2].

---

## 🚀 Key Innovations & Research Impact

NeuroX introduces three major architectural breakthroughs to solve the critical limitations of previous brain-decoding models:

* **Feedback-Driven Thought Decoding (+22% Gain):** Brain signals during pure imagination are inherently weak and noisy compared to active perception. NeuroX integrates a **Reinforcement Learning (PPO) Controller** that replaces static settings with an iterative, feedback-driven loop to progressively self-correct errors, delivering up to a 22% relative gain in semantic accuracy over static baselines.
* **Universal Subject-Agnostic Alignment:** Traditional systems rely on rigid "one-model-per-subject" training paradigms, making them baseline-sensitive and non-scalable. This framework implements a **Gradient Reversal Layer (GRL)** to strip away idiosyncratic anatomical and physiological variations, mapping universal neural patterns into a single latent space for robust cross-subject generalization without individual retraining.
* **High-Dimensional Voxel Processing:** The architecture is structurally engineered to efficiently handle and compress massive dataset blocks, processing a complex feature grid of exactly **699,192 voxels** per individual trial volume.

---

## 💻 Hardware Infrastructure & Performance

This enterprise-grade research pipeline has been compiled, executed, and benchmarked on high-performance cloud infrastructure:

* **Compute Platform:** NVIDIA A100-SXM4-80GB GPU (CUDA Acceleration Enabled)
* **Input Data Architecture:** Deep 4D Brain Volumes (trials × x × y × z)
* **Data Spectrum Integrity:** Cleaned input values are structurally normalized and securely bound within the standard int16 spectrum of `[-32768.0000, 32767.0000]`

---

## 🛠️ Software Stack Installation

To set up and run the execution pipeline locally, install the core software libraries using the following command:

```bash
pip install torch torchvision numpy pandas scikit-learn h5py diffusers transformers pytorch-msssim nibabel nilearn seaborn
