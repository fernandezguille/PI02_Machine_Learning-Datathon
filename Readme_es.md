<h1 align=center> PROYECTO INDIVIDUAL 02 </h1>
<h2 align=center> Machine Learning en Datasets sobre hospitalizaciones</h2>

<br>

¡Hola! Mi nombre es *Guillermo Fernández* y éste mi segundo proyecto individual, que forma parte de la formación práctica del bootcamp de Data Science de la academia Henry. 

<hr>

## Objetivo
Cargar un dataset sobre hospitalizaciones. Mediante la exploración y el entrenamiento de un Modelo de Machine Learning, se debe predecir si los pacientes pasarán más de 8 días hospitalizados, entrenandolo con la parte del dataset que tiene los resultados, y usando eso como referencia para la otra parte que no lo tiene.

[Consigna completa del PI](https://github.com/soyHenry/Datathon)

### Contexto
Es muy importante para el funcionamiento del hospital/clínica, conocer si un paciente tendrá una internación prolongada. Para este trabajo, se utilizó un dataset que estaba fraccionado, y una parte no tenía el tiempo de internación.

<p align="center"> <img alt="ML" src="https://user-images.githubusercontent.com/110403753/208594890-3a68320a-d9ee-4f9b-8f96-cdf8048313dc.png" height=200px> <img src="https://thehill.com/wp-content/uploads/sites/2/2021/11/ca_coronavirusus_013020istock_25.jpg?strip=1" height=200px></p>

### Tecnologías utilizadas
* [Python](https://docs.python.org/3/)
    * [Pandas](https://pandas.pydata.org/)
    * [Numpy](https://numpy.org)
    * [sklearn](https://scikit-learn.org/stable/index.html)
    * [scipy](https://scipy.org)
    * [joblib](https://joblib.readthedocs.io/en/latest/)
    * [Seaborn](https://seaborn.pydata.org)
    * [Matplotlib](https://matplotlib.org)

<hr>

## Plan de trabajo:
1. EDA (Exploratory data analysis)
2. Preprocesamiento de datos
3. Análisis de correlación
4. Tratamiento de features (eliminado y recategorizacion)
5. Pipeline
6. Creación del modelo
7. Predicción

### Archivos del repositorio
- [**Datasets**:](./Datasets/) En esta carpeta se encuentran los archivos raw utilizados para realizar el proyecto, y también el archivo que se creó con los resultados de la predicción. El nombre de éste coincide con el usuario de GitHub.  
- [**Mejor_pipeline**:](./Mejor_pipeline.pkl) En este archivo se guarda el pipeline con mejor accuracy, para evitar correr nuevamente todos los entrenamientos.
- [**Modelado**:](./Modelado.ipynb) Notebook donde se realiza el trabajo.


## EDA <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width=40px height=40px/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg" width=40px height=40px/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width=40px height=40px/>
Para el primer paso, se realiza el EDA. Se exploraron los datasets, revisando tipos de datos y faltantes. En base a este análisis, se obtienen algunas conclusiones iniciales.

## Preprocesamiento de datos
Debido a que la feature relevante es una variable categórica, no sirve el análisis de correlación numérica, por lo que se utiliza análisis estadístico.

## Análisis de correlación
Con la ayuda de las librerías de Python, se obtiene el P valor de las variables categóricas, para evaluar la correlación.

## Tratamiento de features
Se eliminan las features irrelevantes, y se realiza la recategorización mediante OrdinalEncoder y OneHotEncoder.

## Pipeline
Se utiliza Pipeline para entrenar múltiples modelos, y poder evaluar cuál es el que otorga mejor precisión. Como es un proceso que demora mucho tiempo, el resultado lo guardamos en un archivo para luego importarlo.

## Modelo
Se selecciona el modelo de árbol de desición, de acuerdo al resultado del Pipeline. Utilizando Cross Validate y un bucle, se obtiene la profundidad óptima del árbol. Se entrena el modelo con train_test_split. Luego, comparamos los resultados obtenidos con el evaluado en el Pipeline, y nos quedamos con el más equilibrado.  
<p align="center"> <img src="https://static.vecteezy.com/system/resources/previews/001/234/042/original/decision-tree-design-vector.jpg" width="200px"> </p>

## Predicción
Con el modelo entrenado, se realiza la predicción del feature, y se lo exporta a un archivo para su posterior evaluación.

<hr>

## Conclusión
Luego de realizar varias pruebas, con diferentes métodos (dummies, OHE, LE, ORE), este modelo fue el que mejor accuracy y recall tuvo, sin tener overfitting.  
Muchas de las columnas tenían una relación con la estadía, como se vió con el P_valor, pero el resultado solo mejora un poco a comparación de realizar el árbol con sólo 3 features. Esto se observa en el gráfico que mide el peso de las mismas.
Al recibir el feedback del modelo, los valores logrados de las métricas son:
+ Accuracy: 0.7629
+ Recall:   0.8102

Les dejo mi contacto:  
<a href="https://www.linkedin.com/in/fernandezguillermo"><img alt="Linkedin" title="Connect with me" src="https://img.shields.io/badge/Linkedin-0077B5?style=flat&logo=linkedin&logoColor=white"></a>  

¡Muchas gracias por llegar hasta aquí!