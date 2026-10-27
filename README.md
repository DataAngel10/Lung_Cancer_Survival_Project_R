# 🫁 Lung Cancer Survival Analysis

A biostatistical analysis evaluating clinical predictors of survival in advanced lung cancer patients (n=228) using R dataset:`survival::lung`.

## 🛠️ Tools & Methods
- **Language:** R (`survival`, `survminer`, `tidyverse`, `mice`, `flextable`, `ggthemes`)
- **Methods:** Kaplan-Meier curves, Log-Rank test, Cox Proportional Hazards regression, Model selection (BIC, ANOVA, Concordance Index),
Schoenfeld residual testing.

---

## 🎯 Research Questions & Results

**1. What is the median survival time for men vs. women at 6 months?**
- **6-Month Survival:** Women 84.2% | Men 64.4%
- **Median Survival:** Women 14.2 months | Men 9.0 months

**2. Is the difference statistically significant?**
- **Yes:** Log-Rank test p = 0.00013$ (p < 0.001), rejecting null hypothesis.

**3. Which factors are independent predictors of survival (HR)?**
- **Female Sex:** HR = 0.56 (p < 0.001) $\rightarrow$ **44% lower risk of death**
- **ECOG Status 2:** HR = 3.81 (p < 0.001) $\rightarrow$ **281% higher risk of death**
- **Non-significant:** Age, Karnofsky scores, and Weight Loss (p > 0.05).
- **Model Fit:** Model 3 (Sex + ECOG) is optimal (C-index = 0.645) and meets proportional hazards assumptions (p > 0.05).

---

## 📝 Conclusion
Patient survival is mainly driven by sex and physical status (ECOG) rather than age or weight loss. The final model is statistically solid, passes the proportional hazards test, and clearly shows the survival advantage for women.
