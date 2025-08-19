# 🔍 Predicción de Evasión de Clientes – Telecom X (Parte 2)

Este repositorio contiene la **segunda etapa del análisis de churn (evasión de clientes)** para Telecom X. Luego de limpiar y preparar los datos en la Parte 1, aquí se desarrollan modelos de machine learning para predecir qué clientes tienen mayor probabilidad de cancelar el servicio.

---

## 🧠 Objetivo

Construir modelos predictivos que permitan anticipar la cancelación de clientes, identificar las variables más influyentes, y generar estrategias basadas en datos para mejorar la retención.

---

## 🧪 Flujo de Trabajo

### 1. 📥 Carga y Preparación de Datos

- Lectura del archivo limpio: `TelecomX_Datos_Limpios.csv`
- Eliminación de columnas irrelevantes (por ejemplo: ID del cliente)
- One-hot encoding para transformar variables categóricas
- Revisión del balance de clases (`Churn`)
- Escalado de variables numéricas (si aplica)

### 2. 📊 Análisis de Correlación

- Cálculo de correlaciones numéricas con respecto a la variable `Churn`
- Visualización de las variables más influyentes mediante `barplot`
- Análisis dirigido con `boxplots` (tiempo de contrato y gasto total vs. cancelación)

### 3. 🤖 Entrenamiento de Modelos

Se entrenaron y compararon dos modelos:

| Modelo               | Normalización | Tipo de algoritmo      |
|----------------------|----------------|-------------------------|
| Regresión Logística  | Sí              | Basado en distancia     |
| Random Forest        | No              | Basado en árboles       |

### 4. 📈 Evaluación de Desempeño

Cada modelo fue evaluado con las siguientes métricas:

- Accuracy
- Precision
- Recall
- F1-score
- Matriz de confusión

---

## 🔍 Principales Hallazgos

- Los clientes con **contratos mensuales**, **bajo tiempo de permanencia** y sin servicios adicionales como `Tech Support` o `Online Security` son los más propensos a cancelar.
- **Random Forest** presentó mejor rendimiento general, capturando relaciones no lineales entre variables.
- **Regresión Logística** permitió interpretar fácilmente la dirección e impacto de cada variable.

---

## 📌 Archivos Incluidos

- `TelecomX_Datos_Encoded.csv`: Dataset listo para modelado.
- `TelecomX_Modelado-2.ipynb`: Notebook con todo el análisis predictivo, visualizaciones, y conclusiones.
- `README.md`: Esta documentación.

---

## ✅ Próximos pasos sugeridos

- Implementar técnicas para balanceo de clases (`SMOTE`, `class_weight`).
- Realizar ajuste de hiperparámetros con `GridSearchCV`.
- Desarrollar un dashboard de monitoreo de churn.
- Integrar el modelo en un entorno de producción o aplicación de negocio.

---

📬 Para más información o propuestas de colaboración, no dudes en abrir un issue o contactarnos.
