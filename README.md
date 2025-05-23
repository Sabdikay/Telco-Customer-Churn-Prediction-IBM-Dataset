<p align="center"> <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter"> <img src="https://img.shields.io/badge/Python-3.8-blue?logo=python"> <img src="https://img.shields.io/badge/Machine%20Learning-RandomForest-green?logo=scikitlearn"> <img src="https://img.shields.io/badge/Data%20Analysis-Pandas-blue?logo=pandas"> <img src="https://img.shields.io/badge/Visualization-Plotly-green?logo=plotly"> </p> <h1 align="center"> 📈 Telco Customer Churn Analysis & Predictive Model 📉 </h1> <p align="center"> 🚀 Data-driven EDA + ML project to predict customer churn & reasons using IBM Telco dataset.<br> 🎯 Powered by Random Forest classifier with real-time customer simulation & actionable insights.<br> 💼 Built in Jupyter Notebook using Python, pandas, seaborn, plotly, sklearn and more. </p>
# Telco Customer Churn Analysis & Predictive Model

Welcome to the **Telco Customer Churn Analysis & Predictive Model** project!
This Jupyter Notebook project explores customer churn data from a fictional telecommunications company serving 7,043 customers in California during Q3. We not only perform extensive exploratory data analysis (EDA) but also build and evaluate predictive models to forecast both customer churn and churn reasons.

---

## 📚 Table of Contents

- [Introduction](#introduction)
- [Project Enhancements](#project-Enchancements)
- [Data Overview](#data-overview)
- [Exploratory Analysis](#exploratory-analysis)
- [Predictive Modeling](#predictive-modeling)
- [Conclusions](#conclusions)
- [Further Research](#further-research)
- [Usage](#usage)
- [Data Sources](#data-sources)
- [Credits](#credits)
- [License](#license)

---

## Introduction

This project analyzes customer churn for a telco company that provided home phone and Internet services. Using a dataset of 7,043 customers and 33 variables, we delve into key questions:

- What are the main reasons for subscription cancellations?
- When do most churn events occur?
- How do billing factors and contract types influence churn?
- Can we predict churn and the specific churn reason with high accuracy?

The analysis is conducted in a Jupyter Notebook using Python libraries such as **pandas, NumPy, matplotlib, seaborn, plotly, scipy,** and **statsmodels**.

---

## 🚀 Project Enhancements

This project has undergone several critical updates and refinements:

* ✅ **Improved Predictive Models:**

  * Initially, models showed **1.000 training accuracy** due to unscaled numerical data and deep tree algorithms.
  * This issue was corrected by introducing **standard scaling**, tuning model depth, and enhancing the preprocessing pipeline, resulting in more realistic and reliable model accuracy.

* ✅ **Smarter Churn Reason Prediction Logic:**

  * The logic was **redefined to predict churn reason only for customers who are predicted to churn**, rather than all customers.
  * This greatly improved precision and reduced logical inconsistencies.

* ✅ **Class Imbalance Handling & Cross-Validation:**

  * Class imbalances were identified and mitigated.
  * Cross-validation techniques were added to ensure model robustness.

* ✅ **Dynamic User Simulation Feature:**

  * Developed a **custom function** that generates **any number of random customers**.
  * For each simulated customer, the system:

    * Predicts churn probability (with percentage).
    * Outputs prediction result.
    * Shows customer’s key features (e.g., Monthly Charges, Contract Type).
    * If churn is predicted, also returns **predicted churn reason**.

---

## Data Overview

The dataset, **Telco_customer_churn.xlsx**, includes detailed customer information such as demographics, service usage, billing details, and churn indicators (e.g., Churn Label, Churn Value, Churn Score, CLTV, and Churn Reason). Data cleaning steps involved dropping irrelevant columns, converting data types, and handling missing values to prepare for analysis.

---

## Exploratory Analysis

Key EDA steps include:
- Visualizing missing data with heatmaps.
- Examining distributions via histograms and scatter plots.
- Computing correlation matrices to identify relationships among variables (e.g., Tenure Months, Monthly Charges, Total Charges, and CLTV).
- Performing chi-square tests and ANOVA to assess the significance of relationships between churn factors.

These analyses revealed:
- Most churn occurs in the first month.
- Month-to-month contracts have the highest churn rate.
- Strong correlations exist between tenure, total charges, and CLTV, with monthly charges also playing a role.

---

## Predictive Modeling

### Model Development

We extended our analysis by developing predictive models that:
1. **Predict whether a customer will churn**  
2. **Predict the churn reason**

Using techniques like label encoding and feature scaling, we evaluated three models:
- **Decision Tree**
- **Naive Bayes**
- **Random Forest**

### Results

- **Random Forest** emerged as the best model, achieving the highest test accuracy in both churn classification and churn reason prediction.
- Confusion matrices and performance metrics demonstrate the model’s robustness and potential for real-world application.

### Sample Predictions

We also tested the model on simulated new customer data, generating predictions for churn and corresponding churn reasons (e.g., *Service Quality*, *Price*, *Competitor*, *Other*).

### Simulation Example

Using the **dynamic customer generator**, we can simulate multiple new customers and predict:

* Churn probability (%)
* Churn or not
* Monthly Charges
* Contract Type
* Churn Reason (if churn is predicted)

---

## Conclusions

- **Churn Drivers:** Major reasons for churn include poor support, competitive offers, low download speeds, and insufficient data.
- **Timing:** The majority of churn occurs within the first month of service.
- **Billing Impact:** While monthly charges show a statistically significant relationship with subscription duration, they explain only a modest portion of the variance.
- **Contract Influence:** Month-to-month contracts experience the highest churn, whereas one- and two-year contracts demonstrate stability.
- **Predictive Success:** Incorporating a predictive model using Random Forest transforms the analysis into a practical decision support tool—empowering telecom companies to proactively address churn by tailoring interventions based on predicted churn reasons.

---

## Further Research

Future directions include:
1. **Advanced Predictive Modeling:**  
   - Enhance the model with additional features (e.g., customer service interactions, feedback) and integrate it into a real-time decision-support system.
2. **Customer Segmentation:**  
   - Use churn predictions to cluster customers and develop personalized retention strategies.
3. **Continuous Model Improvement:**  
   - Regularly update the model with new data to capture evolving customer behavior.
4. **Temporal and Spatial Analysis:**  
   - Extend the analysis to track churn trends over time and explore geographic patterns in customer behavior.

---

## Usage

### Prerequisites
- Python 3.8+
- Jupyter Notebook

### Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/YourUsername/Telco-Customer-Churn-Project.git
   cd Telco-Customer-Churn-Project
   ```

2. **Install Dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scipy statsmodels scikit-learn
   ```

3. **Launch the Notebook:**
   ```bash
   jupyter notebook
   ```
4. **Open and Run `customer-churn-IBM-dataset(Predictive Model).ipynb`**

---

## Data Sources

- **Telco_customer_churn.xlsx** provided by IBM  
  Detailed dataset available at: [IBM Telco Customer Churn](https://community.ibm.com/accelerators/?context=analytics&query=telco%20churn&type=Data&product=Cognos%20Analytics)

---

## Credits

**Developed by:**  
**Alnur Nurumov**

---

## License

This project is licensed under the [MIT License](LICENSE).

---

*Thank you for exploring the Telco Customer Churn Analysis & Predictive Model project!
Empower your decisions with data-driven churn predictions! 🚀📊✨*
