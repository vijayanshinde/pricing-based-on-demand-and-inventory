

---

# Primal-Dual Learning Algorithm for Personalized Dynamic Pricing

This repository, **`pricing-based-on-demand-and-inventory`**, contains a complete implementation of the *Primal-Dual Learning Algorithm for Personalized Dynamic Pricing with Inventory Constraints*, based on the research paper by Ningyuan Chen and Guillermo Gallego. The project combines **machine learning, optimization, and dynamic pricing** to solve a real-world challenge: maximizing revenue under limited inventory while serving different customer types.

---

## 📊 Project Overview

Dynamic pricing is a key tool in industries like e-commerce, telecommunications, cloud computing, and transportation. The challenge lies in **setting prices dynamically** while accounting for:

- Inventory constraints  
- Customer heterogeneity  
- Uncertainty in demand  

This project addresses the challenge using a **Primal-Dual optimization framework**, where:

- The **Primal problem** maximizes revenue under constraints  
- The **Dual problem** estimates the *shadow price* of inventory to guide pricing  
- The algorithm operates in two phases:
  1. **Exploration** — Learn demand curves via experimental pricing  
  2. **Exploitation** — Use learned models to optimize pricing dynamically  

---

## 🚀 Key Features

- **Demand Simulation**
  - Logistic demand functions with noise injection
  - Multiple customer types (Reserved vs Preemptive)

- **Demand Estimation via Machine Learning**
  - Non-parametric models: Random Forests & LightGBM
  - Captures non-linear demand behavior

- **Optimization Techniques**
  - Dual variable estimation via `scipy.optimize`
  - Interval narrowing for convergence
  - Oracle revenue benchmark for regret analysis

- **Dynamic Pricing Strategy**
  - Real-time price adaptation based on inventory and customer type
  - Near-optimal performance with minimal regret

- **Evaluation Metrics**
  - Revenue vs Oracle
  - Regret analysis
  - Visualizations: demand curves, price intervals, revenue trends

---

## 🧰 Technologies Used

- **Language:** Python (Jupyter Notebook)
- **Libraries:**
  - `numpy`, `pandas` — data handling
  - `scipy.optimize` — optimization
  - `matplotlib`, `seaborn` — visualization
  - `scikit-learn` — Random Forests, GridSearchCV
  - `lightgbm` — boosting for demand estimation

---

## 📈 Results

- Learned demand functions that are **price-sensitive and stochastic**, mimicking real customer behavior  
- Achieved near-oracle revenues with regret consistently between **0% and 10%**, well within the 15% threshold cited in the literature  
- Regret effectively measures deviation from the optimal (oracle) revenue  
- Demonstrated the power of combining **machine learning with optimization theory** in pricing problems  

---

## 🌟 Why This Project Stands Out

- Integrates **ML + optimization** in a full pipeline  
- Goes beyond toy problems — implements a **research-grade algorithm**  
- Relevant to **data science, fintech, and telecom** industries  
- Demonstrates practical skills in:
  - Applied ML (Random Forests, LightGBM)  
  - Optimization under uncertainty  
  - Translating academic research into working code  

---

## ⚙️ How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/vijayanshinde/pricing-based-on-demand-and-inventory.git
   cd pricing-based-on-demand-and-inventory
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook:

   ```bash
   jupyter notebook primal_dual_algo_GK-VS_.ipynb
   ```

4. *(Optional)* Run automated demo:

   ```bash
   ./run_demo.sh
   ```

---

## 📄 References

- Chen, Ningyuan, and Guillermo Gallego. *A Primal-Dual Learning Algorithm for Personalized Dynamic Pricing with an Inventory Constraint*. [arXiv:1812.09234](https://arxiv.org/pdf/1812.09234)
- Additional ML + pricing literature referenced in the report

---
