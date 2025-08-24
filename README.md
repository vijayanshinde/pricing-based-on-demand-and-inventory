# Primal-Dual Learning Algorithm for Personalized Dynamic Pricing

This repository contains a **complete implementation** of the *Primal-Dual Learning Algorithm for Personalized Dynamic Pricing with Inventory Constraints*, based on the research paper by Ningyuan Chen and Guillermo Gallego. The project combines **machine learning, optimization, and dynamic pricing** to solve a real-world challenge: maximizing revenue under limited inventory while serving different customer types.

---

##  Project Overview

Dynamic pricing is a fundamental tool in modern industries such as e-commerce, telecommunications, cloud computing, and transportation. The key challenge lies in **setting prices dynamically** while accounting for:

* Inventory constraints
* Customer heterogeneity
* Uncertainty in demand

This project addresses the challenge using a **Primal-Dual optimization framework**, where:

* The **Primal problem** represents maximizing revenue under constraints.
* The **Dual problem** estimates the *shadow price* of inventory, guiding price decisions.
* The algorithm operates in two phases:

  1. **Exploration:** Learn demand curves using experimental pricing.
  2. **Exploitation:** Apply learned demand models to optimize pricing dynamically.

---

##  Key Features

* **Demand Simulation:**

  * Logistic demand functions to capture realistic customer behavior.
  * Noise injection to reflect market randomness.
  * Multiple customer types (Reserved vs Preemptive) with different price sensitivities.

* **Demand Estimation via Machine Learning:**

  * Implemented using **Random Forests** and **LightGBM** for non-parametric demand curve fitting.
  * Captures non-linearities and variability better than classical parametric models.
  * Enables robust prediction of demand at untested prices.

* **Optimization Techniques:**

  * Dual variable estimation using `scipy.optimize` minimization routines.
  * Interval narrowing strategy to converge to optimal pricing decisions.
  * Oracle revenue benchmark for regret analysis.

* **Dynamic Pricing Strategy:**

  * Prices adapted in real time based on customer type and inventory availability.
  * Exploitation phase ensures near-optimal performance with minimal regret.

* **Evaluation Metrics:**

  * **Revenue:** Actual vs Oracle.
  * **Regret:** Cumulative difference between algorithm and benchmark.
  * **Visualization:** Demand curves, price intervals, revenue trends.

---

##  Technologies Used

* **Programming Language:** Python (Jupyter Notebook)
* **Core Libraries:**

  * `numpy`, `pandas` → numerical + data manipulation
  * `scipy.optimize` → primal-dual optimization
  * `matplotlib`, `seaborn` → visualizations
  * `scikit-learn` → Random Forests, GridSearchCV
  * `lightgbm` → advanced boosting for demand estimation

---

## 📈 Results

* Learned demand functions that are **price-biased and stochastic**, mimicking real customer behavior.
* Achieved near-oracle revenues with regret consistently between 0% and 10%, well within the 15% threshold for strong performance cited in the literature.
* Regret effectively captures the deviation between actual revenue and the optimal benchmark (oracle revenue).
* Demonstrated the strength of combining **machine learning with optimization theory** in real-world pricing problems.



---

##  Why This Project is Special

* Integrates **machine learning** with **mathematical optimization** in a full pipeline.
* Moves beyond toy problems — implements a **research-grade algorithm** end-to-end.
* Directly relevant to today’s **data science, fintech, and telecom industries**, where dynamic pricing and demand learning are business-critical.
* Demonstrates practical skills in:

  * Applied ML (Random Forests, LightGBM)
  * Optimization under uncertainty
  * Translating academic research into working code

---

## ⚙️ How to Run

1. Clone this repository

   ```bash
   git clone https://github.com/vijayanshinde/primal-dual-pricing.git
   cd primal-dual-pricing
   ```
2. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook

   ```bash
   jupyter notebook primal_dual_algo.ipynb
   ```
4. (Optional) Run automated demo

   ```bash
   ./run_demo.sh
   ```

---

## 📄 References

* Chen, Ningyuan, and Guillermo Gallego. *A Primal-Dual Learning Algorithm for Personalized Dynamic Pricing with an Inventory Constraint*. [arXiv:1812.09234](https://arxiv.org/pdf/1812.09234).
* Additional ML + pricing literature referenced in the report.


