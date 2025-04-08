# ODSML Assignment 2

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
- If you have the Hessian ∇<sup>2</sup>f(w), explain in words how and why its eigenvalues indicate whether you have a local maximum, local minimum, or saddle point
- Suppose ∇<sup>2</sup>f(w<sup>*</sup> ) has both positive and negative eigenvalues. What kind of critical point is w<sup>*</sup> ?

## Part B: Applied Coding Tasks
### B1. Minimizing a Real Function
Pick any real-valued function from R<sup>2</sup> → R that is reasonably smooth (e.g., a small polynomial, a 2D Gaussian, or something from your industry data).
- Implement (or use a library function for) gradient descent and Newton’s method to find a local min from some chosen start point.
- Plot the iteration paths if possible (like a contour plot in 2D), or else just track the objective values over iteration.
- Compare iteration counts, final accuracies, or ∥∇f∥ at the end. Are they different? Why?

### B2. Small Data Problem
Take a small dataset (2–10 features) for regression or classification. For instance:
• A mini logistic regression example for binary classification,
• or a linear regression on 10–100 data points.
Use an existing solver (like scikit-learn’s LogisticRegression or LinearRegression) or a library with advanced optimizers:
- Explain how the library likely implements gradient-based optimization (just a short guess about whether it uses a quasi-Newton or gradient descent under the hood).
- Compare different solver/optimizer settings (like Newton-CG, LBFGS, or SGD if avail-
able). Summarize the final model performance (accuracy/MSE), iteration counts, or any relevant solver logs if the library provides them.
- Interpret the results: which solver is fastest in iteration count? Which might be less stable if the function is ill-conditioned?

## Part C: Conceptual Intuition on Quasi-Newton vs. Exact Newton
- In your own words, why might we choose quasi-Newton instead of the exact Newton’s method for a data science problem?
- Suppose your dataset has 50,000 features. Which approach is likely more feasible, and why?
- If you tested a quasi-Newton library function in Part B, comment on how it felt. Did you notice any difference from a full Newton approach?

