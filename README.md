# TasteFace Dataset (Preview)

This repository provides a **preview release** of the *TasteFace* dataset, accompanying the paper:

> *A Dynamic-Static Dataset of Facial Feature Variations Induced by Six Basic Taste*  
> FG 2026 Submission (under review)

TasteFace is a task-oriented facial expression dataset specifically designed for **objective gustatory analysis**.  
Unlike generic affective datasets, TasteFace captures *spontaneous physiological facial responses* induced by six standardized taste modalities using liquid stimuli, following a causal **Label-to-Data** paradigm.

⚠️ **Important Notice**  
This repository currently contains **example data and structural previews only**.  
The *full dataset*, together with complete documentation and preprocessing scripts, will be released **after the paper is formally accepted**.

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
- Designed for:
  - Facial representation learning
  - Gustatory response modeling
  - Cross-domain generalization analysis
  - Sensory computing and affective neuroscience

As demonstrated in the paper, models trained directly on TasteFace achieve an **order-of-magnitude performance gain** over representations learned from generic facial datasets, confirming that taste-induced expressions constitute a **distinct biological signal space**.

---

## Repository Structure (Preview)

```text
Taste-Face/
├─ videos/        # Example taste-induced facial videos (preview only)
├─ images/        # Example extracted frames
├─ README.md
└─ LICENSE
