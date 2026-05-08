# Module 02 — Linear Systems

> **Numerical Methods for Engineering** · Universidad Nacional de Colombia  
> Repository: [`bpatinoa/numerical-methods-for-engineering`](https://github.com/bpatinoa/numerical-methods-for-engineering)

---

## Overview

This module covers numerical methods for solving **systems of linear equations** $A\mathbf{x} = \mathbf{b}$, one of the most fundamental problems in engineering computation. Methods are divided into two families:

- **Direct methods** — transform the system into an equivalent one that is solved exactly in a finite number of steps (up to floating-point rounding).
- **Iterative methods** — start from an initial guess and refine it until convergence; preferred for large sparse systems.

All notebooks follow the same structure: rigorous theoretical background, a clean Python implementation, and three application examples drawn from general mathematics, chemistry, and telecommunications.

---

## Methods

| # | Method | Notebook | Family | Convergence |
|---|--------|----------|--------|-------------|
| 01 | Gaussian Elimination with Partial Pivoting | [`01_Gaussian_Elimination.ipynb`](01_Gaussian_Elimination.ipynb) | Direct | Exact (O(n³) ops) |
| 02 | LU Decomposition (Doolittle) | [`02_LU_Decomposition.ipynb`](02_LU_Decomposition.ipynb) | Direct | Exact (O(n³) ops) |
| 03 | Cholesky Decomposition | [`03_Cholesky.ipynb`](03_Cholesky.ipynb) | Direct | Exact, SPD matrices only |
| 04 | Jacobi Iterative Method | [`04_Jacobi.ipynb`](04_Jacobi.ipynb) | Iterative | Linear (diagonal dominance) |
| 05 | Gauss-Seidel Iterative Method | [`05_Gauss_Seidel.ipynb`](05_Gauss_Seidel.ipynb) | Iterative | Linear (~2× faster than Jacobi) |
| 06 | Successive Over-Relaxation (SOR) | [`06_SOR.ipynb`](06_SOR.ipynb) | Iterative | Linear (tuned by ω parameter) |

---

## Applications by Domain

| Domain | Problem | Methods Applied |
|--------|---------|-----------------|
| **General Mathematics** | Solving dense and sparse coefficient systems, least-squares normal equations | All |
| **General Mathematics** | Matrix inversion via multiple right-hand sides | LU, Gaussian |
| **Chemistry** | Stoichiometric balancing of chemical reactions (conservation equations) | Gaussian, LU |
| **Chemistry** | Multi-component chemical equilibrium — simultaneous mass/charge balances | Gauss-Seidel, SOR |
| **Telecommunications** | Nodal analysis of RF circuits (admittance matrix $Y\mathbf{V} = \mathbf{I}$) | LU, Cholesky |
| **Telecommunications** | Antenna array synthesis — solving the coupling impedance system $Z\mathbf{I} = \mathbf{V}$ | Jacobi, Gauss-Seidel |
| **Telecommunications** | Channel estimation in MIMO systems (least-squares $A^T A \mathbf{x} = A^T \mathbf{b}$) | Cholesky, LU |

---

## Key Concepts

| Concept | Relevant Notebooks |
|---------|-------------------|
| Partial pivoting & numerical stability | 01, 02 |
| LU factorisation and reuse for multiple RHS | 02 |
| Symmetric positive definite (SPD) matrices | 03 |
| Diagonal dominance as convergence condition | 04, 05, 06 |
| Spectral radius and convergence rate | 04, 05, 06 |
| Optimal relaxation parameter $\omega^*$ | 06 |
| Condition number and ill-conditioning | 01, 02, 03 |

---

## Prerequisites

- Linear algebra: matrix operations, determinants, eigenvalues
- Module 01 (Root Finding) — not strictly required, but recommended for context
- Python: `numpy`, `matplotlib`, `scipy.linalg` (for verification only)

---

## How to Run

Each notebook is self-contained and can be executed in Google Colab with no local installation:

```
https://colab.research.google.com/github/bpatinoa/numerical-methods-for-engineering/blob/main/02-Linear-Systems/<notebook_name>.ipynb
```

Or clone the repository and run locally:

```bash
git clone https://github.com/bpatinoa/numerical-methods-for-engineering.git
cd numerical-methods-for-engineering/02-Linear-Systems
jupyter notebook
```

---

## References

- Chapra, S. C., & Canale, R. P. (2015). *Numerical Methods for Engineers* (7th ed.). McGraw-Hill.
- Burden, R. L., Faires, J. D., & Burden, A. M. (2016). *Numerical Analysis* (10th ed.). Cengage.
- Golub, G. H., & Van Loan, C. F. (2013). *Matrix Computations* (4th ed.). Johns Hopkins University Press.
- Saad, Y. (2003). *Iterative Methods for Sparse Linear Systems* (2nd ed.). SIAM.

---

*Module maintained by [@bpatinoa](https://github.com/bpatinoa) · Numerical Methods for Engineering · UNAL*
