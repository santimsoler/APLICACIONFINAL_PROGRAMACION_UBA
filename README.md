# APLICACIONFINAL_PROGRAMACION_UBA
# Grupo 2
# Trabajo Práctico Taller de Programación de la Maestría en Economía Aplicada UBA.
# Autores: Andrea Chasi, Santiago Soler, Pablo Ortiz

# Determinantes de la Pobreza Multidimensional en Chile (CASEN 2024): Un Enfoque de Machine Learning y Econometría

## 📌 Descripción del Proyecto
Este repositorio contiene el código y la documentación para el análisis de los determinantes de la pobreza multidimensional en Chile, utilizando los microdatos de la encuesta CASEN 2024 (aprox. 70,000 hogares). El proyecto contrasta la capacidad predictiva de algoritmos no lineales de Machine Learning con la interpretabilidad de modelos econométricos tradicionales.

## 🎯 Objetivos
* **Predictivo:** Entrenar modelos de ensamble (Random Forest, XGBoost) para predecir el riesgo de que un hogar caiga en pobreza multidimensional basándose en predictores no monetarios (salud, educación, vivienda, entorno).
* **Inferencial:** Estimar modelos de respuesta binaria (Logit/Probit) para cuantificar los efectos marginales de las variables más determinantes identificadas por los algoritmos.
* **Evaluación:** Comparar el rendimiento de los modelos utilizando métricas de clasificación robustas ante clases desbalanceadas (F1-score, AUC-ROC).

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python / R
* **Manipulación de Datos:** Pandas, NumPy / Tidyverse
* **Base de Datos:** PostgreSQL (para almacenamiento estructurado y consultas con DBeaver, en caso de procesar históricos).
* **Machine Learning & Econometría:** Scikit-learn, XGBoost, Statsmodels / caret, tidymodels.
* **Documentación:** LaTeX (vía Pandoc/Overleaf) para la redacción del *paper* o reporte # Determinantes de la Pobreza Multidimensional en Chile (CASEN 2024): Un Enfoque de Machine Learning y Econometría

## 🔍 Segunda Instancia: Segmentación de Severidad (Clustering)

### Herramienta aplicada
K-means, en dos etapas siguiendo la metodología de Caruso, Sosa-Escudero y Svarc (2011, CEDLAS-UNLP): (1) clustering sobre los hogares pobres para encontrar niveles de severidad, y (2) selección de variables externas que permiten explicar esa segmentación sin incurrir en circularidad.

### Qué se hizo
- Filtro de los 10.421 hogares en pobreza multidimensional (`pobreza_multi = 1`)
- Selección de *k* mediante inercia (método del codo) y silhouette score, evaluando *k*=2 a 8
- K-means (*k*=3) sobre variables de redes de apoyo e inseguridad alimentaria (módulo R de CASEN), identificando un cluster del 26,4% de los hogares pobres con mayor severidad
- Selección de variables externas (salud, educación, vivienda) que mejor predicen esa severidad, evitando usar las mismas variables con las que se armaron los clusters

### Resultados principales
- Vivienda predice la severidad con AUC = 0,615; salud con AUC = 0,534 — la vivienda es un predictor bastante más fuerte que la salud
- Las variables de redes de apoyo e inseguridad alimentaria, que no forman parte del índice oficial de pobreza multidimensional, resultaron ser las más informativas para distinguir severidad

### Archivos de esta instancia
- `CASEN2024_analisis.ipynb` — notebook actualizado con las secciones de clustering (puntos 9 a 20)
- `AplicacionFinal_Clustering.pptx` — presentación de esta segunda instancia
