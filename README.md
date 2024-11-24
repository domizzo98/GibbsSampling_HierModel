# Bayesian Hierarchical Models Project

This project implements Gibbs sampling for Bayesian hierarchical models to analyze student math scores from multiple schools in the U.S. The main objectives are:

- Estimate global and school-specific effects.

- Assess the impact of covariates on student performance.

- Diagnose and verify the convergence of Gibbs sampling algorithms.

### Hierarchical Models

- Without Covariates: Student scores modeled with school-specific mean effects.

- With Covariates: Regression framework with school-specific regression coefficients to account for student-level predictors.

### Dataset

The dataset contains:

- Y<sub>i,j</sub> : Score of student i in school j.

- x<sub>i,j</sub> : Covariates of student i in school j (when covariates are included).

- m: Number of schools.

- n<sub>j</sub> : Number of students in school j.

Files:

scores_without_covariates.csv

scores_with_covariates.csv

Scripts

gibbs_sampler_no_covariates.py: Implements the Gibbs sampler for the model without covariates.

gibbs_sampler_with_covariates.py: Implements the Gibbs sampler for the model with covariates.

Instructions

Clone the repository:

git clone https://github.com/yourusername/bayesian_hierarchical_models.git

Navigate to the project directory:

cd bayesian_hierarchical_models

Install required libraries:

pip install numpy scipy matplotlib

Run the scripts:

Without covariates:

python gibbs_sampler_no_covariates.py

With covariates:

python gibbs_sampler_with_covariates.py

Outputs

Trace Plots: Visualize parameter chains for convergence.

Boxplots: Assess parameter stability across iterations.

Autocorrelation Plots: Evaluate mixing and dependency in the chains.

Results and Diagnostics

Trace Plots:

Demonstrate convergence for  (without covariates) and  (with covariates).

Boxplots:

Show stationary distribution across samples.

Autocorrelation:

Low autocorrelation indicates efficient parameter space exploration.

Key Findings

Without Covariates:

Borrowing information across schools stabilizes estimates for schools with smaller sample sizes.

School-specific means  are shrunk towards the global mean .

With Covariates:

Regression coefficients vary significantly across schools, highlighting heterogeneity.

Covariates such as socioeconomic status and free lunch eligibility show measurable impacts on scores.

References

Hoff, Peter D. A First Course in Bayesian Statistical Methods.

Project slides and provided datasets.
