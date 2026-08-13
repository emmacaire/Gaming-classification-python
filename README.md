# Predictive Classification Engine: Gaming addiction
> **An application of classification methods in public health context with a validated algorithm for predictive analysis and prescriptive practical advices.**

[![Notebook](https://img.shields.io/badge/Python-Notebook-F2C94C?logoColor=black)](https://github.com/emmacaire/Gaming-classification-python/blob/main/notebooks/Gaming_addiction_notebook.ipynb)
[![Kaggle](https://img.shields.io/badge/Data_Source-Kaggle-blue?logo=kaggle)](https://www.kaggle.com/datasets/ajitashwath/gaming-addiction-dataset)
[![Source Data CSV](https://img.shields.io/badge/Data_Source-CSV-green?)](https://github.com/emmacaire/Gaming-classification-python/blob/main/source/gaming_addiction.csv)
<br>

## 📌 Summary
Starting from a relatively small and computationally inexpensive dataset, I created a classification model that diagnoses patients that are addicted to gaming. 
The dataset contains only 250 rows but offers over 40 different variables, most of which requiring pre-processing in Python. The nature of the dataset also suggested that LOOCV (Leave One Out Cross Validation) would be the best model evaluation technique, leaving only the minimum number of rows out for testing. 

Some features proved to be excellent variables to train the models, however the low number of positive instances in the small test dataset proved to be the main challenge in the end, significantly impacting on the confusion matrix metrics. 
Given the purpose of the dataset, emphasis was given into detecting all positive instances, maximizing recall and accepting an inferior performance in precision, and Gradient Boosting was the preferred classifier, while the variables that better contributed to an accurate classification were "Screen time total hours", "Sleep hours" and "Missed deadlines".

The key takeaways of the project were:
  1. in this specific project, changing the threshold to classify positive values from 0.5 to 0.7 did not create more false negatives and affect recall, on the contrary it improved classification even in the test set.
  2. to avoid class imbalance on the test set, I should have used a stratified shuffle split in the initial train/test holdout, or employ over-sampling techniques like SMOTE.
<br>

## 📊 Key Deliverables & Artifacts
| Deliverable | Description | Link |
| :--- | :--- | :---: |
| 📄&nbsp;**Notebook** | Python code including EDA, data preparation, model training and testing, discussion and final model selection | [Open&nbsp;Notebook&nbsp;↗](./notebooks/Gaming_addiction_notebook.ipynb) |
| 📄&nbsp;**Data&nbsp;Dictionary** | A synthetic dictionary explaining the source data and further terms used | [View&nbsp;Dictionary&nbsp;↗](./DATA_DICTIONARY.md) |
<br>

## 🛠️ Tech Stack & Methodology
* **Language:** 
Python (Pandas, Scikit-Learn, Matplotlib, Seaborn, NumPy, SciPy)
* **Concepts:** 
Outlier detection, handling missing values (one-hot encoding, average target encoding), feature selection (RFE), model training (logistic regression, Naive Bayes, KNN, Random Forest, Extra Trees, Adaboost, Gradient Boosting), confusion matrix evaluation and metrics (balanced accuracy, F1-score, precision, recall).
