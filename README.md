# analisis-mercado-fertilizantes-mexico
# 🚜 Predicción de Precios de Importación: Fertilizantes Nitrogenados (México 2024)

Este proyecto analiza la cadena de suministro de fertilizantes nitrogenados (Urea) hacia México y desarrolla un modelo de Machine Learning para predecir costos de importación, optimizando la toma de decisiones logísticas y presupuestales.

## 🎯 Objetivos
1.  **Mapear la logística:** Entender rutas críticas (Rusia/Qatar -> Veracruz/Manzanillo).
2.  **Analizar costos:** Detectar ineficiencias y patrones estacionales.
3.  **Predecir precios:** Crear un modelo para estimar el `Unit_Price` (USD/Ton).

## 📊 Hallazgos Clave (EDA)
* **Logística:** Dependencia crítica del transporte marítimo (Vessel) para el 90%+ del volumen.
* **Geopolítica:** Rusia y Qatar dominan el suministro, pero China y EE.UU. son estratégicos en el Pacífico y Frontera Norte respectivamente.
* **Estacionalidad:** Se detectaron picos claros de importación alineados al ciclo agrícola Primavera-Verano.

## 🤖 Modelo Predictivo (Random Forest)
Se implementó un modelo de **Bosque Aleatorio (Random Forest)** optimizado tras una limpieza de *outliers* y segmentación por volumen.

| Métrica | Resultado | Interpretación |
| :--- | :--- | :--- |
| **R² Score** | **0.8816** | El modelo explica el 88% de la variabilidad del precio. |
| **MAE** | **$19.38 USD** | Margen de error menor al 6% sobre el precio promedio. |
| **RMSE** | **$51.64 USD** | Alta estabilidad ante variaciones del mercado. |

### Top 3 Drivers de Precio:
1.  **Categoría de Producto:** (Distinción Urea vs Otros Nitrogenados).
2.  **Tipo de Cambio (MXN-USD):** Impacto macroeconómico directo.
3.  **País de Origen:** (Rusia/Qatar vs EE.UU. tienen estructuras de costos muy distintas).

## 🛠️ Tecnologías
* Python 3.12
* Pandas & NumPy (Procesamiento)
* Matplotlib & Seaborn (Visualización)
* Scikit-Learn (Machine Learning: Random Forest, GridSearch)

## 🚀 Cómo correr este proyecto
1.  Clonar el repositorio.
2.  Instalar dependencias: `pip install -r requirements.txt`
3.  Ejecutar el Jupyter Notebook `Analisis_Fertilizantes.ipynb`.

---
*Autor: Mtro. César Dudley Castellanos Nieto*
