# Dengue Prediction ML Pipeline

Pipeline completo de *Machine Learning* para el análisis y predicción de casos de dengue utilizando variables climáticas y ambientales. Este proyecto integra técnicas de aprendizaje no supervisado (K-Means) y supervisado (Random Forest) para explorar patrones y generar predicciones robustas.

---

## Descripción del Proyecto

El objetivo principal es predecir el número de casos semanales de dengue en dos ciudades:

* **San Juan (Puerto Rico)**
* **Iquitos (Perú)**

A partir de datos climáticos (temperatura, humedad, precipitación) e índices de vegetación (NDVI), se construyó un pipeline completo que incluye:

* Análisis exploratorio de datos (EDA)
* Preprocesamiento e imputación temporal
* Selección de variables
* Modelado predictivo
* Evaluación interna y externa (DrivenData)

---

## Tecnologías Utilizadas

* Python 
* Pandas & NumPy
* Scikit-learn
* Matplotlib & Seaborn
* Jupyter Notebook

---

## Metodología

### 🔹 1. Análisis Exploratorio (EDA)

* Distribución de casos de dengue por ciudad
* Visualización de variables climáticas
* Análisis de correlaciones

### 🔹 2. Preprocesamiento

* Imputación de valores faltantes mediante interpolación temporal
* Estandarización con StandardScaler
* Selección de 15 variables relevantes

### 🔹 3. Modelos Implementados

#### K-Means (No Supervisado)

* Identificación de patrones climáticos
* Segmentación de datos en clusters

#### Random Forest (Supervisado)

* Modelo principal de predicción
* Configuración:

  * `n_estimators=200`
  * `max_depth=10`
  * `min_samples_leaf=5`

---

## Resultados

| Métrica                | Valor         |
| ---------------------- | ------------- |
| MAE (Cross-Validation) | 23.31 ± 12.19 |
| MAE (DrivenData)       | 26.9207       |

### Hallazgos Clave

* Mejor desempeño en **Iquitos** que en **San Juan**
* Alta variabilidad en brotes epidémicos
* Relación significativa entre temperatura y casos de dengue
* Validación cruzada estándar tiende a ser optimista en series temporales

---

## Cómo Ejecutar

1. Clona el repositorio:

```bash
git clone https://github.com/tu-usuario/dengue-ml-pipeline-kmeans-randomforest.git
```

2. Instala dependencias:

3. Ejecuta el notebook:

```bash
jupyter notebook
```

---

## Limitaciones

* No incluye variables socioeconómicas ni de movilidad
* No modela explícitamente estacionalidad
* No incorpora rezagos temporales (lags)
* Modelo unificado para ambas ciudades

---

## Mejoras Futuras

* Incorporar variables con rezago (2–8 semanas)
* Modelos separados por ciudad
* Uso de modelos de series temporales (SARIMA, Prophet, LSTM)
* Optimización de hiperparámetros
* Validación tipo *walk-forward*

---

## Conclusión

Este proyecto demuestra que es posible predecir casos de dengue con precisión razonable utilizando únicamente variables climáticas. Sin embargo, resalta la importancia de considerar la estructura temporal de los datos y la necesidad de modelos más especializados para mejorar la generalización.

---

## Fuente de Datos

* DrivenData: *DengAI - Predicting Disease Spread*
