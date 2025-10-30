# Micro_Internship_at_TATA-IQ
My complete 4-task project for the Tata iQ Data Science Micro-Internship, focusing on credit delinquency analysis, predictive modeling, and strategic AI system design.

# Tata iQ Data Science Micro-Internship: Credit Delinquency Strategy

This repository contains all my work for the 4-task Tata iQ Data Science Micro-Internship. The project simulates a real-world consulting engagement, progressing from raw data analysis to a final, high-level AI system design for a "Head of Collections" at a client company named Geldium.

##  Project Strategy & Key Finding

The most critical insight from this project was not a high-accuracy model but a realistic business conclusion: **the provided dataset was too small and imbalanced to support a reliable predictive AI.**

My analysis proved that all models (Logistic Regression, Random Forest, Decision Tree) performed at or below a 50/50 random chance (AUC < 0.5).

Therefore, my final recommendation was a practical, hybrid approach:
1.  **Act Now:** Implement a simple, transparent **rules-based system** based on the reliable findings from the Exploratory Data Analysis (EDA).
2.  **Learn & Adapt:** Use an "agentic AI" system to automate these rules and implement a **continuous learning loop** that tracks the outcome of every action.
3.  **Build for the Future:** Use the rich, labeled data gathered by this new system to *eventually* build the powerful, high-accuracy predictive model that was not possible at the start.

##  Project Structure

The project is divided into four main tasks, each in its own folder.

###  Task_1_EDA
* **Goal:** Analyze the `Delinquency_Dataset.xlsx` to find key risk factors.
* **Work:** Performed data cleaning, imputation for missing values, and visualization to find correlations.
* **Key Findings:** Identified `Missed_Payments`, `Credit_Utilization`, and `Credit_Score` as the strongest, most reliable predictors of delinquency.
* **Deliverable:** `EDA_Summary_Report.docx`

###  Task_2_Model_Training
* **Goal:** Build and tune a predictive model to classify delinquent customers.
* **Work:** Developed a `scikit-learn` pipeline including `SimpleImputer`, `StandardScaler`, and `OneHotEncoder`.
* **Challenge:** Rigorous tuning with `GridSearchCV` on models like `DecisionTreeClassifier` and `RandomForestClassifier` (using `SMOTE` to handle imbalance) proved that the data lacked sufficient predictive signal.
* **Deliverable:** `Model_Plan.docx`, which justifies the selection of a simple, transparent **Decision Tree** as the only viable (though weak) model framework.

###  Task_3_Bussiness_Report
* **Goal:** Translate the technical findings into a strategic business report for a non-technical stakeholder (the "Head of Collections").
* **Work:** Wrote a 2-page report that pivoted from the failed AI model to a practical, rules-based strategy based on the **Task 1 EDA findings**.
* **Strategy:** Proposed a **SMART** recommendation for a proactive outreach campaign based on simple, explainable rules (e.g., `Credit_Utilization > 80%`).
* **Deliverable:** `Business_Summary_Report.docx`

###  Task_4_PPT
* **Goal:** Design a high-level framework for an **agentic AI** system to automate the strategy from Task 3.
* **Work:** Created a 5-slide executive presentation outlining a system that uses the rules-based logic as its starting point and implements a **learning loop** to improve over time.
* **Strategy:** The system is designed to be fair, explainable, and compliant, with a "human-in-the-loop" for all critical decisions.
* **Deliverable:** `AI-Powered Collections Strategy.pptx`

##  Tools & Technologies
* **Python**
* **Pandas:** For data manipulation and analysis.
* **Scikit-learn:** For preprocessing (`Pipeline`, `ColumnTransformer`) and modeling (`DecisionTreeClassifier`, `GridSearchCV`).
* **Imbalanced-learn:** For oversampling (`SMOTE`).
* **Jupyter Notebooks:** For all analysis and modeling.
* **Microsoft Word & PowerPoint:** For creating the final business deliverables.
