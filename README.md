# APLICACIONFINAL_PROGRAMACION_UBA

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


