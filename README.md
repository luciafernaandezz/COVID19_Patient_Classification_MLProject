# COVID-19 Patient Classification_MLProject
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

## Results
| Classifier | Mean Accuracy (CV) | Notes |
|-------------|--------------------|-------|
| DummyClassifier | ~0.97 | Indicates class imbalance |
| KNN (k=3,5,7) | 0.25–0.30 | Low accuracy due to imbalance |
| Decision Tree | ~0.46 (balanced) | Better recall on minority classes |
| Random Forest | ~0.50 | More stable, slower training |
| MLP | Variable | Sensitive to data scaling |
