# COVID-19 Patient Classification — Machine Learning Project
This work was developed as part of a **university course project** on data analysis and machine learning.  
Although the models and results are simple, the project provided a practical understanding of:
- how to handle imbalanced data,  
- the importance of proper evaluation metrics, and  
- how different classifiers behave on real-world datasets.

## Project Overview
The dataset (`datosCOVID.csv`) includes demographic and clinical information from patients tested for COVID-19.  
The variable `CLASSIFICATION_FINAL` was regrouped into two broader categories to simplify the classification task.

The analysis consisted of the following steps:
1. **Data preprocessing** – handling missing values and grouping target labels.  
2. **Exploratory data analysis** – creation of a correlation matrix to identify relationships between medical features.  
3. **Model training** – using several basic classifiers:
   - `DummyClassifier`  
   - `KNeighborsClassifier`  
   - `DecisionTreeClassifier`  
   - `RandomForestClassifier`  
   - `MLPClassifier`  

4. **Model evaluation** using cross-validation.  
5. **Dataset balancing** using under-sampling to analyze its impact on accuracy and recall.

## Main Findings

- The dataset was **highly imbalanced**, with most patients belonging to the same class.  
- The baseline model achieved around **97% accuracy**, which reflected the imbalance rather than true predictive performance.  
- After applying **under-sampling**, classifiers such as Decision Trees and K-Nearest Neighbors showed **better recall** for minority classes, although overall accuracy decreased.  
- The **correlation matrix** revealed clear relationships between certain variables, such as *ICU* and *intubated*, or *sex* and *pregnancy*.

## Results Summary

| Classifier | Mean Accuracy (CV) | Notes |
|-------------|--------------------|-------|
| DummyClassifier | ~0.97 | Indicates class imbalance |
| KNN (k=3,5,7) | 0.25–0.30 | Low accuracy due to imbalance |
| Decision Tree | ~0.46 (balanced) | Better recall on minority classes |
| Random Forest | ~0.50 | More stable, slower training |
| MLP | Variable | Sensitive to data scaling |
