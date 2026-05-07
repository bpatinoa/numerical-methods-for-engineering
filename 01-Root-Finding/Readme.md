# Module 01 — Root Finding

> **Numerical Methods for Engineering** | `bpatinoa/numerical-methods-for-engineering`

This module covers numerical methods for finding roots (zeros) of nonlinear equations $f(x) = 0$. All notebooks are self-contained Google Colab documents: open the link and press **Run All**.

---

## Notebooks in This Module

| # | Notebook | Method | Status |
|---|----------|--------|--------|
| 01 | [`01_Bisection.ipynb`](./01_Bisection.ipynb) | Bisection Method | ✅ Ready |
| 02 | [`02_Newton_Raphson.ipynb`](./02_Newton_Raphson.ipynb) | Newton-Raphson Method | ✅ Ready |
| 03 | `03_Secant.ipynb` | Secant Method | 🔜 Coming soon |
| 04 | `04_Regula_Falsi.ipynb` | Regula Falsi (False Position) | 🔜 Coming soon |
| 05 | `05_Fixed_Point.ipynb` | Fixed-Point Iteration | 🔜 Coming soon |
| 06 | `06_Muller.ipynb` | Müller's Method | 🔜 Coming soon |

---

## Method Overview

### 01 — Bisection Method
- **Basis:** Intermediate Value Theorem (IVT)
- **Convergence:** Linear (order 1), rate 1/2 per iteration
- **Requires:** Bracketing interval $[a, b]$ with $f(a)\cdot f(b) < 0$; no derivative
- **Error bound:** $|c_n - r| \leq (b-a)/2^n$
- **Best for:** Robust, guaranteed convergence when a bracket is known

### 02 — Newton-Raphson Method
- **Basis:** First-order Taylor expansion → tangent line intersection
- **Convergence:** Quadratic (order 2) near a simple root
- **Requires:** Good initial guess $x_0$; first derivative $f'(x)$
- **Best for:** Fast refinement when $f'$ is available and $x_0$ is close to root

### 03 — Secant Method *(coming soon)*
- **Basis:** Finite-difference approximation of $f'$ using two previous iterates
- **Convergence:** Superlinear (order ≈ 1.618, golden ratio)
- **Requires:** Two initial guesses $x_0, x_1$; **no derivative needed**
- **Best for:** Newton-Raphson speed without explicit derivative computation

### 04 — Regula Falsi (False Position) *(coming soon)*
- **Basis:** IVT + secant line through bracket endpoints (always maintains bracket)
- **Convergence:** Linear but faster than Bisection in practice
- **Requires:** Bracketing interval; no derivative
- **Best for:** Guaranteed convergence with better speed than Bisection

### 05 — Fixed-Point Iteration *(coming soon)*
- **Basis:** Rewrite $f(x)=0$ as $x = g(x)$; iterate $x_{n+1} = g(x_n)$
- **Convergence:** Linear when $|g'(r)| < 1$ (contraction mapping)
- **Requires:** Valid rearrangement $g$ and initial guess
- **Best for:** Understanding convergence theory; precursor to Newton-Raphson

### 06 — Müller's Method *(coming soon)*
- **Basis:** Quadratic interpolation through three points
- **Convergence:** Order ≈ 1.84 (superlinear)
- **Requires:** Three initial guesses; finds complex roots
- **Best for:** Polynomials and functions with complex roots

---

## Applications Covered

Each notebook contains examples from three domains:

| Domain | Topics |
|--------|--------|
| **General Mathematics** | Polynomials, transcendental equations, fixed points |
| **Chemistry** | Acid-base equilibria, Van der Waals gas, reaction kinetics, solubility |
| **Telecommunications** | Link budgets, BER/SNR (BPSK), transmission lines, antenna resonance |

---

## How to Open in Google Colab

```
https://colab.research.google.com/github/bpatinoa/numerical-methods-for-engineering/blob/main/01-Root-Finding/<NOTEBOOK>.ipynb
```

Example:
```
https://colab.research.google.com/github/bpatinoa/numerical-methods-for-engineering/blob/main/01-Root-Finding/01_Bisection.ipynb
```

---

## References

1. Chapra, S. C., & Canale, R. P. (2015). *Numerical Methods for Engineers* (7th ed.). McGraw-Hill.
2. Burden, R. L., Faires, J. D., & Burden, A. M. (2016). *Numerical Analysis* (10th ed.). Cengage.
3. Press, W. H. et al. (2007). *Numerical Recipes* (3rd ed.). Cambridge University Press.
4. Atkinson, K. E. (1989). *An Introduction to Numerical Analysis* (2nd ed.). Wiley.
5. Goldsmith, A. (2005). *Wireless Communications*. Cambridge University Press.
