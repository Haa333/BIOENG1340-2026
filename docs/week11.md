---
title: "Week 11 — CT Artifacts, Contrast Agents, Nuclear Imaging, Dosimetry & Project Methods"
---

Finishing CT (artifacts and contrast agents), **nuclear imaging** (scintigraphy, SPECT, PET) and **radiation dosimetry**, plus hands-on **project-analysis methods** discussed in the project reviews (segmentation quantification, group statistics, and an ultrasound M-mode preview).

[Browse this week on GitHub](https://github.com/menonpg/BIOENG1340-2026/tree/main/Week11)

## Notebooks

### [Week 11 — CT Artifacts]({{ '/notebooks/week11-ctartifacts/' | relative_url }})

Real CT images are rarely perfect. This notebook simulates the artifacts discussed in class and shows **why** they arise and **which go away with more projections** and which do not.

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/CTArtifacts.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/CTArtifacts.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/CTArtifacts.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/CTArtifacts.ipynb)

### [Week 11 — Comparing Two Groups (Patients vs Controls)]({{ '/notebooks/week11-comparingtwogroups/' | relative_url }})

Most imaging projects end with the same question: **is a measured metric different between two groups?** (e.g. hippocampal volume in Alzheimer's vs controls). Choosing the **right statistical test** depends on whether the data are **normally distributed**. This notebook walks the full decision:

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/ComparingTwoGroups.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/ComparingTwoGroups.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/ComparingTwoGroups.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/ComparingTwoGroups.ipynb)

### [Week 11 — Contrast Agents (CT & MRI)]({{ '/notebooks/week11-contrastagents/' | relative_url }})

Many structures (blood vessels, tumors, inflamed tissue) have almost the **same** native attenuation or relaxation as their surroundings, so they are invisible. **Contrast agents** are injected to *temporarily* change a tissue property and make those structures stand out.

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/ContrastAgents.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/ContrastAgents.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/ContrastAgents.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/ContrastAgents.ipynb)

### [Week 11 — Nuclear Imaging: Scintigraphy, SPECT & PET]({{ '/notebooks/week11-nuclearimaging-pet-spect/' | relative_url }})

After MRI, CT, and ultrasound we turn to **nuclear imaging** (scintigraphy). A **radiotracer** is injected; it collects where metabolism is high (tumors, perfused myocardium) and **emits** radiation that we detect from outside. This notebook builds the key ideas and simulates them.

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/NuclearImaging_PET_SPECT.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/NuclearImaging_PET_SPECT.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/NuclearImaging_PET_SPECT.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/NuclearImaging_PET_SPECT.ipynb)

### [Week 11 — Radiation Dosimetry]({{ '/notebooks/week11-radiationdosimetry/' | relative_url }})

Ionizing-radiation imaging (X-ray, CT, fluoroscopy, nuclear) carries a **dose** cost. Dosimetry is the science of **measuring** it. This notebook defines the units and simulates the key quantities.

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/RadiationDosimetry.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/RadiationDosimetry.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/RadiationDosimetry.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/RadiationDosimetry.ipynb)

### [Week 11 — Quantifying a Segmentation: Volume & Shape]({{ '/notebooks/week11-segmentationquantification/' | relative_url }})

Once you have a **3-D segmentation mask** (from ITK-SNAP, ParaView, or an AI model), the next step is to turn it into **numbers**: a physical **volume** and **shape descriptors**. This is the core measurement step for several class projects (hippocampus volume, left-ventricle volume over time, optic-nerve-head vessel morphology).

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/SegmentationQuantification.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/SegmentationQuantification.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/SegmentationQuantification.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/SegmentationQuantification.ipynb)

### [Week 11 — Ultrasound M-mode (a scan line over time)]({{ '/notebooks/week11-ultrasound-mmode/' | relative_url }})

A preview of ultrasound imaging, motivated by the echocardiography project (stacking video frames into a 3-D volume). Standard **B-mode** ultrasound is a 2-D image that updates in time (a video). **M-mode** (“motion mode”) instead takes a **single scan line** and plots it **over time** — depth on one axis, time on the other — giving very high temporal resolution for moving structures (heart valves, vessel walls, chamber walls).

[View on GitHub](https://github.com/menonpg/BIOENG1340-2026/blob/main/Week11/Ultrasound_MMode.ipynb) · [nbviewer](https://nbviewer.org/github/menonpg/BIOENG1340-2026/blob/main/Week11/Ultrasound_MMode.ipynb) · [Open in Colab](https://colab.research.google.com/github/menonpg/BIOENG1340-2026/blob/main/Week11/Ultrasound_MMode.ipynb) · [Download](https://raw.githubusercontent.com/menonpg/BIOENG1340-2026/main/Week11/Ultrasound_MMode.ipynb)

<p class="backlinks"><a href="{{ '/' | relative_url }}">← Home</a> · <a href="{{ '/notebooks/' | relative_url }}">All notebooks</a></p>