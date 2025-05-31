# Dynamic-Pricing-based-on-Demand-Curves
Dynamic Pricing by learning Demand Curves with Inventory constraint

This is an ongoing project and the work shown is incomplete. In telecom industries, the GPUs or high-speed computing hardware is used to optimize their 4g, 5g, 6g networks. But when network is not utilized at their full extent by users or customers which is at non-peak hours for e.g. in night (midnight to 5 am), this computing hardware is almost ideal which is waste of very useful resources. Hence, it is being strategized by the company that they can rent this hardware resources to other clients who need such computing hardware which can contribute as new income to the revenue. 


Since, the industry comes into B2C business model, the product pricing is very competitive such they need to offer optimal prices which will create balanced demand with respect to achieving maximum revenue and correctly valuing the inventory. This becomes a primal dual problem which can be solved using Primal dual algorithm. We also consider 2 customer types: reserved and pre-emptive. Reserved is willing to pay more as they have confirmed reserve hardware after booking. The pre-emptive one is uncertain if they will get the hardware and can be refunded back. 


We refer to a research paper titled as: A Primal-dual Learning Algorithm for Personalized Dynamic Pricing with an Inventory Constraint by Ningyuan Chen and Guillermo Gallego (1812.09234).
This paper basically follows a primal dual algorithm which solves our problem and achieves a near to optimal price at the ending of booking phase of hardware using dynamic pricing. 


The algorithm is divided into two parts: Exploration and Exploitation which in phase 1 experiments prices and studies real time demand on which temporary optimal price is obtained. Taking that optimal price to second phase we estimate future demand by price and demand relation and compare that to inventory after which we understand if we have enough inventory for current temporary optimal price. If demand is below inventory then we keep prices same, but if demand is more than inventory then we need to increase the prices.

Currently we are developing in phase 1 i.e. exploration. Here, we found that there are different methods to simulate demand and we are trying out different methods. Demand simulation becomes important as if we have good demand then our algorithm mis re4ally working well or if demand simulation is not good then we may go into fake assumption that algorithm is running well and cause problem in future while taking real trials.


I have shared a rough code which shows Phase 1: exploration, where we simulate demand, throw experimental prices with higher and lower bound, calculate dual variable which values inventory and then calculate optimal price which is above dual variable value
