# DataModels - Supervised & Unsupervised Learning Models

## Descripción general

Este módulo contiene documentación y estructuras base relacionadas con modelos de Machine Learning aplicados a la toma de decisiones mediante algoritmos matemáticos.

Los modelos se dividen en dos grandes categorías:

- **Supervised Learning Models (Supervised_LMs)**
- **Unsupervised Learning Models (Unsupervised_LMs)**

Cada enfoque utiliza técnicas matemáticas y estadísticas distintas para analizar información, generar predicciones y apoyar procesos de decisión automatizados.

---

# Supervised_LMs

## ¿Qué son?

Los modelos supervisados utilizan datos etiquetados para aprender una función matemática capaz de realizar predicciones o clasificaciones.

El objetivo principal es aproximar una relación entre variables de entrada y resultados esperados mediante entrenamiento iterativo.

---

## Conceptos clave

- Datos de entrenamiento y prueba
- Variables de entrada (*features*)
- Variables de salida (*labels*)
- Ajuste de parámetros mediante minimización de error
- Validación cruzada (*cross-validation*)
- Generalización del modelo

---

## Algoritmos comunes

### Regresión

- Regresión lineal
- Regresión polinómica
- Regresión logística

### Clasificación

- Support Vector Machines (SVM)
- Árboles de decisión
- Random Forests
- Redes neuronales supervisadas

---

## Aplicaciones en toma de decisiones

- Predicción de riesgo
- Sistemas de scoring
- Clasificación binaria y multiclase
- Recomendación basada en historial
- Optimización de recursos
- Pronósticos y análisis predictivo

---

## Matemáticas importantes

### Funciones de pérdida

- Mean Squared Error (MSE)
- Cross-Entropy Loss

### Optimización

- Gradiente descendente
- SGD, Adam y variantes

### Regularización

- L1 (Lasso)
- L2 (Ridge)

### Fundamentos matemáticos

- Álgebra lineal
- Transformaciones matriciales
- Probabilidad y estadística
- Distribuciones y estimación

---

# Unsupervised_LMs

## ¿Qué son?

Los modelos no supervisados trabajan con datos sin etiquetas y buscan descubrir estructuras, relaciones o patrones ocultos dentro de los datos.

Estos modelos son útiles para exploración, segmentación y análisis de comportamiento.

---

## Conceptos clave

- Agrupamiento (*clustering*)
- Segmentación
- Reducción de dimensionalidad
- Detección de anomalías
- Extracción de características

---

## Algoritmos comunes

### Clustering

- K-Means
- Clustering jerárquico
- DBSCAN

### Reducción de dimensionalidad

- PCA (Principal Component Analysis)

### Representaciones profundas

- Autoencoders
- Modelos de embeddings

---

## Aplicaciones en toma de decisiones

- Segmentación de usuarios o pacientes
- Identificación de anomalías
- Descubrimiento de relaciones ocultas
- Agrupación de comportamientos similares
- Preprocesamiento para modelos supervisados

---

## Matemáticas importantes

### Métricas de distancia

- Distancia euclidiana
- Distancia Manhattan
- Similitud coseno

### Optimización

- Convergencia iterativa
- Minimización de funciones objetivo

### Estadística y álgebra lineal

- Covarianza
- Varianza
- Proyecciones lineales
- Factorización de matrices
- Espacios vectoriales

---

# Objetivo del proyecto

El propósito de este módulo es proporcionar una base estructurada para:

- Investigación en Machine Learning
- Desarrollo de modelos predictivos
- Sistemas de apoyo a decisiones
- Experimentación matemática y computacional
- Integración futura con sistemas hospitalarios y analíticos

# Estructura General


---


## Equipo de Desarrollo

| Integrante                   | Matrícula | Rol en el Equipo                     | Contacto                                                   |Observaciones |
|------------------------------|------------|--------------------------------------|-----------------------------------------------------------|--------------|
| Derek Sesni Carreño          | `230892`   | Lider, Desarrollo Backend           | [@DevFntxy](https://github.com/DevFntxy)                   | ⚠️ Pendiente |
| Diego Miguel Rivera Chavez   | `230260`   | Frontend, Diseño y Estructura de BD | [@DiegoMiguel04](https://github.com/DiegoMiguel04)         | ⚠️ Pendiente |
| José Arturo Garcia Gonzalez  | `230629`   | Diseño y Estructura de BD           | [@ppyo1234](https://github.com/ppyo1234)                   | ⚠️ Pendiente |
| Mauricio Rosales Gabriel     | `220859`   | Desarrollo Backend                  | [@elmau0834x](https://github.com/elmau0834x)               | ⚠️ Pendiente |
| Erick Matias Granillo Mejia  | `220045`   | Desarrollo Backend                  | [@EMATIAS](https://github.com/EMATIAS230045)               | ✔️ Validado |

---

# Estructura del proyecto

```text
DataModels/
│
├── Supervised_LMs/
│   ├── README.md
│   ├── supervised.gitkeep
│   └── vacio.js
│
└── Unsupervised_LMs/
    ├── README.md
    ├── unsupervised.gitkeep
    └── vacioun.js