# Proyecto de Predicción de Drawdown en Pozos Petroleros

Este repositorio contiene los datos y el cuaderno de Jupyter con todo el flujo de análisis, modelado y optimización para predecir la eficiencia de los incrementos en pozos petroleros utilizando técnicas de Deep Learning.

---

## Contenido del repositorio

- **Datos**:  
  Archivo Excel con la información histórica de los pozos y sus propiedades geológicas y de producción.

datos/Dataset incrementos_8-19-2025.xlsx
Contiene la hoja `data` con todas las variables necesarias para el análisis.

- **Cuaderno de Jupyter**:  
El notebook principal organiza todo el proceso de forma secuencial:
1. **Carga de datos**: Importación de los datos desde Excel.
2. **Exploración de datos**:
   - Características geológicas y de reservorio (Formación, Porosidad, Permeabilidad, Profundidad OWC, Espesor, Composición de grano, Tipo y calidad de arena, etc.)
   - Producción histórica y desempeño de los pozos (BOPD, BWPD, BSW, tasas de producción, producción acumulada).
   - Gráficas resumidas (countplots, histograms, scatterplots, boxplots, lineplots).
3. **Preparación para modelado**:
   - Limpieza de datos.
   - Feature engineering.
   - Codificación de variables categóricas.
   - Escalado de variables numéricas.
   - Balanceo de clases usando SMOTENC.
4. **Entrenamiento de modelos de Deep Learning**:
   - MLP
   - LSTM
   - GRU
   - 1D-CNN
   - Evaluación de desempeño (accuracy, precision, recall, F1, matrices de confusión, curvas ROC)
5. **Optimización Bayesiana**:
   - Ajuste de hiperparámetros para GRU y CNN-1D.
   - Reentrenamiento de los modelos con los mejores parámetros.
   - Evaluación final.

---

## Requisitos

- Python 3.8+
- Librerías principales:
- pandas, numpy, matplotlib, seaborn
- scikit-learn, imblearn
- tensorflow, keras
- bayesian-optimization
- Para instalar todas las dependencias:
```bash
pip install -r requirements.txt
