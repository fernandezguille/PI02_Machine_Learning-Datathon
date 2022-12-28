<h1 align=center> INDIVIDUAL PROJECT 02 </h1>
<h2 align=center> Machine Learning on hospitalizations Datasets</h2>

<br>

¡Hi! My name is *Guillermo Fernández* and this is my second individual project, which is part of the training for the Henry Data Science bootcamp.
(Para la versión en español, revisar el readme_es)

<hr>

## Objetive
Load a dataset on hospitalizations. By exploring and training a Machine Learning Model, it is needed to predict if patients will spend more than 8 days in hospital, training it with the part of the dataset that has the results, and using that as a reference for the other part that doesn't. 

[Project description (in Spanish)](https://github.com/soyHenry/Datathon)

### Context
To know if a patient will have a prolonged stay is very important for the operation of the hospital/clinic. For this work, a dataset that was divided was used, and one part did not have the hospitalization time.

<p align="center"> <img alt="ML" src="https://user-images.githubusercontent.com/110403753/208594890-3a68320a-d9ee-4f9b-8f96-cdf8048313dc.png" height=200px> <img src="https://thehill.com/wp-content/uploads/sites/2/2021/11/ca_coronavirusus_013020istock_25.jpg?strip=1" height=200px></p>

### Tech stack
* [Python](https://docs.python.org/3/)
    * [Pandas](https://pandas.pydata.org/)
    * [Numpy](https://numpy.org)
    * [sklearn](https://scikit-learn.org/stable/index.html)
    * [scipy](https://scipy.org)
    * [joblib](https://joblib.readthedocs.io/en/latest/)
    * [Seaborn](https://seaborn.pydata.org)
    * [Matplotlib](https://matplotlib.org)

<hr>

## Workplan:
1. EDA (Exploratory data analysis)
2. Data preprocessing
3. Correlation analysis
4. Features treatment
5. Pipeline
6. Model creation
7. Prediction

### Repository archives
- [**Datasets**:](./Datasets/) Inside this folder are the raw files used to carry out the project, and also the file that was created with the results of the prediction. The name of this one matches the GitHub user.
- [**Mejor_pipeline**:](./Mejor_pipeline.pkl) The pipeline with the best accuracy is saved in this file, to avoid running all the training sessions again.
- [**Modelado**:](./Modelado.ipynb) Notebook where the work is done.


## EDA <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width=40px height=40px/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg" width=40px height=40px/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width=40px height=40px/>
For the first step, the EDA is performed. The datasets were explored, reviewing data types and missing data. Based on this analysis, some initial conclusions are drawn.

## Data preprocessing
Because the relevant feature is a categorical variable, the numerical correlation analysis is useless, so statistical analysis is used.

## Correlation analysis
With Python libraries, the P value of the categorical variables is obtained, to evaluate the correlation.

## Features treatment
Irrelevant features are removed, and recategorization is performed using OrdinalEncoder and OneHotEncoder.

## Pipeline
Pipeline is used to train multiple models, and to be able to evaluate which one provides the best precision. As it is a process that takes a long time, we save the result in a file to import it later.

## Model creation
The decision tree model is selected, according to the Pipeline result. Using Cross Validate and a loop, the optimal depth of the tree is obtained. The model is trained with train_test_split. Then, we compare the results obtained with the one evaluated in the Pipeline, and we keep the most balanced.
<p align="center"> <img src="https://static.vecteezy.com/system/resources/previews/001/234/042/original/decision-tree-design-vector.jpg" width="200px"> </p>

## Prediction
With the model trained, the prediction of the feature is made, and it is exported to a file for further evaluation.

<hr>

## Conclusion
After carrying out several tests, with different methods (dummies, OHE, LE, ORE), this model was the one with the best accuracy and recall, without having overfitting.
Many of the columns had a relationship with the stay, as seen with the P_value, but the result only improves a little compared to making the tree with only 3 features. This is observed in the graph that measures their weight.
Upon receiving the feedback from the model, the achieved values of the metrics are:
+ Accuracy: 0.7629
+ Recall:   0.8102

Here is my contact info:  
<a href="https://www.linkedin.com/in/fernandezguillermo"><img alt="Linkedin" title="Connect with me" src="https://img.shields.io/badge/Linkedin-0077B5?style=flat&logo=linkedin&logoColor=white"></a>  

Thank you very much for reading all!