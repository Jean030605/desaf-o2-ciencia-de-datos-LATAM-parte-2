# 🤖 Predicción y Modelado de Retención de Clientes (Churn) - Telecom X (Parte 2)

Este proyecto representa la segunda fase del análisis de retención de clientes para Telecom X. Tras finalizar la etapa de limpieza y análisis exploratorio (ETL y EDA), este enfoque se centra en el **Machine Learning**. Se implementan técnicas de preprocesamiento avanzado, balanceo de datos y entrenamiento de modelos predictivos para anticipar qué clientes tienen mayor probabilidad de abandonar el servicio y entender los motivos subyacentes.

## 🎯 Propósito del Análisis

El objetivo principal de esta fase es pasar de la descripción a la predicción y prescripción:
- **Preprocesar** los datos categóricos y numéricos para que sean interpretables por algoritmos de Machine Learning.
- **Resolver el desbalanceo de clases** (es común que haya menos clientes que se van que los que se quedan) utilizando técnicas sintéticas como ADASYN, asegurando que el modelo aprenda a detectar las fugas correctamente.
- **Entrenar y evaluar** modelos de clasificación (SGD Classifier y Gradient Boosting) para predecir el churn.
- **Extraer insights accionables** para el negocio mediante la interpretación de la importancia de las variables, identificando qué factores retienen a los clientes y cuáles los empujan a cancelar.

## 📂 Estructura del Proyecto

La organización de los archivos para esta fase es la siguiente:

* `Analisis_Churn_TelecomX_2_Jean.ipynb`: El notebook de Jupyter principal que contiene el flujo completo de Machine Learning (Encoding, Balanceo, Modelado y Evaluación).
* `telecom_x_limpio.csv`: Archivo de entrada requerido. Es el dataset limpio generado en la primera parte del proyecto (ETL). El script te pedirá subir este archivo al iniciar.

## 💡 Ejemplos de Gráficos e Insights Obtenidos

El notebook genera visualizaciones analíticas y resultados estratégicos, tales como:

1. **Relevancia por Información Mutua:** Un gráfico de barras que clasifica qué variables comparten más información con la decisión de cancelar el servicio, destacando los predictores más fuertes antes del modelado.
2. **Matrices de Confusión:** Visualizaciones térmicas (heatmaps) que permiten comparar el rendimiento del *SGD Classifier* frente al *Gradient Boosting*, mostrando claramente los falsos positivos y la precisión en la detección de fugas (Recall).
3. **Importancia de Variables (Permutation Importance):** Gráficos que revelan el "Top 10" de factores decisivos para el modelo Gradient Boosting al momento de predecir el churn.
4. **Insights Estratégicos Directos:** A través de los coeficientes del modelo SGD, el código imprime directamente qué factores *aumentan radicalmente la probabilidad de cancelación* y cuáles son los mejores *anclajes de retención* para la empresa.

## 🚀 Instrucciones de Ejecución

Sigue estos pasos para reproducir los modelos predictivos:

### Prerrequisitos
Además de las librerías básicas, necesitarás instalar `scikit-learn` y `imbalanced-learn`. Ejecuta:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
