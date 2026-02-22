# Active Learning for Planet Habitability Classification

This repository accompanies the manuscript:

**El-Kholy & Hayman (2026)**
*Active Learning for Planet Habitability Classification under Extreme Class Imbalance*

---

## Overview

Exoplanet catalogs now contain thousands of confirmed planets, but only a small fraction are labeled as potentially habitable. This creates an **extreme class imbalance** problem that challenges traditional supervised learning.

This project investigates whether **pool-based Active Learning (AL)** can:

* Improve recall of rare potentially habitable planets
* Reduce the number of labeled instances required
* Provide uncertainty-aware prioritization of follow-up targets

Habitability is treated as a **binary classification problem**:

$$
f_\theta : \mathbb{R}^d \rightarrow [0,1]
$$

where feature vectors include planetary, stellar, and system-level parameters.

---

## Dataset

We merge:

* **Habitable Worlds Catalog (HWC)**
* **NASA Exoplanet Archive (PSCompPars table)**

Final dataset:

* 5,821 confirmed exoplanets
* 70 labeled as potentially habitable
* ~1% positive class fraction

---

## Repository Structure

```
.
├── data/
├── notebooks/
├── results/
├── requirements.txt
└── README.md
```

---

## Installation

```bash
git clone https://github.com/rehamelkholy/ExoplanetAL
cd ExoplanetAL

python -m venv venv
source venv/bin/activate

pip install -r requirements.txt
```

---

## Citation

If you use this repository, please cite:

```bibtex
@article{ElKholy2026,
  author  = {El-Kholy, R. I. and Hayman, Z. M.},
  title   = {Active Learning for Planet Habitability Classification under Extreme Class Imbalance},
  year    = {2026}
}
```