# Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

This project transforms NO2 concentration data using a roll-number-parameterized non-linear function and learns parameters of a Gaussian-form probability density function using Maximum Likelihood Estimation (MLE).

---

## Methodology

1. Load dataset and extract NO2 feature (x).
2. Compute roll-number-based parameters.
3. Apply non-linear transformation to obtain z.
4. Estimate PDF parameters using MLE.
5. Plot the learned probability density function.

---

## Transformation Details

- Roll Number: 102313056
- ar = 0.05 × (r mod 7) = 0.1
- br = 0.3 × (r mod 5 + 1) = 0.6

Transformation applied:

z = x + 0.1 * sin(0.6 * x)

---

## PDF Model Used

Gaussian-form Probability Density Function:

p(z) = c * exp(-lambda * (z - mu)^2)

Parameter Estimation:

mu = mean(z)
lambda = 1 / (2 * variance(z))
c = 1 / sqrt(2 * pi * variance(z))

---

## Input

- NO2 concentration values (x)
- Roll Number: 102313056

---

## Output

- Transformed variable (z)
- Estimated parameters: mu, lambda, c
- Learned probability density function plot

