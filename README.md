# Magnetic Transition Analysis in LaFeO₃ Samples

**A more detailed discussion is found in the "analysis.ipynb" file**

This repository presents the analysis of experimental magnetization data (M vs T) obtained from VSM measurements, with the goal of identifying and characterizing magnetic curves in LaFeO₃-based samples in the context of 
the analysis of these samples for my undergraduate thesis (Green precursor-assisted solid-state synthesis of LaFeO3 perovskite:
role of tannic acid on structural and magnetic properties).

## Overview
Two types of samples were studied:
**SS5**: synthesized via solid-state method  
**ATSS5**: synthesized using a tannic-acid-assisted route  

Magnetic measurements were performed under:
**ZFC (Zero-Field-Cooling)**
**FC (Field-Cooling)**

The analysis focuses on understanding how synthesis conditions and microstructural differences affect the magnetic response.

## Methodology

1. **Data loading and cleaning**
   - Parsing `.DAT` files from VSM measurements
   - Extracting relevant columns (Temperature, Magnetization)

2. **Data processing**
   - Normalization by sample mass and realization of the graph of the curves M vs T.
     
   <img width="708" height="547" alt="image" src="https://github.com/user-attachments/assets/99d11a03-4988-4fa0-b8dd-b1dbd8d7a823" />

3. **Feature extraction and peak fitting**
   - Identification of transition temperatures from peaks in dM/dT
   - Lorentzian model using `lmfit`
   - Extraction of:
     **μ (mu)** → transition temperature  
     **σ (sigma)** → peak width (transition broadening)

4. **Visualization**
   - dM/dT curves for each sample and overlay of experimental data and fitted models.
     
  <img width="689" height="547" alt="image" src="https://github.com/user-attachments/assets/81a73ec0-2d1e-46b3-8b93-13f4f780cd23" />

---

## Results

- A magnetic transition is observed around **260 K (250 K)** in all samples.
- The transition in **SS5** is sharper and better defined.
- **ATSS5** shows a broader and less defined transition.

These results are consistent with:
- Presence of a **hematite (Fe₂O₃)** secondary phase (from XRD)
- Differences in **particle size distribution** (from SEM)

The transition is attributed to the **Morin transition** of hematite, whose temperature depends on particle size and structural heterogeneity.

## Tools & Libraries

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- lmfit  
