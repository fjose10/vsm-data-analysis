# Magnetic Transition Analysis in LaFeO₃ Samples

This project presents the analysis of experimental magnetization data (M vs T) obtained from VSM measurements, with the goal of identifying and characterizing magnetic transitions in LaFeO₃-based samples.

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
   - Normalization by sample mass
   - Computation of the numerical derivative **dM/dT**

3. **Feature extraction**
   - Identification of transition temperatures from peaks in dM/dT
   - Selection of fitting models around the transition

4. **Peak fitting**
   - Lorentzian model using `lmfit`
   - Extraction of:
     **μ (mu)** → transition temperature  
     **σ (sigma)** → peak width (transition broadening)

5. **Visualization**
   - dM/dT curves for each sample
   - Overlay of experimental data and fitted models

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
