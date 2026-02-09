# Causal Evaluation of Residential Energy Efficiency Programs
Code for the assessment of causal effect of incentive programs  to encourage energy efficiency retrofits, when implemented by different regional governments.

Context:
## Motivation
Improving residential energy efficiency is a crucial component of global climate policy. In 2019, regional governments implemented new incentive programs to encourage homeowners to retrofit properties older than 10 years.

**Policy Timeline:**
* **Pre-2019:** No anticipation or public discussion of the policies.
* **2019:** Programs announced and discussed in media.
* **End of 2019:** All programs became fully operational.

## 🧪 Experimental Design
The data comes from a quasi-experimental setup where regions were divided into three distinct policy groups:

* **🟢 Program A (High Incentives):** Households received strong financial incentives, including generous subsidies and tax credits for implementing comprehensive energy retrofits.
* **🟡 Program B (Nudges):** Due to budget limitations, households received only information campaigns and small rebates.
* **🔴 Region C (Control):** Households in these regions could still undertake retrofits but received **no subsidies**.

## 📉 The Empirical Challenge
Evaluating these programs is challenging due to **Selection Bias**. Households that participate in energy programs often differ systematically from those that do not. For example, they may be:
* Wealthier
* More environmentally conscious
* Living in specific building types

A simple comparison of means would yield biased estimates. To address this, this project employs **Double Machine Learning (DML)** and **Causal Forests** to control for high-dimensional confounders.

## 🎯 Research Questions
To help policymakers design optimal future policies, this project aims to understand not just *if* the program works, but *why* (mechanism) and *for whom* (heterogeneity).

The analysis is divided into four key tasks:

1.  **Program Effects:** What is the causal effect of **Program A** and **Program B** on *energy consumption* and *energy costs*?
2.  **Non-Energy Outcomes:** What is the causal effect of each program on household *health*?
3.  **Mechanism (IV):** What is the causal effect of the **retrofit itself** on energy consumption and costs? (Using program assignment as an instrument).
4.  **Heterogeneity:** Which types of households responded the most? 
    * *Goal:* Identify groups with the largest (and smallest) treatment effects to target future policies effectively.
