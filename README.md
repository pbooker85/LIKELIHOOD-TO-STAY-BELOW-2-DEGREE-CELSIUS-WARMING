# Likelihood to Stay Below 2°C of Global Warming

## Overview

Uncertainty in Earth's response to increasing atmospheric CO₂ concentrations remains one of the central challenges in projecting future climate change. In particular, uncertainty in **equilibrium climate sensitivity (ECS)** and **transient climate response (TCR)** strongly influences projections of global mean surface temperature (GMST).

This repository contains the computational analysis developed for my M.S. thesis in Atmospheric Sciences at the University at Albany, SUNY:

> **Assessment of the Likelihood to Stay Below 2°C Warming: Combining Modeling and Scenario Uncertainty**

The project combines a **two-layer energy balance model (EBM)** with **CMIP6 climate-model experiments**, climate-sensitivity analysis, and an **emerging-constraint approach based on the Gregory method** to investigate uncertainty in climate sensitivity and its implications for the likelihood of remaining below 2°C of global warming.

The overall objective is to connect uncertainty in climate sensitivity with projections of future GMST under different emissions scenarios.

---

## Research Questions

The analysis addresses several related questions:

1. How do CMIP6 models estimate **transient climate response (TCR)** and **equilibrium climate sensitivity (ECS)**?
2. How can a two-layer energy balance model be calibrated to reproduce characteristics of CMIP6 climate-model behavior?
3. How does the **Gregory method** estimate ECS from abrupt CO₂-increase experiments?
4. Can observed historical warming provide an **emerging constraint** on climate sensitivity?
5. How does constraining climate sensitivity affect projected global mean surface temperature?
6. What is the resulting likelihood of remaining below **2°C of global warming** under a given emissions scenario?

---

## Methodology

### Two-Layer Energy Balance Model

A two-layer energy balance model is used to represent the climate system as a simplified representation of the atmosphere/ocean surface layer and the deeper ocean.

The model provides a computational framework for examining the relationship between:

* Radiative forcing
* Global mean surface temperature
* Ocean heat uptake
* Climate feedback
* Equilibrium climate sensitivity
* Transient climate response

The EBM is calibrated and evaluated using information derived from CMIP6 climate-model experiments.

---

### Transient Climate Response (TCR)

TCR is evaluated using the standard **1% per year atmospheric CO₂ increase experiment**, in which CO₂ concentration increases exponentially until reaching approximately a doubling after 70 years.

The analysis examines the temperature response of CMIP6 models and compares those responses with the two-layer EBM.

The repository includes:

* `CMIP6_1%_TCR_experiment.ipynb`
* `CMIP6_TCR_F2.ipynb`

These notebooks contain calculations associated with the TCR experiment and radiative forcing relationships.

---

### Equilibrium Climate Sensitivity (ECS)

ECS represents the eventual equilibrium global mean surface temperature response to a doubling of atmospheric CO₂ after the climate system reaches equilibrium.

The repository investigates ECS using both the two-layer EBM and CMIP6 climate-model output.

Relevant notebooks include:

* `CMIP6_4xco2.ipynb`
* `ECS_comparison_Gregory_GCMs.ipynb`
* `ECS_partial_derivative_analysis_with_sympy_and_plots.ipynb`

The analysis also examines relationships between radiative forcing, temperature response, and the parameters controlling climate sensitivity.

---

## Gregory Method

The **Gregory method** is used to estimate ECS from abrupt CO₂-increase climate-model experiments.

The method relates changes in top-of-atmosphere radiative imbalance to changes in global mean surface temperature. The resulting regression provides estimates of the effective climate feedback and equilibrium climate sensitivity.

This analysis is contained primarily in:

* `ECS_comparison_Gregory_GCMs.ipynb`
* `Overlay_Gregory_GCM.ipynb`

The repository also includes additional analysis examining the mathematical sensitivity of the ECS calculation:

* `ECS_partial_derivative_analysis_with_sympy_and_plots.ipynb`

---

## Emerging Constraint

A central component of the project is an **emerging-constraint analysis**.

The approach investigates whether the relationship between an observable aspect of historical climate change and an uncertain model parameter—in this case climate sensitivity—can be used to constrain the range of possible future climate responses.

The analysis compares modeled historical warming with observational estimates and examines the resulting relationship with climate sensitivity.

The primary notebook for this work is:

`Gregory_emerging_constraint.ipynb`

This analysis follows methods discussed in the climate-sensitivity literature, including work on constraining CMIP6 climate sensitivity using historical warming.

---

## Global Mean Surface Temperature and the 2°C Threshold

The final stage of the analysis connects climate sensitivity and scenario uncertainty to projections of global mean surface temperature.

`GMST_probability.ipynb`

is used to investigate the probability distribution of projected GMST and the likelihood that warming remains below the **2°C threshold relative to the preindustrial baseline**.

The analysis considers how uncertainty in both the climate response and future emissions/scenario pathways contributes to uncertainty in the resulting temperature projections.

---

## Repository Structure

| Notebook                                                     | Description                                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------------------- |
| `CMIP6_1%_TCR_experiment.ipynb`                              | Analysis of the CMIP6 1%/yr CO₂ experiment and transient climate response |
| `CMIP6_4xco2.ipynb`                                          | Analysis of abrupt 4×CO₂ experiments and climate response                 |
| `CMIP6_TCR_F2.ipynb`                                         | TCR and radiative-forcing analysis                                        |
| `ECS_comparison_Gregory_GCMs.ipynb`                          | Comparison of ECS estimates using the Gregory method                      |
| `ECS_partial_derivative_analysis_with_sympy_and_plots.ipynb` | Mathematical sensitivity and partial-derivative analysis of ECS           |
| `GMST_probability.ipynb`                                     | GMST probability and 2°C threshold analysis                               |
| `Gregory_emerging_constraint.ipynb`                          | Emerging-constraint analysis using historical warming                     |
| `Overlay_Gregory_GCM.ipynb`                                  | Visualization and comparison of Gregory-method results                    |

---

## Research Workflow

The notebooks collectively represent the following analysis pathway:

```text
CMIP6 Climate-Model Experiments
              │
              ▼
     TCR and ECS Analysis
              │
              ▼
   Two-Layer Energy Balance Model
              │
              ▼
       Gregory Method
              │
              ▼
     Emerging Constraint
              │
              ▼
   Constrained Climate Sensitivity
              │
              ▼
   Global Mean Temperature
              │
              ▼
 Probability of Remaining Below 2°C
```

---

## Key Concepts

The project brings together several important components of climate-system analysis:

* **CMIP6 climate models**
* **Two-layer energy balance modeling**
* **Transient Climate Response (TCR)**
* **Equilibrium Climate Sensitivity (ECS)**
* **Radiative forcing**
* **Ocean heat uptake**
* **Global mean surface temperature (GMST)**
* **Gregory regression**
* **Emerging constraints**
* **Scenario uncertainty**
* **Climate-sensitivity uncertainty**
* **Probability of remaining below 2°C warming**

---

## Scientific Context

Climate projections contain multiple sources of uncertainty. These include uncertainty in the physical response of the climate system as well as uncertainty in future greenhouse-gas emissions and socioeconomic development.

This project focuses on the interaction between these sources of uncertainty.

In particular, it examines whether information from the historical climate record can be used to constrain the range of climate sensitivity represented by climate models, and how such constraints affect projections of future warming.

The work is intended as a computational investigation of climate-sensitivity and scenario uncertainty rather than as a standalone climate prediction.

---

## Data and Computational Methods

The analysis is conducted primarily using **Python and Jupyter Notebooks**.

The computational workflow makes use of climate-model data and analytical methods associated with CMIP6 experiments, including:

* 1% per year CO₂ increase experiments
* Abrupt 4×CO₂ experiments
* Historical simulations
* Global mean surface temperature
* Top-of-atmosphere radiative imbalance
* Radiative forcing

The notebooks contain the calculations, analysis, and visualizations used throughout the project.

Additional documentation of data sources, Python package requirements, and reproducibility procedures will be added as the repository is developed.

---

## Thesis

This repository supports research conducted as part of my:

**M.S. in Atmospheric Sciences**
University at Albany, SUNY
Albany, New York

**Thesis:**
*Assessment of the Likelihood to Stay Below 2°C Warming: Combining Modeling and Scenario Uncertainty*

The project integrates climate modeling, CMIP6 analysis, uncertainty assessment, scientific literature, and quantitative analysis to investigate uncertainty in future global warming.

---

## Status

This repository represents an ongoing effort to organize and document the computational work associated with the thesis.

The notebooks contain the primary analysis and are being progressively organized and documented to improve readability, reproducibility, and accessibility.

---

## Author

**Peter Booker**

M.S. Atmospheric Sciences
University at Albany, SUNY

B.S. Geology
Virginia Tech

---

## References

Key scientific methods and concepts used in this project are based on the published climate-science literature, including research concerning:

* Climate sensitivity
* CMIP6
* Transient climate response
* Gregory regression
* Emerging constraints
* Historical warming
* Two-layer energy balance models

A complete bibliography and formal citation information will be added as the repository is further developed.

