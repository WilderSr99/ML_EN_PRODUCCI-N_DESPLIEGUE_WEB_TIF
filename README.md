# 🚀 Despliegue de Modelos de Machine Learning en Producción para el Sector Público Peruano

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28%2B-FF4B4B?logo=streamlit&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-1.7%2B-28B463?logo=xgboost&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3%2B-F7931E?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-150458?logo=pandas&logoColor=white)

Este repositorio consolida el desarrollo, entrenamiento y despliegue web de dos modelos de Machine Learning diseñados para fortalecer la toma de decisiones proactiva en el sector público peruano. Transicionamos del análisis descriptivo tradicional hacia sistemas predictivos en dos ejes críticos: **Ejecución Presupuestal** y **Calidad del Agua**.

---

## 📌 Información Académica

| Atributo | Detalle |
| :--- | :--- |
| **Curso** | 612491 - Machine Learning en Producción (Despliegue Web) |
| **Docente** | Orlando Advíncula Zeballos |
| **Grupo** | 04 |
| **Integrantes** | Chavez Gallo D., Medina Santamaria C., Poma Huaman B., Ramos Arphi C., Salcedo Piscoya R., Sebastian Rios W. |

---

## 🎯 Proyectos Desarrollados

### 🔹 A. Modelo de Regresión: Pronóstico de Ejecución Presupuestal
**Objetivo:** Predecir el porcentaje de ejecución presupuestal institucional al cierre del tercer trimestre (septiembre) basado en el comportamiento previo.

* **Contexto de Datos:** Histórico de datos abiertos del Ministerio de Economía y Finanzas (MEF) 2017–2025 (~30,000 registros procesados).
* **Problema de Negocio:** La gestión presupuestal pública peruana carece de herramientas de alerta temprana, dependiendo excesivamente de análisis forenses o descriptivos.
* **Solución Técnica:**
    * **Algoritmo:** `XGBoost Regressor`.
    * **Desempeño:** Error Cuadrático Medio (RMSE) validado entre **13% – 14%**.
    * **Features Clave:** `% ejecución acumulada a agosto`, `variación intermensual`, `departamento` y `categoría de gasto`.

### 🔹 B. Modelo de Clasificación: Riesgo en Cloro Residual (MVCS)
**Objetivo:** Clasificar y predecir el cumplimiento de los estándares de cloración en sistemas de agua potable administrados por prestadores de servicios de saneamiento rurales/pequeños.

* **Contexto de Datos:** Universo de 18,855 prestadores (donde históricamente solo ~35% cumple la norma de salubridad).
* **Problema de Negocio:** Incapacidad operativa para fiscalizar presencialmente a todos los prestadores a nivel nacional.
* **Solución Técnica:**
    * **Algoritmo:** Modelado supervisado de clasificación ensamblada.
    * **Impacto:** Actúa como un Sistema de Alerta Temprana, optimizando la asignación de recursos para inspecciones físicas y focalizando la asistencia técnica estatal basada en **riesgo predictivo**.

---

## ⚙️ Arquitectura y Pipeline de Machine Learning

El proyecto sigue metodologías estándar de MLOps para la puesta en producción de modelos aislados:

1.  **Ingeniería de Datos y Modelado (Training Pipeline)**
    * **Preprocesamiento:** Limpieza de datos, imputación y análisis exploratorio exhaustivo (`pandas`, `seaborn`).
    * **Selección de Features:** Algoritmos de envoltura y filtrado como **Boruta** y **RFE** (Recursive Feature Elimination) para asegurar parsimonia.
    * **Entrenamiento Algorítmico:** Benchmarking entre *Random Forest*, *Gradient Boosting* y *XGBoost*.
    * **Persistencia:** Exportación de modelos y transformadores óptimos vía `.joblib` para baja latencia de inferencia.

2.  **Desarrollo de Interfaz de Usuario (Inference Application)**
    * **Framework:** Construcción de UI interactiva utilizando **Streamlit** (`streamlitpipelines.py`).
    * **Flujo:** Interfaz de formularios dinámicos $\rightarrow$ Sanitización de *inputs* $\rightarrow$ Inferencia del modelo cargado en caché $\rightarrow$ Renderizado de indicadores y gráficos de soporte.

3.  **Despliegue y CI/CD Básico (Deployment)**
    * Repositorios versionados en GitHub.
    * Entorno virtual replicable administrado a través de `requirements.txt`.
    * Alojamiento de las aplicaciones en la nube PaaS de **Streamlit Cloud**.

---

## 🌐 Aplicaciones en Vivo (Endpoints de Producción)

Explora e interactúa con los modelos desplegados:

* 📊 **App de Ejecución Presupuestal (Regresión):** [https://grupo4regresion.streamlit.app/](https://grupo4regresion.streamlit.app/)
* 🚰 **App de Calidad del Agua (Clasificación):** [https://grupo4clasificacion.streamlit.app/](https://grupo4clasificacion.streamlit.app/)

---

## 💻 Estructura de Repositorios Fuente

El código fuente de modelado y despliegue se encuentra segmentado en los siguientes repositorios:

* **Módulo de Regresión:**
    * `zerolab-dev/TRABAJO_REGRESION_G4` ([Enlace](https://github.com/zerolab-dev/TRABAJO_REGRESION_G4))
    * Espejo: `WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF`
* **Módulo de Clasificación:**
    * `WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF` ([Enlace](https://github.com/WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF.git))

---

## 🏁 Conclusión Estratégica

La dualidad de este proyecto (Regresión cuantitativa + Clasificación cualitativa de riesgo) demuestra la viabilidad técnica de introducir **Machine Learning operativo en el estado peruano**. Al acoplar el poder analítico de XGBoost con herramientas de despliegue ágil como Streamlit, hemos construido un prototipo escalable que transforma datos estáticos en **inteligencia accionable para la optimización del gasto y la salud pública.**
