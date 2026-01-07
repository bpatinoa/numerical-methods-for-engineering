# Numerical Methods for Chemistry & Telecommunications (Colab)

This repository contains **run-ready Google Colab notebooks** for an undergraduate-level course on **Numerical Methods**, with applications in **Chemistry** and **Telecommunications**.

## Goals
- Provide clear theoretical explanations (Markdown/LaTeX) and practical Python implementations.
- Focus on applied, engineering-oriented problems.
- Ensure notebooks are **"Run-only"**: students should only need to open in Colab and click **Run**.

## How to use (Open in Colab)
Open any notebook directly in Colab using this URL format:

`https://colab.research.google.com/github/bpatinoa/numerical-methods-for-engineering/blob/main/<PATH_TO_NOTEBOOK>.ipynb`

Example:
`https://colab.research.google.com/github/bpatinoa/numerical-methods-for-engineering/blob/main/00-Getting-Started/00_Colab_Setup.ipynb`

## Repository structure (high level)
- `00-Getting-Started/` : Colab setup and conventions
- `01-Root-Finding/` : Bisection, Newton-Raphson, Secant, etc.
- `02-Linear-Systems/` : Gaussian elimination, LU, iterative methods
- `03-Interpolation/` : Lagrange, Newton, splines
- `04-Numerical-Differentiation-Integration/` : finite differences, quadrature
- `05-ODEs/` : Euler, Heun, Runge-Kutta methods
- `problems/` : domain-specific problem sets (chemistry / telecom)
- `assets/` : images and datasets

## Notebook standard
Each notebook follows the same structure:
1. Definition of the method (theory)
2. Applications (theory + code)
3. Examples (theory + code)
4. Student exercises (statements only)

## Requirements
Most notebooks run on standard Colab. A minimal dependency list is provided in `requirements.txt`.

## License
This project is released under the license specified in `LICENSE`.

## Citation
If you use this material for teaching or derivative work, please cite this repository (see `CITATION.cff`).
