# Insurance Fraud Detection Analysis: Global Insure Case Study

## Table of Contents
* [General Info](#general-information)
* [Problem Statement](#problem-statement)
* [Key Findings](#key-findings)
* [Recommendations](#recommendations)
* [Technologies Used](#technologies-used)
* [Contact](#contact)

## General Information
This project aims to improve Global Insure's fraud detection process using data-driven insights to classify claims as fraudulent or legitimate early in the approval process. By developing predictive models based on historical claim data, the company can minimize financial losses while optimizing the overall claims handling process.

The key challenge for Global Insure is **reducing fraudulent claim payouts** while maintaining customer satisfaction. The company must balance two critical aspects:
1. **Identifying fraudulent claims** to prevent financial losses before payments are made
2. **Processing legitimate claims efficiently** to ensure positive customer experiences without unnecessary delays

By understanding the **patterns and indicators of fraudulent behavior**, Global Insure can transform its currently time-consuming manual inspection process into a more efficient, data-driven approach.

The project utilizes a **dataset of 1,000 insurance claims with 40 features** that includes:
- Policy information (deductibles, annual premiums, coverage limits)
- Customer demographics (age, gender, education, occupation)
- Incident details (time, location, witnesses, vehicles involved)
- Claim information (total amounts, injury/property/vehicle components)
- Vehicle information (make, model, year)

Through **exploratory data analysis (EDA)** and **machine learning**, the dataset was analyzed to develop predictive models that can classify incoming claims with high accuracy.

## Problem Statement
Global Insure processes thousands of claims annually, with a significant percentage proving to be fraudulent, resulting in considerable financial losses. The company's current identification process relies on time-consuming manual inspections, with fraudulent claims often detected after payments have already been made. This inefficient system not only impacts the company's bottom line but also subjects legitimate claims to unnecessary scrutiny, creating delays for honest customers.

The business objective is to build a predictive model that quickly classifies incoming claims as fraudulent or legitimate using historical data, customer profiles, claim amounts, and claim types, enabling early fraud detection before approval and payment.

## Key Findings
1. **Fraud Patterns & Indicators**
   - 24.75% overall fraud rate across analyzed claims
   - Male claimants show higher fraud rates than females
   - Education level significantly impacts fraud likelihood (Masters: 45% vs. High School: 10-15%)
   - Vehicle theft claims show very low fraud rates compared to other incident types
   - Certain vehicle makes (Saab, Toyota, BMW) associated with higher fraud rates

2. **Claim Characteristics**
   - Higher deductibles ($2,000 vs. $1,000) associated with more fraud
   - Claims approaching policy coverage limits more likely fraudulent
   - Fewer witnesses correlate with higher fraud likelihood
   - Later incident hours associated with more suspicious claims
   - Claims filed within 30 days of policy initiation show significantly higher fraud rates

3. **Model Performance**
   - Random Forest model achieved 79% accuracy on validation data
   - Logistic Regression model achieved 77% accuracy on validation data
   - Both models showed good sensitivity (72% and 69% respectively)
   - Precision challenges identified (55% and 53%), indicating refinement needs
   - Strong discriminatory power (ROC AUC: 0.89)

4. **Feature Importance**
   - Claim-to-coverage ratio emerged as strongest predictor
   - Policy timing features highly significant
   - Demographic risk factors offer strong signals
   - Witness patterns provide reliable fraud indicators
   - Vehicle characteristics offer meaningful predictive value

## Recommendations
1. **Implementation Strategy**
   - Implement tiered risk classification (low/medium/high) rather than binary decisions
   - Use models as decision support tools rather than for automatic rejection
   - Establish feedback mechanism to continuously improve model performance
   - Create specialized protocols for high-risk patterns

2. **Process Improvements**
   - Enhance verification for claims filed shortly after policy initiation
   - Apply risk-based verification protocols based on demographic and geographic factors
   - Strengthen witness documentation requirements for high-value claims
   - Incorporate vehicle characteristics into risk assessment procedures

3. **Model Refinements**
   - Implement integrated approach where hyperparameter tuning precedes feature selection
   - Explore more sophisticated resampling methods (SMOTE, ADASYN)
   - Develop ensemble models combining multiple algorithms
   - Introduce stronger regularization techniques to address overfitting

4. **Business Impact**
   - Early fraud detection before payment will reduce financial losses
   - More efficient resource allocation for investigations
   - Streamlined processing for legitimate claims
   - Improved customer experience for honest policyholders
   - Estimated 15-20% reduction in fraud losses

## Technologies Used
- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Statsmodels
- Imbalanced-learn

## Contact
Created by [@tuyettu1712](https://github.com/tuyettu1712) - feel free to contact me!
