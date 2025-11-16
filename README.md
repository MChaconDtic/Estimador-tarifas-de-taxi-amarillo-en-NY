Repositorio con proyecto de bookcamp en python

# 🚕 Estimador-tarifas-de-taxi-amarillo-en-NY

Un proyecto de análisis de datos que utiliza viajes históricos de taxi amarillo en Nueva York para **explorar patrones de demanda** y construir un **modelo sencillo de regresión** que estime la tarifa aproximada de un viaje según la distancia y el horario.

---

## 2. 🏷️ Badges (opcional)

<!-- Actualiza estos badges con tu usuario / estado real -->
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Status](https://img.shields.io/badge/Status-En%20desarrollo-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 3. ❓ Problema que resuelve

Las personas que usan taxi amarillo en Nueva York (residentes y turistas) **no siempre saben cuánto les costará un viaje ni cuánto tiempo tardarán en llegar**, especialmente en horas de alta demanda.

Esto genera:

- 💸 **Sorpresas en la tarifa** al final del viaje.  
- ⏰ Dificultad para **planificar el tiempo** para citas, reuniones o vuelos.  
- 🤔 Falta de información clara y basada en datos históricos para decidir si conviene tomar un taxi u otra alternativa.

Este proyecto busca, de forma sencilla, aprovechar datos reales de viajes de taxi para **dar más transparencia** al usuario y ayudarle a **planificar mejor su tiempo y presupuesto**.

---

## 4. ✅ Solución propuesta

La solución es un **análisis exploratorio + modelo de regresión simple** entrenado con el dataset público  
**“NYC Yellow Taxi Trip Data”** (Kaggle), que:

- Analiza variables como:
  - Fecha y hora del viaje  
  - Distancia recorrida  
  - Número de pasajeros  
  - Tarifa pagada  
- Construye variables derivadas:
  - Duración del viaje  
  - Hora del día  
  - Día de la semana  
- Entrena un modelo de **regresión** (por ejemplo, regresión lineal) para **estimar la tarifa** a partir de distancia, hora y día.
- Expone los resultados en un **notebook / pequeño dashboard** donde:
  - El usuario ingresa distancia aproximada y horario.  
  - El modelo entrega una **tarifa estimada** (y opcionalmente duración).  
  - Se muestran gráficos simples de demanda y tarifas promedio por hora/día.

Outputs principales:

- 📊 Gráficos de patrones de demanda y tarifas.  
- 🤖 Modelo entrenado guardado en archivo (`.pkl`).  
- 🧮 Función o notebook para hacer predicciones de tarifa a partir de inputs sencillos.

---

## 5. ⭐ Características principales (Features)

- 🔍 **Análisis exploratorio de datos (EDA)** sobre viajes de taxi amarillo en NYC.
- 🧼 **Limpieza básica** de datos (valores nulos, distancias/tarifas inválidas, outliers extremos).
- ⏱️ Cálculo de **duración del viaje** y extracción de **hora del día** y **día de la semana**.
- 📈 **Visualizaciones** de:
  - Tarifas promedio por hora del día.
  - Número de viajes por día de la semana.
  - Relación entre distancia y tarifa.
- 🤖 **Modelo de regresión simple** para estimar la tarifa (modelo baseline fácil de entender).
- 🧮 Función / notebook que permite **ingresar un escenario** (distancia + horario) y obtener una **tarifa estimada**.
- 💾 Proyecto organizado con carpetas de `data/`, `notebooks/`, `src/` y `models/`.

---

## 6. 🛠️ Tecnologías utilizadas (Tech Stack)

**Lenguaje y entorno:**

- Python 3.10+

**Procesamiento de datos:**

- Pandas  
- NumPy  

**Machine Learning:**

- Scikit-learn  

**Visualización:**

- Matplotlib  
- Seaborn  

**Entorno de trabajo:**

- Jupyter Notebook / JupyterLab / Google Colab  

*(Opcional, si agregas dashboard)*

- Streamlit

---

## 7. 🗂️ Estructura del proyecto

> Nota: esta es la estructura sugerida. Puedes ajustarla a lo que realmente implementes.

```bash
taxifare-nyc/
├── data/
│   ├── raw/               # Datos originales descargados de Kaggle (CSV)
│   ├── processed/         # Datos limpios / muestreados
│   └── external/          # (Opcional) otras fuentes si las hubiera
│
├── notebooks/
│   ├── 01_exploracion_eda.ipynb      # Análisis exploratorio
│   ├── 02_limpieza_y_features.ipynb  # Limpieza y feature engineering
│   └── 03_modelo_regresion.ipynb     # Entrenamiento y evaluación del modelo
│
├── src/
│   ├── data_prep.py        # Funciones para cargar y limpiar datos
│   ├── train_model.py      # Script para entrenar y guardar el modelo
│   └── predict.py          # Función simple para cargar el modelo y predecir
│
├── models/
│   └── taxifare_regression.pkl  # Modelo entrenado (salida de train_model.py)
│
├── docs/
│   └── images/             # Capturas de gráficas y del flujo del proyecto
│
├── requirements.txt        # Dependencias del proyecto
├── README.md               # Este archivo
└── .gitignore
