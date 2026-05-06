# TitanGPUReproduction

# GPU Lifetime Survival Analysis (Reproduction Study)

This repository contains a reproduction study of a published GPU reliability analysis using survival analysis methods. The original study analyzes GPU reliability using survival analysis techniques, including Kaplan–Meier curves and Cox proportional hazards models. The goal is to replicate the results from the original paper and validate the reported findings using the provided dataset and implementation approach.

## Reference Paper

This work reproduces results from: *[GPU Lifetimes on Titan Supercomputer: Survival Analysis and Reliability*](https://www.researchgate.net/publication/349528960_GPU_Lifetimes_on_Titan_Supercomputer_Survival_Analysis_and_Reliability)

## Dataset

The [dataset](https://doi.ccs.ornl.gov/dataset/4aa54c30-3d51-5443-b839-88a130e4c713) used in this project includes GPU lifecycle logs with the following key variables:

- `SN`: Device identifier  
- `insert`: Installation timestamp  
- `remove`: Removal/failure timestamp  
- `event`: Failure type (DBE / OTB)  
- `location`: Physical GPU location  
- Derived batch label: Old vs New GPUs  

This dataset is a processed version of raw operational logs used in the original study.

## Code Reference 
LINK: [Github link to the code from the paper referenced](https://github.com/olcf/TitanGPULife)
The analysis is implemented in **R**, following the methodology described in the original paper. Key packages used:

- `survival`
- `survminer`
- `ggplot2`
- `dplyr`

The workflow includes:
- Kaplan–Meier survival estimation  
- Cox proportional hazards modeling  
- Device-level MTBF computation  
- Diagnostic checks (Schoenfeld residuals)

## Objective

The objective of this project is to:

- Reproduce the survival analysis results reported in the original paper  
- Validate hazard ratio patterns across GPU batches and locations  
- Compare reliability differences between Old and New GPU batches  
- Assess consistency of MTBF and Cox model outputs with published results  

## Notes

- This is a reproduction study; minor differences may occur due to preprocessing.
- HTML outputs are generated.

## Author

Samyoga Bhattarai
