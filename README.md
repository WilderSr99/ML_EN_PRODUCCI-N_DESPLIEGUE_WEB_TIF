# 📊 Proyecto de Despliegue de Modelos de Machine Learning en Web

**Curso:** 612491 - Machine Learning en Producción (Despliegue Web)  
**Docente:** Orlando Advíncula Zeballos  
**Grupo:** 04  

---

## 👥 Integrantes

- Chavez Gallo, Daniel Alfredo  
- Medina Santamaria, Carlos Santiago  
- Poma Huaman, Brayan  
- Ramos Arphi, Carlos Humberto  
- Salcedo Piscoya, Ricardo Martin  
- Sebastian Rios, Wilder Teddy  

---

## 🧠 Descripción del Proyecto

Este repositorio presenta el desarrollo, implementación y despliegue de dos modelos de **Machine Learning** orientados a fortalecer la **toma de decisiones en el sector público peruano**, específicamente en:

- 💰 Ejecución presupuestal  
- 🚰 Calidad del agua (cloro residual)  

El enfoque del proyecto busca evolucionar desde análisis descriptivos hacia **sistemas predictivos proactivos**, facilitando la gestión basada en datos.

---

## 📌 Proyectos Desarrollados

### 🔹 A. Modelo de Regresión: Ejecución Presupuestal

**Objetivo:**  
Predecir el nivel de ejecución presupuestal al cierre del tercer trimestre (septiembre).

**Fuente de datos:**  
- Datos abiertos del MEF (2017–2025)  
- ~30,000 registros  

**Problemática:**  
La gestión presupuestal suele depender de análisis históricos descriptivos sin capacidad predictiva.

**Modelo implementado:**  
- Algoritmo: `XGBoost`  
- Métrica principal: RMSE ≈ 13% – 14%  

**Variables relevantes:**
- % de ejecución acumulada a agosto  
- Variación mensual  
- Departamento  
- Categoría de gasto  

---

### 🔹 B. Modelo de Clasificación: Cloro Residual (MVCS)

**Objetivo:**  
Predecir el cumplimiento de niveles adecuados de cloro residual en sistemas de agua potable.

**Contexto:**
- 18,855 prestadores de servicios de saneamiento  
- Solo ~35% cumple con estándares  

**Problemática:**  
Limitada capacidad de detección temprana de riesgo en la calidad del agua.

**Enfoque del modelo:**
- Clasificación supervisada  
- Sistema de alerta temprana  
- Priorización de intervenciones  

**Impacto esperado:**
- Optimización de inversiones públicas  
- Mejora en asistencia técnica  
- Gestión basada en riesgo  

---

## ⚙️ Pipeline de Machine Learning

### 🧪 1. Construcción y Entrenamiento

- Limpieza y análisis exploratorio (`pandas`)  
- Ingeniería de características  
- Selección de variables:
  - Boruta  
  - RFE  
- Modelos evaluados:
  - Random Forest  
  - Gradient Boosting  
  - XGBoost  
- Métricas:
  - Regresión: RMSE, MAE  
  - Clasificación: Accuracy  
- Serialización del modelo (`.joblib`)  

---

### 🖥️ 2. Desarrollo de la Aplicación

- Framework: **Streamlit**  
- Archivo principal: `streamlitpipelines.py`  

**Funcionalidades:**
- Ingreso de variables por el usuario  
- Transformación de inputs  
- Predicción en tiempo real  
- Visualización de resultados:
  - Gráficos  
  - Indicadores clave  

---

### 🚀 3. Despliegue

- Control de versiones con GitHub  
- Despliegue en **Streamlit Cloud**  
- Gestión de dependencias con `requirements.txt`  

---

## 🌐 Aplicaciones en Producción

### 🔹 Modelo de Regresión
👉 https://grupo4regresion.streamlit.app/

### 🔹 Modelo de Clasificación
👉 https://grupo4clasificacion.streamlit.app/

---

## 💻 Repositorios

### 📁 Regresión
- https://github.com/zerolab-dev/TRABAJO_REGRESION_G4  
- https://github.com/WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF.git  

### 📁 Clasificación
- https://github.com/WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF.git  

---

## 📈 Enfoque Estratégico

El proyecto integra dos paradigmas complementarios:

- **Regresión:** Predicción cuantitativa del desempeño presupuestal  
- **Clasificación:** Identificación temprana de riesgo en servicios de agua  

**Valor generado:**
- Anticipación de escenarios críticos  
- Soporte a la toma de decisiones  
- Priorización eficiente de recursos públicos  

---

## 🏁 Conclusión

Este proyecto demuestra cómo el uso de **Machine Learning en producción**, combinado con herramientas de despliegue accesibles como Streamlit, puede generar soluciones aplicables y escalables en el sector público.

---