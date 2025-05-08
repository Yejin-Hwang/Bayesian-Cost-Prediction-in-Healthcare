## 🩺 Bayesian vs Frequentist Healthcare Cost Prediction

This project compares **Bayesian Linear Regression** (using the `rethinking` R package) and traditional **Frequentist Linear Regression** for predicting individual healthcare costs. The analysis is based on the Medical Cost Personal Dataset (n = 1338), and the goal was to assess the predictive performance, interpretability, and uncertainty quantification of both approaches.

### 🔍 Key Techniques
- Full Bayesian workflow using `quap()` and `ulam()` with HMC sampling
- Posterior visualization, traceplots, rank plots, and convergence diagnostics
- Model comparison using RMSE, MAE, R², and WAIC
- Hierarchical model structure with group-level intercepts for region
- Interaction term analysis (e.g., `BMI × Smoker`) and nonlinear effects (e.g., `Age²`)

### 📊 Key Results
| Model | RMSE | MAE | R² | WAIC |
|-------|------|-----|----|------|
| Frequentist Linear Regression | 4930.55 | 2952.02 | 0.8409 | N/A |
| Bayesian Linear Regression    | 4796.80 | 2888.05 | 0.8430 | 1857.32 |

- **Bayesian model showed slightly better predictive accuracy**
- **Uncertainty visualization and posterior interpretation were key advantages**

📄 [View Full Report (PDF)](./Healthcare_Cost_Prediction_Comparative_Study_yejin.pdf)
