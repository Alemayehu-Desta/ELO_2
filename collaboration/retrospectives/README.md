# Final Reflection / Retrospective

This capstone project set out to identify the strongest determinants of Foreign Direct Investment (FDI) inflows in developing economies using a fully reproducible data science workflow. The goal was not only to answer a research question but to build a rigorous, transparent analytical pipeline—from domain research all the way to communication products for policymakers. This reflection summarizes what was achieved, what was learned, and how I grew as an analyst through the process.

---

## Were the Original Project Objectives Achieved?

Overall, **yes**, the objectives were achieved.

### Achievements
- Built a *clean, multi-source panel dataset* integrating World Bank, WGI, and LPI data.
- Conducted *comprehensive Exploratory Data Analysis* (EDA).
- Ran *econometric models* (Pooled OLS) with clustered standard errors.
- Implemented *machine learning models* (Random Forest Regressor).
- Engineered *lagged features* to study FDI persistence.
- Created *visualizations*, including choropleths and bar-chart races.
- Developed a *policy brief* targeting African Union decision-makers.
- Produced a *reproducible GitHub repository* with clear structure and documentation.

Even though some technical tasks—such as fully estimating a Fixed Effects model with clustered SEs—were not successful due to data limitations, the main analytical and policy objectives were fulfilled.

### Challenges
- Fixed-effects models with cluster-robust SEs failed due to multicollinearity and insufficient within-variation.
- Missing institutional data reduced power in some regressions.
- Time constraints limited advanced ML experimentation (XGBoost, SHAP).
- A full production Tableau dashboard was not completed, though a specification was.

Despite these obstacles, the project still delivered coherent, consistent, and actionable insights aligned with the research question.

---

## Most Valuable Learning

The most important lesson was understanding the fundamental difference between:

### **Econometrics (Causal Inference)**  
vs.  
### **🤖 Machine Learning (Prediction)**

**Econometrics** forces explicit modeling assumptions:  
- risk of omitted variable bias  
- careful coefficient interpretation  
- diagnostics and statistical significance  

**Machine learning**, in contrast:  
- ignores functional form assumptions  
- tolerates multicollinearity  
- captures nonlinearities and interactions automatically  
- focuses on predictive accuracy  

Seeing both approaches converge on similar conclusions increased confidence in the results:

> **Infrastructure quality and previous investment matter more than governance metrics.**

This dual-method learning deepened my understanding of how to select the right tool for the right analytical purpose—one of the most valuable outcomes of the project.

### Additional Learning Highlights
- Building a *reproducible repository* is just as important as running models.
- Communication is not decoration—it is part of the analytical process.
- Policymaker-oriented storytelling requires distilling technical results down to what truly drives decisions.

---

## Reflection on the Individual Capstone Experience

Since this project was completed individually, self-assessment focuses on discipline, analytical rigor, and project management.

### What I Did Well
1. **Persisted through difficult technical obstacles**  
   (clustered SEs failures, imperfect data, FE model issues).

2. **Maintained a clear narrative thread**  
   Domain research → Data prep → EDA → OLS → ML → Policy brief.

3. **Communicated findings effectively**  
   Created concise messaging for AU policymakers, including a two-page brief.

4. **Followed reproducibility best practices**  
   Clean folder structures, no modification of original datasets, documented pipeline.

### 🛠 What I Would Improve Next Time
1. **Begin complex econometric modeling earlier**  
   FE issues consumed late-stage time.

2. **Avoid overscoping**  
   I attempted everything: econometrics, ML, dashboards, communication. Prioritization will be stronger in future projects.

3. **Automate more of the cleaning pipeline**  
   Reduce manual steps and improve future replicability.

4. **Deepen ML experimentation**  
   XGBoost, SHAP, and regularization models could have enriched predictive insights.

---

## Conclusion

This project strengthened my analytical identity in three major ways:

### 1. **As a Researcher**  
I learned to form disciplined hypotheses, choose appropriate methods, and interpret results responsibly.

### 2. **As a Data Scientist**  
I built a full end-to-end pipeline that others can replicate—something that distinguishes technical competence from true professionalism.

### 3. **As a Policy Communicator**  
I practiced translating complex statistical results into actionable insights for African Union ministers and investment policy leaders.

The most important takeaway is that impactful data science is not just analysis—it is a *full system* that blends structured inquiry, clean engineering, and persuasive communication. I leave this project with stronger confidence, deeper skills, and a clearer vision of the analyst I want to become.

---

If you want, I can also export this as a PDF or format it as part of your repository’s main README.
