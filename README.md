# CMB-Analysis-HEALPix-NaMaster-MpSolve-PolyMV
Analysis of Cosmic Microwave Background Maps Using HEALPix, NaMaster, and Planck Data - EP491 UG Project (IIT BHU)

## Overview

This repository contains the complete computational analysis framework for studying Cosmic Microwave Background (CMB) temperature maps using advanced Python-based tools and methodologies. This work was conducted as part of the EP491 undergraduate research project at the Department of Physics, IIT (BHU) Varanasi.

**Key Focus Areas:**
- Spherical harmonic analysis and power spectrum estimation using HEALPix/Healpy
- Pseudo-Cℓ analysis on masked sky data using NaMaster
- Multipole Vector (MV) and Fréchet Vector (FV) statistical analysis
- CMB isotropy and Gaussianity tests
- Planck PR2/PR3 data analysis and validation

## Project Structure

### Jupyter Notebooks

1. **`healpix_exercises_v1.ipynb`** - Comprehensive HEALPix/Healpy Analysis
   - Generation of 100 CMB map realisations from theoretical Planck power spectra
   - Spherical harmonic transforms and power spectrum recovery
   - Masking operations using WMAP kq85 mask
   - NaMaster pseudo-Cℓ analysis with mode-coupling deconvolution
   - Resolution effects and beam smoothing analysis
   - Map operations: scaling, masking, arithmetic, and safe division

2. **`My_Fv_related_exercises_UG.ipynb`** - Multipole/Fréchet Vector Analysis
   - Extraction and visualization of Multipole Vectors (MVs) for Planck maps
   - Fréchet Vector (FV) computation for geometric analysis
   - Statistical isotropy tests using vector-based methods
   - Analysis for Planck PR2 and PR3 data releases
   - Benchmarking against reference datasets from PolyMV repository

### Documentation

- **Project Report** (`22174007-EP491_-UG-Project-Report-Final.pdf`) - Full technical report with theoretical background, methodology, results, and analysis

## Technical Details

### Data Sources
- **Planck Mission**: PR3 and PR4 temperature maps (Commander, NILC, SEVEM, SMICA)
- **WMAP**: kq85 galactic mask for sky coverage
- **Theoretical Spectra**: Planck 2018 best-fit ΛCDM power spectrum

### Key Methodologies

#### HEALPix Framework
- Hierarchical Equal Area isoLatitude Pixelization for full-sky analysis
- NSIDE parameters: 128, 512, 1024, 2048 for multi-resolution studies
- Spherical harmonic decomposition up to ℓ_max = 3*NSIDE - 1

#### NaMaster Pseudo-Cℓ Pipeline
- Mode-coupling matrix computation and deconvolution
- Bandpower binning for variance reduction
- Mask apodization to suppress spectral leakage
- Validation against published Planck power spectra

#### Multipole Vector Analysis
- Novel representation encoding each multipole as unit direction vectors
- Inter-multipole alignment tests (ℓ = 2-10 range)
- Non-Gaussianity and statistical anisotropy signatures
- Geometric measures complementing traditional harmonic statistics

## Key Results

### Power Spectrum Validation
- Successfully reproduced Planck published power spectrum to within 1σ statistical uncertainties
- Accurate recovery of first three acoustic peaks at ℓ ≈ 220, 540, 850
- Proper handling of mode coupling induced by ~70% sky fraction galactic mask

### Resolution Studies
- Demonstrated information loss with map downgrading (NSIDE 1024 → 16)
- Quantified pixel window function effects at different resolutions
- Analyzed beam function damping on small-scale power

### Statistical Analysis
- Characterized inter-multipole correlations and spatial alignments
- Quantified deviations from statistical isotropy expectations
- Validated Gaussian random field assumptions for large-scale modes

## Software Dependencies

- **Core Libraries**: Python 3.x, NumPy, Matplotlib
- **CMB Tools**: Healpy (HEALPix Python wrapper), NaMaster (pseudo-Cℓ framework)
- **Specialized**: MPSolve (polynomial root-finding), PolyMV (multipole vector computation)
- **Environment**: Google Colab with GPU acceleration

## Installation & Usage

```python
# Install required packages
!pip install healpy
!pip install pymaster  # NaMaster

# Mount Google Drive for data access
from google.colab import drive
drive.mount('/content/drive')
```

## Research Team

**Student Investigator:**  
Eshan Sugeesh E R  
Roll No. 22174007  
Integrated B.Tech-M.Tech, Engineering Physics  
Department of Physics, IIT (BHU) Varanasi

**Supervisor:**  
Dr. Pavan Kumar Aluri  
Assistant Professor  
Department of Physics, IIT (BHU) Varanasi

**Teaching Assistant:**  
Mr. Sanjeev Sanyal  
Research Scholar  
Department of Physics, IIT (BHU) Varanasi

## Acknowledgments

This work utilizes publicly available data from:
- ESA Planck Mission (PR2, PR3, PR4 releases)
- NASA WMAP Mission (kq85 mask)
- Planck Legacy Archive
- LAMBDA CMB Experiments Archive

We acknowledge the use of open-source software:
- HEALPix/Healpy development teams
- NaMaster (LSST DESC collaboration)
- PolyMV package (Oliveira et al. 2020)

## References

1. Planck Collaboration (2020). Planck 2018 results. VI. Cosmological parameters. *A&A*, 641, A6
2. Górski et al. (2005). HEALPix: A Framework for High-Resolution Discretization. *ApJ*, 622, 759
3. Oliveira, R. A., Pereira, T. S., & Quartin, M. (2020). CMB statistical isotropy confirmation at all scales using multipole vectors. *Physics of the Dark Universe*, 30, 100608
4. Sullivan, R. M., Hergt, L. T., & Scott, D. (2024). Methods for CMB map analysis. arXiv:2410.12951

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Project Status

**Completed:** November 2025  
**Course:** EP491 - UG Research Project  
**Institution:** Indian Institute of Technology (BHU) Varanasi  

---

**Topics:** CMB, Cosmology, Astrophysics, HEALPix, Healpy, NaMaster, Python, Planck, Spherical Harmonics, Power Spectrum, Multipole Vectors, Data Analysis, Scientific Computing
