# ODSML-Assignment
Part A: Warm-up (Total: 30 marks)
A1. Gradient Descent Recap (10 marks)
Consider a function f(w) in R
d
. Let ∇f(w) be its gradient.
(a) In your own words, explain why the update rule
wk+1 = wk − α ∇f(wk)
leads us closer to a (local) minimum, provided α is suitably chosen.
(b) Give an example of how you might pick a fixed step size versus using a simple Armijo line
search. Briefly discuss one advantage of line search in practice.
A2. Newton’s Method (10 marks)
You have f(x) = x
4 − 4x
2 + 5 (1D).

(a) Derive f
′
(x) and f
′′(x).

(b) Show the Newton update formula in 1D: xk+1 = xk −
f
′
(xk)
f
′′(xk)
.

(c) If x0 = 2, manually compute x1 and x2, then comment on whether you’re converging to a
local min or something else.
