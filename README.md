[README.md](https://github.com/user-attachments/files/34651523/README.md)
# Regression Discontinuity: Bandwidths, Manipulation and Close Elections

## Objective

I examined how bandwidth choices and differences around a cutoff affect the credibility of regression discontinuity estimates.

## Methodology

- Simulated a grant with a known effect and compared global quadratic and local linear estimates.
- Repeated the simulation 300 times to compare bias, variability and root mean squared error across bandwidths.
- Tested for sorting across the cutoff and jumps in pre-treatment characteristics.
- Used Lee, Moretti and Butler’s (2004) election data to estimate the effect of a narrow Democratic win on liberal representation.
- Built a local linear RD estimator with triangular weights and checked it against `rdrobust`.

## Key Findings

For a true grant effect of 8 percentage points, I found that the global quadratic estimated 3.57 points, while the local linear fit estimated 7.89 points at a bandwidth of 16.1. Across the simulations, a bandwidth of 20 had the lowest root mean squared error.

The density test detected sorting across the cutoff, with p = 0.0022. My covariate test found no clear jump in the original prior score but detected the planted 5-point jump.

In the election data, I estimated that barely electing a Democrat increased liberal representation by 46.491 ADA points. My own RD function passed all checks against `rdrobust`.
