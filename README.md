# 📊 Proyectos de Machine Learning  
## Predicción Presupuestal y Calidad del Agua (MVCS)

Este repositorio contiene la implementación y despliegue de dos modelos de **Machine Learning** orientados a transformar el análisis descriptivo tradicional en herramientas predictivas proactivas dentro del sector público peruano.

---

## 📌 1. Proyectos Desarrollados

### 🔹 A. Modelo de Regresión: Ejecución Presupuestal (Sector Producción)

**Objetivo:**  
Anticipar el nivel de ejecución presupuestal al cierre del tercer trimestre (septiembre).

**Problemática:**  
La gestión actual se basa en análisis descriptivos que no aprovechan el comportamiento histórico para predecir el gasto futuro.

**Metodología:**  
- Dataset: Datos abiertos del MEF (2017–2025)  
- Tamaño: ~30,000 registros  

**Algoritmo Seleccionado:**  
- `XGBoost`  
- Métrica: RMSE ≈ 13% – 14%  

**Variables Clave:**  
- Porcentaje acumulado al mes de agosto  
- Variación mensual de ejecución  
- Departamento  
- Categoría de gasto  

---

### 🔹 B. Modelo de Clasificación: Cloro Residual (MVCS)

**Objetivo:**  
Predecir el cumplimiento de estándares de cloro residual en sistemas de agua potable.

**Contexto:**  
- 18,855 prestadores de servicios de saneamiento  
- Solo el 35% cumple con niveles adecuados  

**Problemática:**  
Limitada capacidad de acción proactiva en la gestión de calidad del agua.

**Enfoque:**  
- Modelo de clasificación para detección temprana de riesgo  
- Sistema de alertas y priorización  

**Impacto Esperado:**  
- Optimización de inversiones  
- Mejora en programas de asistencia técnica  
- Gestión basada en riesgos  

---

## ⚙️ 2. Flujo de Trabajo (Machine Learning Lifecycle)

### 🧪 Fase 1: Construcción y Entrenamiento

- Exploración y limpieza de datos (`pandas`)  
- Ingeniería de características (variables acumuladas y variaciones)  
- Selección de variables (Boruta, RFE)  
- Entrenamiento de modelos:
  - Random Forest  
  - Gradient Boosting  
  - XGBoost  
- Evaluación con métricas (RMSE, MAE, accuracy según el caso)  
- Exportación del modelo (`.joblib`)  

---

### 🖥️ Fase 2: Desarrollo de la Interfaz

- Implementación en **Streamlit**  
- Archivo principal: `streamlitpipelines.py`  
- Transformación de inputs del usuario  
- Predicciones en tiempo real  
- Visualización:
  - Gráficos de barras  
  - Insights para toma de decisiones  

---

### 🚀 Fase 3: Despliegue

- Versionamiento en GitHub  
- Despliegue en **Streamlit Cloud**  
- Instalación automática de dependencias (`requirements.txt`)  

---

## 🌐 3. Acceso a las Aplicaciones

### 🔹 App de Regresión (Ejecución Presupuestal)
👉 https://mlenappucci-ndesplieguewebtif-ahxkwptjae8nchs9kvcqfq.streamlit.app/

### 🔹 App de Clasificación (Cloro Residual)
👉 https://mlenappucci-ndesplieguewebtif-gdajjaamzx8icq7i7qhlsr.streamlit.app/

---

## 💻 4. Repositorios del Proyecto

- 📁 **Modelo de Regresión:**  
  https://github.com/zerolab-dev/TRABAJO_REGRESION_G4  
  https://github.com/WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF.git

- 📁 **Modelo de Clasificación:**  
  https://github.com/WilderSr99/ML_EN_PRODUCCI-N_DESPLIEGUE_WEB_TIF.git

---

## 👥 5. Integrantes – Grupo 04

- Chavez Gallo, Daniel Alfredo  
- Medina Santamaria, Carlos Santiago  
- Poma Huaman, Brayan  
- Ramos Arphi, Carlos Humberto  
- Salcedo Piscoya, Ricardo Martin  
- Sebastian Rios, Wilder Teddy  

---

## 📈 6. Enfoque del Proyecto

Este trabajo integra dos enfoques complementarios:

- **Regresión:** Anticipación cuantitativa del gasto público  
- **Clasificación:** Identificación de riesgo en calidad del agua  

Ambos modelos permiten:

- Anticipación de escenarios críticos  
- Toma de decisiones basada en datos  
- Priorización eficiente de recursos públicos  
