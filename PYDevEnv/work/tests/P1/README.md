# Parcial 1 — Teoría de Aprendizaje de Máquina (TAM 2025-2)

### Universidad Nacional de Colombia

**Curso:** Teoría de Aprendizaje de Máquina  
**Profesor:** Andrés Marino Álvarez Meza
**Estudiante:** Mateo Almeida Gómez
**Periodo:** 2025-2  
**Repositorio:** `MLT-LR/PYDevEnv/work/P1/...

---

## Descripción General

Este proyecto desarrolla un **pipeline completo de aprendizaje supervisado y análisis comparativo CPU vs GPU** utilizando el conjunto de datos de **NFL Big Data Bowl 2026** (Kaggle).  
El objetivo es **evaluar, ajustar y optimizar distintos modelos de regresión** implementados en **scikit-learn** y **cuML (RAPIDS)**, analizando su rendimiento, tiempos de ejecución y capacidad predictiva.

El trabajo se estructura en torno a la teoría vista en clase (Bishop, Prince, Murphy) y al flujo aplicado de _machine learning engineering_.

---

## Entorno y dependencias

**Requisitos base**

- Python ≥ 3.9
- pip install -r requirements.txt

**Principales librerías**

- pandas / numpy / matplotlib / seaborn
- scikit-learn
- RAPIDS (cuDF + cuML)
- Optuna / scikit-optimize
- Jupyter Notebook

---

## Roadmap del trabajo

### Etapas principales

- [x] **1️ Revisión teórica**

  - Entendiendo el desarrollo del problema, planeando el flujo de trabajo, comprendiendo los fundamentos de regresión lineal, regularización (L1/L2), descenso de gradiente, kernel, ensambles y modelos bayesianos.
  - Estructurando el cuadro comparativo sobre los diferentes modelos y regresores, de acuerdo a sus hiperparámetros, métodos y estructura matemática.
  - Consulta y verificacion del funcionamiento de RAPIDS, métodos, hiperparámetros e implementación.
  - Textos guía: Bishop (2006), Prince (2024).
    - Kaggle NFL Big Data Bowl 2026.
    - RAPIDS AI Documentation.

- [x] **2 Exploración del dataset de la NFL (EDA)**

  - Carga y descripción del conjunto _NFL Big Data Bowl 2026_.
  - Limpieza, codificación de variables, detección de valores faltantes.
  - Visualización de distribuciones, correlaciones y patrones.

- [x] **2.1 Preprocesamiento**

  - Escalado y normalización (`StandardScaler` / `cuml.preprocessing.StandardScaler`).
  - Codificación de variables categóricas.
  - División del dataset (60 % entrenamiento / 20 % validación / 20 % prueba).
  - Conversión a `cudf` para ejecución en GPU.

- [x] **2.2 Entrenamiento de modelos**

  - **Lineales:** LinearRegression, Ridge, Lasso, ElasticNet, BayesianRidge.
  - **Kernel y gradiente:** KernelRidge, SVR, SGDRegressor.
  - **Ensamble:** RandomForestRegressor, GradientBoostingRegressor, XGBoostRegressor.
  - Medición de tiempos, cálculo de métricas (MAE, MSE, RMSE, R², MAPE).
  - Comparación CPU vs GPU.

- [x] **2.3 Optimización bayesiana (HPO)**

  - Definición de espacios de búsqueda (`n_estimators`, `max_depth`, `alpha`, `gamma`, etc.).
  - Ejecución con Optuna (`study.optimize`) — mínimo 20 trials.
  - Guardado del estudio en `hpo_study.db` y visualización de importancia de parámetros.

- [x] **2.4 Comparativa y resultados**

  - Generación de `metrics_comparison.csv`.
  - Visualización con gráficos de barras (tiempo / error).
  - Identificación del mejor modelo y análisis teórico del resultado.

- [x] **3 Conclusiones**
  - Evaluación global del desempeño en CPU y posterior implementación en GPU.
  - Discusión sobre precisión, velocidad y generalización.
  - Propuestas de mejora y extensiones (deep learning, más datos, tuning avanzado).

---

## Estructura de Directorios

P1/  
├── data/ # Datasets descargados de Kaggle  
├── notebooks/ # Jupyter notebooks del proyecto  
│ ├── 01_exploracion.ipynb  
│ ├── 02_entrenamiento.ipynb  
│ └── 03_evaluacion.ipynb  
│  
├── results/ # Resultados del entrenamiento y métricas  
│ ├── metrics/ # Reportes de rendimiento  
│ ├── plots/ # Gráficos de comparación  
│ └── models/ # Modelos guardados  
│  
├── docs/ # Documentación específica del proyecto  
│  
└── README.md # Descripción y guía del P1

---

## Referencias

- Bishop, C. (2006). _Pattern Recognition and Machine Learning._ Springer.
- scikit-learn User Guide — [https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)
- RAPIDS AI Documentation — [https://rapids.ai/](https://rapids.ai/)
- Kaggle NFL Big Data Bowl 2026 — [https://www.kaggle.com/competitions/nfl-big-data-bowl-2026](https://www.kaggle.com/competitions/nfl-big-data-bowl-2026)
