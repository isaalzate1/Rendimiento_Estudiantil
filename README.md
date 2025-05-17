# Clasificación de Rendimiento Estudiantil
Autor:Isabella Alzate Restrepo

Este proyecto aplica técnicas de aprendizaje supervisado para predecir el rendimiento académico de estudiantes en función de hábitos de estudio, salud mental, estilo de vida y factores socioeconómicos.

### Exploración y Preprocesamiento de Datos

Fuente de datos: student_habits_performance.csv

Transformaciones clave:

- Variables categóricas a dummies

- Estandarización de variables numéricas

- División en conjunto de entrenamiento (80%) y prueba (20%)

### Modelos y Ajuste de Hiperparámetros

Modelo base: LogisticRegression (baseline)

- Optimizaciones:

- Búsqueda aleatoria con RandomizedSearchCV

- Optimización bayesiana con Optuna

### Evaluación de modelos 

- Baseline 
 AUC CV Media:0.9734
 AUC CV Std:0.0076

- Búsqueda Aleatoria
 AUC CV Media:0.9742
 AUC CV Std:0.0074

- Optuna
 AUC CV Media:0.9755
 AUC CV Std:0.0067

### AUC en Conjunto de Prueba

- Baseline: 0.9773

- Búsqueda Aleatoria: 0.9778

- Optuna: 0.9785

### Gráficas Generadas

- Curvas ROC:

Se graficaron las curvas ROC para los tres modelos, mostrando una excelente capacidad de separación entre clases.

- Distribución de Probabilidades Predichas

Histogramas diferenciados por clase real que muestran buena calibración y separación.

- Matrices de Confusión

Se comparan los errores de clasificación entre modelos. El modelo Optuna tiene menos falsos negativos.

- Importancia de Características (Coeficientes)

Gráfico de barras con coeficientes del mejor modelo:

Las variables más influyentes incluyen: study_hours_per_day, mental_health_rating, exercise_frequency, sleep_hours, attendance_percentage.

- Son los principales factores que explican el rendimiento.
- Esto sugiere que el rendimiento no depende solo de factores académicos, sino también del bienestar integral del estudiante.

### Conclusiones

- Los tres modelos ofrecen alto rendimiento, siendo Optuna el más robusto.

- El modelo permite identificar estudiantes en riesgo con alta precisión.

- Las variables asociadas al bienestar (salud mental, sueño, ejercicio) tienen fuerte impacto en el rendimiento.

✅ Este enfoque puede ser una herramienta preventiva para apoyar estudiantes vulnerable mediante intervenciones tempranas.

### Archivos

- student_habits_performance.csv: Base de datos.

- codigo.ipynb: Todo el código y visualizaciones.

- README.md: Este archivo explicativo.



