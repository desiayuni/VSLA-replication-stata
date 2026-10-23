# VSLA Replication Project

Replication of selected results from *Impact of Village Savings and Loan Associations: Evidence from a Cluster Randomized Trial* (Journal of Development Economics, 2016), using household survey data from Malawi.

This is a learning replication. It runs and adapts the original authors' code to reproduce part of the published results, and does not extend the original analysis.


---



## Research Question

Does participation in Village Savings and Loan Associations (VSLAs) improve access to loans among rural households?



---



## Data

- Household-level survey data from Malawi, with baseline and post-treatment observations

- Data source: the original study's replication data. The data is not included in this repository.


---


## About the code

The main do-file is adapted from the replication code provided by the original authors (Ksoll, Lilleor, Lonborg and Rasmussen). I updated the file paths and ran it to replicate selected results from the paper. The robustness checks with household covariates and the treatment effect plots are my own additions, found `dofiles/main_replication.do`


---



## Methodology

- Cluster Randomized Controlled Trial (RCT), Intention-to-Treat (ITT) estimation

- OLS regression with block fixed effects (`i.blocks`) and standard errors clustered at village level

- Outcome : household loan access 



---



## Workflow

- Set up a reproducible folder structure

- Load and inspect the Stata datasets

- Construct transformed variables

- Check baseline balance between treatment and control groups

- Estimate treatment effects on loan access

- Run robustness checks with household covariates

- Export regression outputs and figures



---



## Results

The replication results suggest that participation in the VSLA treatment is associated with a statistically significant increase in access to loans.

- Example result: treatment coefficient of 0.122 (p = 0.002)
- Robustness check: with household controls, the estimated treatment effect moves from approximately 0.104 to 0.097 and remains positive and statistically significant

The coefficients above come from different outputs saved in this repository. See `outputs/`and the replication report for the exact specification behind each estimate.

  The household controls used in the robustness check are:
  - Age of household head
  - Education of household head
  - Female-headed household indicator

The estimates stay similar after adding these controls, which suggests the main result is relatively stable across the specifications reported here. These findings are consistent with the original paper's argument that community-based financial institutions can improve financial inclusion among rural households.

    
  
---



## Figures


![Professional Treatment Effect Plot](./graphs/professional_treatment_plot.png)


![Robustness Plot](./graphs/robustness_plot.png)




---


## Repository Structure

```
dofiles/    -> STATA do-files used for the replication
outputs/    -> regression outputs
graphs/     -> figures (treatment effect plot, robustness plot)
reports/    -> replication report (pdf)
notes/       -> replication notes and documentation
.gitignore
README.md
```

## Replication Report

[Download Replication Report](reports/Desi_Sari_Ayuni_VSLA_Replication_Report.pdf)



## Skills demonstrated

Stata, applied econometrics, data cleaning, causal inference, clustered standard errors, empirical replication, research documentation

## Next steps

- Replicate additional treatment effect tables

- Export regression outputs

- Reproduce figures and tables

- Improve reproducibility workflow

