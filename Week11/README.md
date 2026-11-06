# Week 11 — CT Artifacts, Contrast Agents, Nuclear Imaging, Dosimetry & Project Methods

Finishing CT (artifacts and contrast agents), **nuclear imaging** (scintigraphy, SPECT, PET) and
**radiation dosimetry**, plus hands-on **project-analysis methods** discussed in the project reviews
(segmentation quantification, group statistics, and an ultrasound M-mode preview).

## Contents

| File | Description |
|------|-------------|
| [CTArtifacts.ipynb](CTArtifacts.ipynb) | Simulated CT artifacts: **metal / high-density** streak & **star** artifacts (persist with any number of views), **beam-hardening cupping**, **motion** blur/ghosting, **ring** artifacts (detector miscalibration), and **photon-counting / thermal noise** — plus the rule that *missing-data* streaks fade with more views while *corrupted-data* artifacts do not. |
| [ContrastAgents.ipynb](ContrastAgents.ipynb) | How contrast agents work: **iodine** raising Hounsfield units (CT), the iodine **K-edge** (33.2 keV) and why low kVp boosts contrast, the **time–attenuation (bolus)** curve and scan timing, and **gadolinium** shortening $T_1$ to brighten $T_1$-weighted MRI. |
| [NuclearImaging_PET_SPECT.ipynb](NuclearImaging_PET_SPECT.ipynb) | **Scintigraphy / SPECT / PET**: active-vs-passive imaging framing, radiotracer **decay**, emission tomography as **photon-starved CT** (Poisson counts → SNR ∝ √counts), **SPECT** (Anger gamma camera) vs **PET** (coincidence lines-of-response), and **fusion** of functional activity onto structural anatomy. |
| [RadiationDosimetry.ipynb](RadiationDosimetry.ipynb) | Units of radiation: **becquerel** (activity $A=\lambda N$), **gray** (absorbed dose), **sievert** (equivalent $H=w_R D$ and effective $E=\sum w_T H_T$), the **entrance skin dose** (inverse-square + backscatter), **cumulative fluoroscopy** dose vs skin-injury thresholds, and typical **effective doses** vs background. |
| [SegmentationQuantification.ipynb](SegmentationQuantification.ipynb) | Turning a 3-D **segmentation mask** into numbers: **volume by voxel counting** ($N_\text{vox}\times$ voxel volume), and **shape metrics** (elongation, roundness, flatness, **sphericity**) via **SimpleITK** and **scikit-image** — blob vs tubular. For the hippocampus, LV-volume, and vessel projects. |
| [ComparingTwoGroups.ipynb](ComparingTwoGroups.ipynb) | Comparing a continuous metric between patients and controls: **Shapiro–Wilk** normality → **t-test** (parametric) vs **Mann–Whitney / Wilcoxon** (non-parametric), **Cohen's $d$** effect size, and the tie back to **power / cohort size**. |
| [Ultrasound_MMode.ipynb](Ultrasound_MMode.ipynb) | Ultrasound preview: **B-mode vs M-mode** — a single scan line over time; building an M-mode from a stacked video volume (a **time-axis slice**) and recovering **heart rate** by FFT. |

## Key concepts

### CT artifacts & contrast agents
- **Artifacts**: **metal/high-density** → streak/**star** (persist regardless of views) + shadowing;
  **beam hardening** → **cupping**; **motion** → blur/ghosting; detector miscalibration → **rings**;
  low dose → **photon-counting/thermal noise**. *Missing-data* artifacts improve with more views;
  *corrupted-data* artifacts do not.
- **Contrast agents**: **iodine** raises $\mu$/HU (CT; K-edge at 33.2 keV favors low kVp); **bolus
  timing** separates arterial/venous phases; **gadolinium** shortens $T_1$ → bright on $T_1$-weighted MRI.

### Nuclear imaging
- **Active vs passive**: MRI and nuclear imaging measure an **active** signal the sample emits; CT and
  ultrasound are **passive** (external source, sample attenuates/reflects).
- **Reconstruction is CT-like** (projections → Radon → FBP / algebraic / direct-Fourier), but emission
  events are **rare** → **Poisson** counts, so images are **low-resolution and noisy**; **SNR ∝ √counts**.
- **SPECT** = single gamma + **Anger** camera + collimator (Tc-99m); **PET** = positron → two 511 keV
  photons 180° apart, detected as **coincidence LORs** in a ring (F-18 FDG). Fused with CT/MRI for anatomy.

### Dosimetry
- **Becquerel** (decays/s), **gray** (J/kg absorbed), **sievert** (harm-weighted: $w_R$ radiation type,
  $w_T$ tissue sensitivity).
- **Entrance skin dose** follows the **inverse-square law** + **backscatter**; long **fluoroscopy** can
  cross deterministic skin-injury thresholds (erythema ~2 Gy → burn >15 Gy). **Effective dose** compares
  exams against ~3 mSv/yr background (**ALARA**).

### Project-analysis methods
- **Volume from a mask**: $V = N_\text{voxels}\times \Delta x\Delta y\Delta z$ (spacing from the header);
  **shape** via SimpleITK (`LabelShapeStatisticsImageFilter`: elongation, roundness, flatness) and
  scikit-image (`regionprops`, **sphericity** from a marching-cubes surface) — blob vs tube.
- **Two-group comparison**: **Shapiro–Wilk** → normal ? **t-test** : **Mann–Whitney**; pair the
  $p$-value with **Cohen's $d$**, and size the cohort with the Week 09 power analysis.
- **Ultrasound M-mode**: one scan line over time (depth × time) = a **time-axis slice** of a stacked
  video volume; high temporal resolution for motion timing (e.g. heart rate by FFT).

## Environment

Uses Python with **NumPy**, **SciPy**, **scikit-image**, **SimpleITK**, and **matplotlib**.
