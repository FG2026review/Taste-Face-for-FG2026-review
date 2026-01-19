# TasteFace Dataset (Preview for FG 2026 Review)

This repository provides a **preview release** of the *TasteFace* dataset, accompanying the paper:

> *A Dynamic–Static Dataset of Facial Feature Variations Induced by Six Basic Tastes*  
> Submission to the **20th IEEE International Conference on Automatic Face and Gesture Recognition (FG 2026)**  
> *(under double-blind review)*

TasteFace is a task-oriented facial behavior dataset specifically designed for **objective gustatory analysis**.  
Unlike generic affective datasets, TasteFace captures *spontaneous physiological facial responses* induced by six standardized taste modalities using liquid stimuli, following a causal **Label-to-Data** paradigm:  
the stimulus (taste) is precisely controlled and serves as the ground-truth condition from which facial behavior emerges.

**Important Notice (Review Version)**  
This repository is an **anonymous preview** created solely for the FG 2026 double-blind review process.

- It contains **example data and structural previews only**.  
- The purpose is to demonstrate the **data organization, modality design, and authenticity** of the dataset.  
- The **full dataset**, together with complete documentation and auxiliary utilities, will be released **after formal acceptance**.

No identifying information about the authors or institutions is included in this repository.

---

## Overview

TasteFace is constructed to bridge the semantic gap between:

- Social-emotion-oriented facial datasets (e.g., AffectNet, FER2013), and  
- Task-specific chemosensory facial dynamics.

Key characteristics:

- **Six taste modalities**:  
  *Astringency, Bitterness, Saltiness, Sourness, Sweetness, Umami*
- **48 participants**, demographically diverse  
- **Liquid stimuli** to eliminate mastication artifacts  
- **Dynamic sequences** preserving micro-expressions and temporal evolution  
- A design centered on **causal controllability** rather than post-hoc affect labeling  

The dataset is designed for:

- Facial representation learning under controlled physiological stimuli  
- Gustatory response modeling  
- Cross-domain and cross-task generalization analysis  
- Sensory computing and affective neuroscience  

As shown in the accompanying paper, models trained directly on TasteFace achieve an **order-of-magnitude performance gain** over representations learned from generic facial datasets on taste-related tasks.  
This empirically demonstrates that taste-induced facial behavior constitutes a **distinct biological signal space**, which is not adequately covered by existing affective datasets.

---

## Repository Structure (Preview)

This preview repository reflects the *final dataset organization* while exposing only a small, non-identifying subset of the data:

Taste-Face/
├── data/
│ ├── ratings/ # Anonymized subjective rating tables (preview)
│ ├── videos/ # Example taste-induced facial videos (preview only)
│ └── frames/ # Example extracted frame sequences
│
├── docs/ # Dataset documentation (structure, protocol, schema)
├── README.md
└── DATA_USAGE_POLICY.md


- `data/videos/` and `data/frames/` contain **example samples only**, selected to illustrate:
  - The authenticity of the recordings  
  - The temporal structure of the sequences  
  - The correspondence between modalities  

- `data/ratings/` provides a preview of the **anonymized subjective annotation format**.

The **complete dataset** follows the same structure and will be released upon acceptance.

---

## Usage Terms (Review Version)

This dataset contains real facial data collected under informed consent.

All materials in this repository are provided **strictly for academic review purposes** in the context of FG 2026.  
They must not be redistributed, reused, or repurposed outside the review process.

The final public release will be governed by a non-commercial academic license
and accompanied by full documentation and access instructions.