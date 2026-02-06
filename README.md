# ♻️Análisis y Predicción del Valor Económico de Metales en Desechos Electrónicos

Este proyecto analiza la composición de metales presentes en desechos electrónicos (e-waste) y desarrolla un modelo predictivo para estimar el beneficio económico (Profit) asociado a la recuperación de dichos materiales.

El trabajo combina análisis exploratorio de datos (EDA), preprocesamiento avanzado, modelado de regresión y la construcción de un pipeline reproducible, con foco en economía circular, reciclaje y sostenibilidad.

## 🎯Objetivos del proyecto

- Analizar la cantidad de metales valiosos presentes en distintos dispositivos electrónicos.
- Explorar relaciones entre:
- Tipo de dispositivo
- Antigüedad
- Estado
- Contenido metálico
- Estimar el beneficio económico potencial de la recuperación de metales.
- Construir un pipeline de Machine Learning listo para producción.
- Evaluar el modelo con métricas estándar de regresión.

## 🌍Contexto y motivación

Los residuos electrónicos representan uno de los flujos de desechos de mayor crecimiento a nivel global, pero también constituyen una fuente estratégica de metales valiosos como oro, plata, platino y litio.

## 📌Este análisis permite:

- Optimizar procesos de reciclaje.
- Priorizar dispositivos con mayor valor recuperable.
- Apoyar decisiones económicas y ambientales basadas en datos.

# 📊Dataset

- Se utilizan tres datasets complementarios sobre residuos electrónicos.
  
- Variables principales:
  - Identificación del dispositivo
  - Item Name
  - Category
  - Brand
  - Device Type
  - Características
  - Device Age
  - Manufacturing Year
  - Device Condition
  - Contenido metálico (g)
  - Oro, Plata, Aluminio, Carbono
  - Platino, Rodio, Níquel, Estaño, Litio

- Variables económicas:
  - Current Metal Value ($)
  - Profit / Profit ($) (variable objetivo)

📌 Los valores están medidos en gramos y dólares.

## 🔍Metodología

1️⃣ Limpieza y preparación de datos

- Eliminación de valores faltantes.
- Separación de variables numéricas y categóricas.
- Estandarización de variables continuas.
- Codificación One-Hot para variables categóricas.

2️⃣ Análisis Exploratorio de Datos (EDA)

- Estadísticos descriptivos.
- Análisis de correlaciones entre metales y beneficios.
- Mapas de calor para distintos conjuntos de datos.
- Comparación entre datasets originales y actualizados.

3️⃣ Modelado Predictivo

📌 Modelo principal

- Regresión Lineal

📌 Pipeline de Machine Learning

- Se construye un pipeline que incluye:
- StandardScaler para variables numéricas.
- OneHotEncoder para variables categóricas.
- LinearRegression como estimador final.
- El pipeline permite:
- Reproducibilidad.
- Facilidad de despliegue.
- Prevención de data leakage.

4️⃣ Evaluación del modelo

- Métricas utilizadas:
  - MSE (Mean Squared Error)
  - RMSE (Root Mean Squared Error)
  - MAE (Mean Absolute Error)
  - R² Score

📌 El modelo muestra una capacidad razonable para explicar la variabilidad del beneficio económico a partir del contenido metálico.

5️⃣ Persistencia del modelo

- El pipeline completo se guarda en formato .pkl mediante pickle.
- Permite reutilización directa sin reentrenamiento.

## 📈Principales insights

- Existe una fuerte correlación positiva entre metales preciosos y beneficio económico.
- El tipo y estado del dispositivo influyen significativamente en la rentabilidad.
- Los dispositivos más antiguos pueden contener composiciones metálicas más valiosas.
- El enfoque de pipeline facilita la escalabilidad del modelo a nuevos datos.

## 🛠️Tecnologías y Librerías

- Python
- Pandas / NumPy
- Matplotlib / Seaborn
- Scikit-learn
- Pickle

## 📁Estructura del proyecto

├── e_waste_dataset_with_profit.csv
├── e_waste_dataset (1).csv
├── updated_e_waste_dataset.csv
├── Análisis de metales en los desechos electrónicos.py
├── e_waste_pipeline.pkl
└── README.md


## 🚀Posibles mejoras futuras

- Modelos no lineales (Random Forest, XGBoost).
- Interpretabilidad con SHAP.
- Optimización del beneficio económico bajo restricciones ambientales.
- Análisis de sensibilidad por tipo de metal.
- Deploy como API para evaluación en tiempo real.

## 👤Autor

Flavia Hepp
Proyecto de Data Science aplicado a economía circular, reciclaje y sostenibilidad ambiental.
