# ODSML-Assignment

## Overview
The assignment covers foundational concepts and practical applications of optimization techniques, including:
- Gradient Descent
- Newton’s Method
- Hessian Analysis and Local Optimality
- Applied optimization on real functions and small datasets
- Comparison between solvers and conceptual understanding of Quasi-Newton methods

## Part A: Warm-up
### A1. Gradient Descent Recap
- explain why the gradient descent update rule
  w<sub>k</sub> = w<sub>k</sub> − α ∇f(w<sub>k</sub>)
leads us closer to a (local) minimum, provided α is suitably chosen.
- Give an example of how you might pick a fixed step size versus using a simple Armijo line search. Briefly discuss one advantage of line search in practice.

### A2. Newton’s Method
Given f(x) = x<sup>4</sup> - 4x<sup>2</sup> + 5

- Derive f'(x) and f"(x).
- Show the Newton update formula in 1D: x<sub>k+1</sub> = x<sub>k</sub> − (f'(x<sub>k</sub>)/f'(x<sub>k</sub>))
- If x<sub>0</sub> = 2, manually compute x<sub>1</sub> and x<sub>2</sub>, then comment on whether you’re converging to a local min or something else.

### A3. Hessian & Local Optimality
(a) If you have the Hessian ∇<sup>2</sup>f(w), explain in words how and why its eigenvalues indicate whether you have a local maximum, local minimum, or saddle point.
(b) Suppose ∇<sup>2</sup>f(w<sup>*</sup> ) has both positive and negative eigenvalues. What kind of critical point is w<sup>*</sup> ?

## Part B: Applied Coding Tasks
### B1. Minimizing a Real Function
