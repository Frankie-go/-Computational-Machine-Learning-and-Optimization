# -Computational-Machine-Learning-and-Optimization

🌿 Smart Greenhouse Ventilation Optimization
📌 Project Summary
This project builds a nonlinear optimization model for smart greenhouse ventilation control. The goal is to minimize electricity cost while maintaining optimal temperature conditions for crop growth over a 48-hour period. A multi-objective approach is used to balance energy consumption and temperature deviation.

🧠 Key Objectives
Minimize ventilation cost by adjusting the hourly air exchange rate.

Maintain ideal greenhouse temperature close to a target value.

Explore tradeoffs between electricity cost and temperature deviation.

Evaluate solver performance using a variety of nonlinear optimization solvers.

🔧 Methodology
Nonlinear cost function: Ventilation cost is modeled as a cubic function of airflow rate.

Temperature dynamics: Indoor temperature evolves hourly based on the previous temperature and outdoor temperature, influenced by the ventilation rate.

Constraints:

Indoor temperature must stay within allowable bounds.

Ventilation rate is bounded between 0% and 100%.

📊 Optimization Tasks
Task 1 - Cost Minimization
Objective: Minimize electricity cost
Result: Optimal strategy ventilates only between hour 11-15; cost ≈ £90.61

Task 2 - Temperature Deviation Minimization
Objective: Minimize deviation from 27°C target
Result: 100% ventilation in early hours; cost ↑ to £1607.5

Task 3 - Tradeoff Optimization
Objective: Minimize weighted sum of cost and temperature deviation
Result: A balanced penalty (λ = 1.0) yields cost ≈ £157.7, deviation ≈ 4.02

Task 4 - Solver Comparison
Tested solvers: BARON, CONOPT, KNITRO, SNOPT, OCTERACT, etc.
Best performance: CONOPT and KNITRO (fastest & accurate)

🧪 Tools and Languages
Python & AMPL modeling

Solvers: CONOPT, KNITRO, BARON via NEOS Server

🧭 Recommendations
Incorporate sunlight heat gain and heat loss for more realistic modeling.

Extend model with robustness for power failures or weather extremes.

📌 Conclusion
This project demonstrates the effectiveness of nonlinear optimization in smart agriculture. By tuning ventilation rates intelligently, energy consumption can be reduced significantly while maintaining crop-friendly temperatures.

