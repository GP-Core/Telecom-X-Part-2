# Telecom X - Parte 2

## Propósito del Proyecto
El objetivo principal de este análisis es **predecir el churn (cancelación de clientes)** de TELECOM X.  
Se busca identificar los **factores más influyentes en la decisión de cancelar** y generar **estrategias de retención** basadas en los resultados obtenidos.

---

##  Proceso de Preparación de los Datos

### Clasificación de Variables
- **Variables categóricas:** tipo de contrato, servicio de internet, soporte técnico, método de pago, etc.  
- **Variables numéricas:** cargo mensual, cargo total, tiempo de permanencia (tenure), entre otras.  
---

### Normalización y Codificación
- **Codificación:** las variables categóricas se transformaron mediante **One-Hot Encoding**, lo que permitió convertirlas en variables binarias sin sesgar el modelo.  
- **Normalización:** se aplicó **MinMaxScaler** a las variables numéricas para llevarlas a una escala común entre 0 y 1, asegurando que modelos sensibles a la magnitud de las variables (ej. KNN, Regresión Logística) no se vieran sesgados.  

---

### Separación de Datos
Los datos fueron divididos en:
- **Conjunto de entrenamiento (80%)** → para entrenar los modelos.  
- **Conjunto de prueba (20%)** → para evaluar el rendimiento real de los modelos.  

Esto garantizó una **validación más justa** del desempeño y evitó el sobreajuste.

---

## Modelización y Justificación de Decisiones
Se utilizaron diferentes modelos de clasificación para comparar resultados:

- **Regresión Logística:** ofrece interpretabilidad a través de los coeficientes, útil para identificar el impacto de cada variable.  
- **Random Forest:** mejora la precisión y ofrece análisis de **feature importance**.  
La combinación de estos modelos permitió obtener **predicciones más confiables** y al mismo tiempo comprender **qué variables afectan más al churn**.
