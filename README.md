# 🩺 Bayesian vs Frequentist Healthcare Cost Prediction

A comprehensive comparative study of **Bayesian Linear Regression** and traditional **Frequentist Linear Regression** for predicting individual healthcare costs using the Medical Cost Personal Dataset.

## 📋 Project Overview

This project implements and compares two statistical approaches for healthcare cost prediction:

- **Frequentist Linear Regression**: Traditional statistical approach using maximum likelihood estimation
- **Bayesian Linear Regression**: Probabilistic approach using Hamiltonian Monte Carlo (HMC) sampling with the `rethinking` R package

The analysis is based on the Medical Cost Personal Dataset (n = 1,338) and evaluates predictive performance, interpretability, and uncertainty quantification of both approaches.

## 🔍 Key Features

### Bayesian Analysis
- Full Bayesian workflow using `quap()` and `ulam()` with HMC sampling
- Posterior visualization, traceplots, rank plots, and convergence diagnostics
- Hierarchical model structure with group-level intercepts for region
- Interaction term analysis (e.g., `BMI × Smoker`) and nonlinear effects (e.g., `Age²`)
- Uncertainty quantification and credible intervals

### Model Comparison
- Performance metrics: RMSE, MAE, R², and WAIC
- Cross-validation and model diagnostics
- Statistical significance testing
- Residual analysis and model assumptions

## 📊 Key Results

| Model                         | RMSE    | MAE     | R²     | WAIC    |
| ----------------------------- | ------- | ------- | ------ | ------- |
| Frequentist Linear Regression | 4930.55 | 2952.02 | 0.8409 | N/A     |
| Bayesian Linear Regression    | 4796.80 | 2888.05 | 0.8430 | 1857.32 |

### Key Findings
- **Bayesian model showed slightly better predictive accuracy**
- **Uncertainty visualization and posterior interpretation were key advantages**
- **Bayesian approach provides more robust uncertainty quantification**
- **Both models performed well with R² > 0.84**

## 📁 Project Structure

```
├── data/
│   └── insurance.csv                    # Medical Cost Personal Dataset
├── notebooks/
│   └── Health Care Cost Prediction Frequentist vs bayesian method.ipynb
├── results/
│   ├── bayesian Final presentation_yejin.pdf
│   ├── Bayesian Final report_yejin hwang.pdf
│   ├── Healthcare_Cost_Prediction_Comparative_Study_yejin.pdf
│   ├── charge.png                       # Charge distribution visualization
│   ├── cor1.png, cor2.png, cor3.png    # Correlation plots
│   ├── dataset.png                      # Dataset overview
│   ├── Frequentist vs bayesian.png      # Model comparison
│   ├── interaction.png                  # Interaction effects
│   ├── pairs_plot.pdf                   # Pairwise relationships
│   ├── posterior distribution.png       # Posterior distributions
│   ├── posterior summary.png            # Posterior summaries
│   ├── result-HMC.png                   # HMC sampling results
│   ├── traceplot.png                    # MCMC trace plots
│   └── trankplot.png                    # Rank plots for diagnostics
├── docs/
│   ├── Bayesian final project format.docx
│   ├── Bayesian Final report_yejin hwang.docx
│   ├── Bayesian Proposal of Final Project_yejin.docx
│   ├── COSC 6338_Final report_group4.docx
│   └── bayesian Final presentation_yejin.pptx
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- R (version 4.0 or higher)
- Required R packages:
  - `rethinking` (for Bayesian analysis)
  - `ggplot2` (for visualization)
  - `dplyr` (for data manipulation)
  - `Hmisc` (for statistical functions)
  - `cowplot` (for plot arrangement)
  - `WVPlots` (for additional visualizations)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Yejin-Hwang/Bayesian-Cost-Prediction-in-Healthcare.git
cd Bayesian-Cost-Prediction-in-Healthcare
```

2. Install required R packages:
```r
install.packages(c("ggplot2", "dplyr", "Hmisc", "cowplot", "WVPlots"))
# Install rethinking package
install.packages("rethinking")
```

3. Run the analysis:
```bash
# Open the Jupyter notebook
jupyter notebook notebooks/Health\ Care\ Cost\ Prediction\ Frequentist\ vs\ bayesian\ method.ipynb
```

## 📈 Methodology

### Data Preprocessing
- Exploratory data analysis and visualization
- Feature engineering and transformation
- Missing value handling
- Outlier detection and treatment

### Model Development
1. **Frequentist Approach**:
   - Linear regression with maximum likelihood estimation
   - Model selection using AIC/BIC
   - Cross-validation for performance evaluation

2. **Bayesian Approach**:
   - Prior specification and justification
   - HMC sampling with `ulam()` function
   - Convergence diagnostics (trace plots, rank plots)
   - Posterior predictive checks

### Evaluation Metrics
- **RMSE**: Root Mean Square Error
- **MAE**: Mean Absolute Error
- **R²**: Coefficient of determination
- **WAIC**: Widely Applicable Information Criterion (Bayesian)

## 📊 Visualizations

The project includes comprehensive visualizations:

- **Data Exploration**: Distribution plots, correlation matrices, pairwise relationships
- **Model Diagnostics**: Residual plots, Q-Q plots, leverage plots
- **Bayesian Analysis**: Posterior distributions, trace plots, rank plots
- **Model Comparison**: Performance metrics comparison, prediction intervals

## 📚 References

- McElreath, R. (2020). *Statistical Rethinking: A Bayesian Course with Examples in R and Stan* (2nd Edition)
- Original dataset: [Kaggle - Health Care Cost Prediction](https://www.kaggle.com/code/ruslankl/health-care-cost-prediction-w-linear-regression/input)
- Gelman, A., Carlin, J. B., Stern, H. S., Dunson, D. B., Vehtari, A., & Rubin, D. B. (2013). *Bayesian Data Analysis* (3rd Edition)

## 👥 Author

**Yejin Hwang**
- Texas A&M University-Corpus Christi
- Course: COSC 6338 - Bayesian Inference
- Final Project: Spring 2025

## 📄 License

This project is for educational purposes as part of the Bayesian Inference course at Texas A&M University-Corpus Christi.

## 🤝 Contributing

This is a final project submission. Contributions are not expected, but feedback and suggestions are welcome.

## 📞 Contact

For questions about this project, please contact the author or refer to the course materials.

---

*This project demonstrates the practical application of Bayesian statistical methods in healthcare cost prediction, showcasing the advantages of probabilistic modeling over traditional frequentist approaches.*
