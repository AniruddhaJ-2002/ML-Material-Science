# ML-Material-Science
ML for Material Science- surrogate modelling, FEA integrations, and computational materials applications
# ML for Materials Science — FEA Surrogate Modeling

Machine Learning applied to Computational Materials Science and 
Structural Engineering. Built alongside M.Sc. Computational 
Materials Science studies at TU Bergakademie Freiberg.

## Project 1: FEA Surrogate Model for Automotive Engine Mount Bracket

### Overview
A data-driven surrogate model that predicts structural response 
(Von Mises stress and displacement) of an automotive engine mount 
bracket from simulation parameters — replacing expensive FEM 
simulations with instant ML predictions.

### Dataset
- 32 Abaqus FEM simulations
- 2 bracket geometries (V1: baseline, V2: optimized with gussets)
- 4 load cases: vertical, lateral, longitudinal, combined
- 4 force levels: 50%, 75%, 100%, 150% of design loads

### Results — Phase 1 (Linear Surrogate)
| Output | Model | R² | RMSE |
|--------|-------|----|------|
| Von Mises Stress | Linear Regression | 0.92 | 8.32 MPa |
| Displacement (vertical) | Linear Regression | 0.85 | 0.0075 mm |
| Displacement (lateral) | Linear Regression | 0.95 | 0.0018 mm |
| Displacement (longitudinal) | Linear Regression | 0.71 | 0.053 mm |
| Displacement (combined) | Linear Regression | 0.66 | 0.071 mm |

### Key Finding
A single global displacement model failed (R²=-0.43) because 
load direction fundamentally changes structural response. 
Physically-motivated stratification by load type improved 
performance to R²=0.66-0.95 — demonstrating the importance 
of domain knowledge in engineering ML.

### Phase 2 (Planned)
- Neural network surrogate replacing linear models
- Dynamic impact surrogate from explicit Abaqus results
- Extended dataset from thin-walled tube crushing project

## Curriculum Notebooks
Parallel ML learning notebooks covering:
- Linear & Logistic Regression from scratch
- PCA Mathematics and Implementation  
- Model Evaluation & Cross Validation
- K-Means Clustering
- Neural Networks (NumPy + PyTorch)

## Tools & Libraries
Python, NumPy, Pandas, Scikit-learn, PyTorch, Matplotlib, 
Seaborn, Abaqus CAE

## Background
B.Tech Mechanical Engineering → M.Sc. Computational Materials 
Science (TUBAF).Target: CAE/Simulation Engineering roles in 
German automotive industry.
