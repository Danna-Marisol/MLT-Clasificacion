# MLT-Clasificacion


Objetivo del proyecto:

Aplicar técnicas de aprendizaje automático tradicional para clasificar a las personas como diabéticas o no diabéticas, mediante la ejecución de un análisis exploratorio de datos (EDA), la selección de características basada en la ganancia de información mutua, la comparación de algoritmos de clasificación utilizando LazyPredict, la elección del modelo con mejor desempeño evaluado a través de métricas como la exactitud (accuracy) o el F1-score, y el registro sistemático de resultados, métricas y artefactos empleando la plataforma MLflow.

=======================================================================

Descripción del dataset:

Dataset: Diabetes Clinical Dataset(100k rows)

Fuente: Kaggle ----> https://www.kaggle.com/datasets/ziya07/diabetes-clinical-dataset100k-rows

Se accede al dataset descomprimiendo un archivo .zip llamado desde la nube

  Acerca del conjunto de datos
  
Conjunto de datos detallados que comprende datos demográficos y de salud de 100,000 personas, destinados a facilitar la investigación relacionada con la diabetes y el modelado predictivo. Este conjunto de datos incluye información sobre el sexo, la edad, la ubicación, la raza, la hipertensión, las enfermedades cardíacas, los antecedentes de tabaquismo, el IMC, el nivel de HbA1c, el nivel de glucosa en sangre y el estado de la diabetes.

=======================================================================

Decisiones tomadas en el modelado:

Se usaron solo las primeras 4 caracteristicas con mayor información mutua para entrenar el modelo:
'hbA1c_level', 'blood_glucose_level', 'age', 'bmi'
No se usó lazypredict para evaluar los modelos de clasificación por que no hay suficiente ram para ejecutarlo.
Se evaluaron solo 3 modelos de clasificación: Logistic Regression, DecisionTreeClassifier y RandomForestClassifier.
Modelo con mejor Accuracy y MAE: RandomForestClassifier 
El código final fue adaptado a la ejecución en github usando deepseek, originalmente fue hecho en google colab y mostrando las métricas en mlflow con ngrok

=======================================================================

Resultados y métricas principales:

accuracy: 0.96795

precision: 0.9129082426127527

mse: 0.03205

recall: 0.6893716970052848

mae: 0.03205

f1_score: 0.7855470056875209







