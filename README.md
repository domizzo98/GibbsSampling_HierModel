# Bayesian Hierarchical Models Project

This project implements Gibbs sampling for Bayesian hierarchical models to analyze student math scores from multiple schools in the U.S. The main objectives are:

- Estimate global and school-specific effects.

- Assess the impact of covariates on student performance.

- Diagnose and verify the convergence of Gibbs sampling algorithms.

## Hierarchical Models

`Model_with_covariates.ipynb` Without Covariates: Student scores modeled with school-specific mean effects.

- With Covariates: Regression framework with school-specific regression coefficients to account for student-level predictors.

## Outputs

- **Trace Plots**: Demonstrate convergence for  (without covariates) and  (with covariates).

- **Boxplots**: Show stationary distribution across samples.

- **Autocorrelation Plots**: Low autocorrelation indicates efficient parameter space exploration.

## Key Findings

Without Covariates:

- Borrowing information across schools stabilizes estimates for schools with smaller sample sizes.

- School-specific means  are shrunk towards the global mean .

With Covariates:

- Regression coefficients vary significantly across schools, highlighting heterogeneity.

- Covariates such as socioeconomic status and free lunch eligibility show measurable impacts on scores.

## References

Hoff, Peter D. *A First Course in Bayesian Statistical Methods*.

Project slides and provided datasets.
