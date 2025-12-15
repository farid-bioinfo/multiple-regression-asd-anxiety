# Multiple Regression Analysis: Anxiety Predictors in ASD

**Multifactorial Statistical Analysis | Gut-Brain Axis Research**

**Author:** Farid Hakimi  
**Date:** December 2025  
**Language:** R

---

## 📋 Project Overview

This project demonstrates advanced multiple regression analysis examining factors that influence anxiety in individuals with Autism Spectrum Disorder (ASD). The analysis explores how gut microbiome diversity, diet quality, sleep duration, and systemic inflammation independently contribute to anxiety levels, providing insights into the multifactorial nature of mental health in neurodevelopmental conditions.

### Research Question

**What independent factors predict anxiety severity in ASD individuals when controlling for confounding variables?**

---

## 🔬 Methodology

### Dataset Characteristics
- **Sample Size:** 60 participants with ASD diagnosis
- **Response Variable:** Anxiety Score (continuous, 0-100 scale)
- **Predictor Variables:**
  - Gut Bacteria Diversity (Shannon index equivalent)
  - Diet Quality Score (0-100 scale)
  - Sleep Hours (per night)
  - C-Reactive Protein (CRP) - Inflammation marker (mg/L)

### Statistical Approach

**Multiple Linear Regression Model:**
```
Anxiety Score = β₀ + β₁(Gut Diversity) + β₂(Diet Quality) + 
                β₃(Sleep Hours) + β₄(CRP Inflammation) + ε
```

**Why Multiple Regression?**

Unlike simple regression (one predictor → one outcome), multiple regression:
- Quantifies the **independent effect** of each predictor
- Controls for confounding relationships between variables
- Assesses **relative importance** of different factors
- Provides comprehensive understanding of multifactorial influences

---

## 📊 Key Findings

### Model Performance

- **R² = 0.728** (73% of anxiety variance explained)
- **Adjusted R² = 0.708** (accounting for number of predictors)
- **F-statistic = 36.82** (p < 0.001) - overall model highly significant
- **Residual SE = 4.77** points on anxiety scale

### Independent Effects of Each Predictor

| Predictor | Coefficient (β) | SE | t-statistic | p-value | Interpretation |
|-----------|----------------|-----|-------------|---------|----------------|
| **Sleep Hours** | **-3.59** | 0.51 | -7.06 | <0.001 | Strongest predictor |
| Gut Diversity | -0.083 | 0.014 | -5.94 | <0.001 | Significant negative effect |
| Diet Quality | -0.285 | 0.047 | -6.02 | <0.001 | Significant negative effect |
| CRP Inflammation | +2.83 | 0.86 | 3.29 | 0.002 | Significant positive effect |

### Practical Impact Analysis

**Real-world effect sizes across observed data ranges:**

| Factor | Observed Range | Total Impact on Anxiety |
|--------|---------------|------------------------|
| **Sleep** | 4-10 hours (6-hour range) | **-22.8 points** |
| **Diet Quality** | 30-98 (68-point range) | -19.2 points |
| **Gut Diversity** | 252-458 (207-unit range) | -17.3 points |
| **Inflammation** | 1.4-4.3 mg/L (2.8-unit range) | +7.9 points |

**Key Insight:** Sleep duration has both the strongest coefficient AND largest practical impact. Improving sleep from 4→10 hours predicts a 22.8-point anxiety reduction - greater than any other single intervention.

### Statistical Interpretation

**Sleep Hours (β = -3.59, p < 0.001):**
- Holding gut diversity, diet, and inflammation constant
- Each additional hour of sleep predicts 3.59-point reduction in anxiety
- This is the **unique contribution** of sleep after accounting for correlations with other factors

**Inflammation (β = +2.83, p = 0.002):**
- Only predictor with positive coefficient
- Higher systemic inflammation associated with increased anxiety
- Suggests immune-brain signalling pathway involvement

---

## 🧠 Scientific Context

### Why This Analysis Matters

**Multifactorial Etiology:** Anxiety in ASD isn't caused by a single factor - it emerges from interactions between:
- Biological systems (gut microbiome, immune function)
- Lifestyle factors (sleep, nutrition)
- Physiological states (inflammation)

**Clinical Implications:**
- **Personalised intervention design:** Target the factor with greatest deficit for each individual
- **Prioritisation guidance:** When resources are limited, sleep intervention shows largest effect
- **Mechanistic insights:** Identifies pathways worth investigating in experimental studies

### Limitations

- **Observational data:** Cannot establish causal relationships
- **Sample size:** n=60 limits generalisability
- **Unmeasured confounders:** Medication use, co-occurring conditions not controlled
- **Cross-sectional design:** Single time-point measurement
- **Self-report bias:** Anxiety and diet scores subject to reporting accuracy

### Future Directions

- Longitudinal studies tracking changes over time
- Intervention trials manipulating specific factors
- Mediation analysis examining pathways (e.g., does gut diversity affect anxiety via inflammation?)
- Larger sample sizes for subgroup analyses
- Integration with metabolomics data (gut bacterial metabolites)

---

## 💻 Technologies Used

**R Programming:**
- Base R statistical functions (`lm()`, `summary()`, `anova()`)
- Regression diagnostics and model validation
- Effect size calculations

**Statistical Methods:**
- Multiple linear regression
- Hypothesis testing (t-tests for coefficients, F-test for overall model)
- Model diagnostics (residual analysis, multicollinearity checks)
- Practical significance assessment

---

## 📁 Repository Structure

```
multiple-regression-asd-anxiety/
├── README.md                           # This file
├── gut_brain_multifactor_data.csv     # Dataset (60 participants, 5 variables)
└── multiple_regression_analysis.R     # R analysis script
```

---

## 🚀 How to Run

### Requirements
- R version 4.0+
- Base R packages (no additional installations needed)

### Execution

```r
# Load and run the analysis
source("multiple_regression_analysis.R")
```

**Outputs:**
- Model summary with coefficients and significance tests
- Practical impact calculations
- Correlation matrix
- Model comparison statistics

---

## 📊 Model Comparison

**Simple vs. Multiple Regression:**

**Model 1 (Sleep Only):**
- R² = 0.287
- Sleep coefficient: β = -3.74

**Model 2 (All Four Predictors):**
- R² = 0.728 (154% improvement)
- Sleep coefficient: β = -3.59 (similar, showing robust effect)

**Interpretation:** Adding gut diversity, diet, and inflammation more than doubles explanatory power, confirming multifactorial nature of anxiety in ASD.

---

## 🎯 Skills Demonstrated

This project showcases:

✅ **Multiple Regression Analysis:** Multivariable modelling with interpretation of partial regression coefficients  
✅ **Confounding Control:** Understanding independent vs. confounded effects  
✅ **Model Comparison:** Simple vs. multiple regression, R² improvement assessment  
✅ **Effect Size Quantification:** Translating statistical coefficients to practical impact  
✅ **Scientific Interpretation:** Biological mechanisms and clinical implications  
✅ **Research Communication:** Clear presentation of complex statistical concepts  
✅ **Critical Analysis:** Identification of limitations and future research directions  

---

## 🔗 Related Projects

**This analysis builds on foundational skills:**
- [Statistical Hypothesis Testing (t-test)](https://github.com/farid-bioinfo/diabetes-bp-analysis) - Two-group comparisons
- Simple Linear Regression - One predictor relationships

**This analysis leads to:**
- Interaction Effects Modelling - When predictors work synergistically
- Mediation Analysis - Understanding causal pathways
- Longitudinal Analysis - Tracking changes over time

---

## 📧 Contact

**GitHub:** [farid-bioinfo](https://github.com/farid-bioinfo)  
**LinkedIn:** [linkedin.com/in/farid-hakimi-32525a45](https://www.linkedin.com/in/farid-hakimi-32525a45)  
**Email:** fh.faridhakimi@gmail.com

---

## 🎓 Academic Connection

This analysis applies statistical methods from **CEMP MSc Biostatistics & Bioinformatics** (Grade: 9.43/10):
- Module 3: Biostatistics & R II (Grade: 9.59/10)
- Topics: Multiple regression, hypothesis testing, model comparison, effect sizes

Demonstrates proficiency in advanced statistical modelling relevant to gut-brain axis research and neurodevelopmental conditions.

---

*Part of ongoing portfolio development in computational biology and gut-brain axis research.*
