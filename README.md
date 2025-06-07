
# Ethical Machine Learning for Crime Recidivism Prediction

This project applies machine learning techniques to predict whether individuals are likely to reoffend within two years of release, based on the COMPAS recidivism dataset. The focus is not only on prediction accuracy but also on fairness, interpretability, and ethical AI principles.

## 📌 Project Overview

- **Goal**: Predict two-year recidivism and analyze model fairness across racial and gender groups.
- **Dataset**: [COMPAS Recidivism Subset](https://raw.githubusercontent.com/suneman/socialdata2022/main/files/recidivism_dataset_sub.csv)
- **Model Used**: Random Forest Classifier (with Decision Tree baseline)
- **Tools**: Python, scikit-learn, pandas, matplotlib, Bokeh, imbalanced-learn, dtreeviz

## 🧠 Key Features

- Preprocessing includes filtering arrest-screening time range and OneHotEncoding of categorical variables.
- Age is grouped into categories for improved interpretability.
- Data split into train/test sets using a stratified 70/30 split.
- Hyperparameter tuning via RandomizedSearchCV to improve model generalization.
- Evaluation metrics include **Accuracy**, **Precision**, **Recall**, and **F1 Score**.
- Visualization of individual decision trees using `dtreeviz`.
- Fairness evaluation using ROC-based threshold selection across racial groups (Equal Odds).
- Undersampling used to balance subgroup data distributions.

## ⚖️ Ethical Considerations

- Identified and addressed racial and gender bias in model predictions.
- Highlighted how accuracy alone can be misleading in socially sensitive predictions.
- Used Equal Odds method to adjust thresholds and improve fairness for African-American and Caucasian groups.

## ✅ Results

| Model         | Accuracy | Precision | Recall | F1 Score |
|---------------|----------|-----------|--------|----------|
| Decision Tree | ~59%     | —         | —      | ~0.55    |
| Random Forest | **68.8%** | **58.3%**  | **68.5%** | **62.9%**  |

## 📂 File Structure

- `MainNotebook.ipynb`: Full Jupyter notebook with data processing, model training, evaluation, and fairness analysis.
- `README.md`: This file.

## 💬 Key Takeaways

- Fair and interpretable AI can be built using widely available tools.
- Ethical awareness and subgroup performance analysis are essential in justice-related prediction tasks.
- F1 Score is a more appropriate metric in cases of asymmetric error costs.

---

**Author**: *Pranjal Garg*, *Tala* , *Ananthu*   
**Date**: March 2022  
**License**: MIT 

