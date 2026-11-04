---
title: "Week 10 — CT Image Formation & Reconstruction"
---

How a CT scanner **acquires** projections and **reconstructs** an image. Notebooks cover scanner generations + the sinogram/back-projection, the **Fourier theory** behind CT, and a head-to-head **comparison** of the three reconstruction families.

[Browse this week on GitHub](https://github.com/menonpg/BIOENG1340-2026/tree/main/Week10)

## Notebooks

### [Week 10 — CT Scanner Generations, the Sinogram & Back-Projection]({{ '/notebooks/week10-ctscanners-sinogram-backprojection/' | relative_url }})

The companion to the **algebraic reconstruction** work: how real scanners *acquire* projections, and the **back-projection** route to an image. Topics:

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week10/CTScanners_Sinogram_BackProjection.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week10/CTScanners_Sinogram_BackProjection.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week10/CTScanners_Sinogram_BackProjection.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week10/CTScanners_Sinogram_BackProjection.ipynb)

### [Week 10 — Fourier Theory & Parseval's Theorem in CT Image Formation]({{ '/notebooks/week10-fouriertheory-parseval-ct/' | relative_url }})

CT reconstruction is, at heart, a **Fourier** problem. This notebook builds the theory that connects X-ray projections to the image:

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week10/FourierTheory_Parseval_CT.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week10/FourierTheory_Parseval_CT.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week10/FourierTheory_Parseval_CT.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week10/FourierTheory_Parseval_CT.ipynb)

### [Week 10 — Comparing CT Reconstruction Methods]({{ '/notebooks/week10-reconstructionmethods-compare/' | relative_url }})

Three ways to turn a **sinogram** (projections at many angles) back into an image, each rooted in the theory from FourierTheory_Parseval_CT.ipynb and ../Week09/AlgebraicReconstruction_4x4.ipynb:

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week10/ReconstructionMethods_Compare.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week10/ReconstructionMethods_Compare.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week10/ReconstructionMethods_Compare.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week10/ReconstructionMethods_Compare.ipynb)

<p class="backlinks"><a href="{{ '/' | relative_url }}">← Home</a> · <a href="{{ '/notebooks/' | relative_url }}">All notebooks</a></p>