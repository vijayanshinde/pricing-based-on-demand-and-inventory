## Dynamic Pricing Based on Demand Curves (Exploration Phase Completed)

This project implements dynamic pricing under inventory constraints by learning demand curves, specifically tailored to a telecom setting where unused GPU hardware during off-peak hours (e.g., midnight to 5 AM) is rented out to external clients. This monetizes idle infrastructure and contributes to new revenue streams.

### Problem Context:

Telecom companies operate under a B2C model where pricing must balance competitive market conditions and optimal inventory utilization. We treat this as a **primal-dual optimization problem**, considering **two customer types**:

* **Reserved**: Pays more and has guaranteed allocation.
* **Pre-emptive**: Pays less but may lose access if capacity runs out.

The solution approach is based on the paper:
📄 *“A Primal-Dual Learning Algorithm for Personalized Dynamic Pricing with an Inventory Constraint”* by Ningyuan Chen and Guillermo Gallego
→ [Link to paper](https://arxiv.org/pdf/1812.09234)
→ Also available in this repository as:
**`Main paper - Pimal dual learning algorithm-compressed.pdf`**

---

###  Phase 1: Exploration (Completed)

The **exploration phase** of the algorithm is implemented and demonstrated in the Jupyter Notebook:
📁 **`exploration_2_cust_type.ipynb`**

In this notebook:

* Demand is simulated for both **reserved** and **pre-emptive** customer types.
* A range of experimental prices is tested (using upper and lower bounds).
* **Demand observations** are collected at each price point.
* The **dual variable** (shadow price of inventory) is estimated based on observed demand.
* The **optimal price** for each customer type is computed such that it exceeds the dual value.


---

### Next Steps:

After exploration, the next stage is **Phase 2: Exploitation**, where the learned prices are used to allocate inventory and generate revenue. Model performance will be evaluated end-to-end, and iterations will follow as needed.

---

