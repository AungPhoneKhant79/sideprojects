# Titanic Survival Prediction – Logistic Regression

## Overview
This project predicts passenger survival on the Titanic using a logistic regression model. The dataset includes passenger demographics, travel class, family aboard, and port of embarkation.

## Features & Findings

- **Sex**  
  - Female (Sex_1.0): +1.015 → significantly increases survival odds.  
  - Male (Sex_0.0): -0.898 → significantly decreases survival odds.  

- **Passenger Class (Pclass)**  
  - First Class (Pclass_1.0): +0.833 → higher chance of survival.  
  - Third Class (Pclass_3.0): -0.797 → lower chance of survival.  
  - Second Class (Pclass_2.0): +0.081 → minimal impact.  

- **Age**  
  - Coefficient -0.416 → older passengers have lower odds of survival; each year increases log-odds of death.  

- **Siblings/Spouses Aboard (SibSp)**  
  - Coefficient -0.170 → more siblings/spouses reduces individual survival odds.  

- **Parents/Children Aboard (Parch)**  
  - Coefficient -0.022 → slight negative effect; more family slightly lowers survival likelihood.  

- **Port of Embarkation (Embarked)**  
  - Coefficients near zero → minimal influence on survival probability.  

## Interpretation of Coefficients
- Positive → increases probability of survival.  
- Negative → decreases probability of survival.  
- Larger absolute values → stronger influence on survival.

## Key Insights
- Most important survival factors: being female and traveling first class.  
- Older age, traveling third class, and having more family aboard decrease survival odds.  
- Logistic regression allows ranking feature importance and understanding how each feature shifts survival probability.
