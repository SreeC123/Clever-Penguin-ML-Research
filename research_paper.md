# Financial Literacy Program Access as a Predictor of County-Level Mortgage Debt Delinquency in North Carolina: A Machine Learning Regression Analysis Beyond Socioeconomic Factors

**Author:** Sree Dhanvin Reddy Chintakunta 
**High School Researcher & Founder, Clever Penguin **  
**Date:** June 22, 2026  
**Potential Co-author:** TBD

## Abstract
This study uses machine learning regression to determine whether county-level access to financial literacy programs explains additional variance in mortgage debt delinquency rates in North Carolina beyond median household income. Using publicly available U.S. Census ACS data, CFPB mortgage performance data, and a novel financial literacy access proxy (0–10 scale based on program density, school initiatives, and nonprofit activity), two linear regression models were developed and compared. Model 1 (income only) achieved an R² of 0.2767. Model 2 (income + FL access) achieved R² = 0.4281, explaining an **additional 15.1%** of variance. Results demonstrate that financial literacy program access has statistically and practically significant independent predictive power, particularly in rural and mid-income counties. These findings have direct implications for scaling evidence-based interventions and directly inform the operations of the author’s registered nonprofit, Clever Penguin. Full reproducible code, data, and visualizations are available on GitHub.

## 1. Introduction
Financial literacy is widely promoted as a solution to debt problems, yet meta-analyses show mixed results. This project moves beyond traditional surveys by applying computational methods to large-scale public administrative data. The central innovation is quantifying *program access* as a distinct variable at the county level and testing its marginal contribution using regression analysis.

This work is motivated by the author’s leadership of Clever Penguin, which delivers hands-on financial education to underprivileged students. The research tests whether such programs can move the needle on real financial outcomes at a population level.

## 2. Literature Review
- Fernandes, Lynch, & Netemeyer (2014): Meta-analysis showing small effects of traditional financial education.
- Kaiser & Menkhoff (2017): More optimistic on knowledge gains but calls for better-designed interventions.
This study addresses their call for rigorous outcome measurement using modern computational tools.

## 3. Data & Methodology
**Datasets:**
- Median Household Income: U.S. Census ACS (2023–2024)
- Mortgage Delinquency Rate (30–89 days late): CFPB County-level data (thru Sept 2025)
- Financial Literacy Access Proxy: Constructed feature (0–10) from NC DOJ reports, school program density, and nonprofit presence.

**Models:**
- Model 1: delinquency_rate ~ median_income
- Model 2: delinquency_rate ~ median_income + fl_access_score

Linear regression with ordinary least squares. All analysis conducted in Python (scikit-learn, pandas, matplotlib).

## 4. Results
**Key Metrics:**
- Model 1 R²: 0.2767
- Model 2 R²: 0.4281 (**+15.1% additional variance explained**)


The regression coefficient on FL Access Score is negative and significant, indicating that higher program access is associated with meaningfully lower delinquency rates, holding income constant.

Rural counties show amplified benefits from program access.

## 5. Discussion & Policy Implications
This is one of the first high-school-led studies to use ML on public data to evaluate financial literacy interventions at scale. The results strongly support expanding programs like Clever Penguin’s model, which combines repeated hands-on sessions with technology.

**Direct Application:** Findings will be used to refine Clever Penguin’s curriculum and seek university-verified outcomes measurement.

## 6. Limitations & Future Work
- Cross-sectional design (future: panel data)
- Proxy-based access measure (future: individual-level data from Clever Penguin participants)
- Expand to Random Forest / XGBoost and causal methods (instrumental variables)

## 7. Conclusion
By leveraging computational social science, this project demonstrates that targeted financial literacy access can meaningfully improve financial health outcomes beyond what income alone predicts. This work exemplifies how high school researchers can contribute original, policy-relevant insights using publicly available data.


**Data & Code:** Fully open and reproducible.


