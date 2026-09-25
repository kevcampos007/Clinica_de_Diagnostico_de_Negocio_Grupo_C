# Caso A — Predicción de abandono de clientes

**Tipo de tarea:** clasificación binaria (`Churn = 1` si el cliente abandona; `Churn = 0` si permanece).

## Objetivo

Identificar clientes de un servicio de suscripción hipotético con mayor riesgo de abandono para priorizar acciones de retención. Las predicciones permitirían comparar abandonos detectados con contactos innecesarios; no autorizan decisiones sobre clientes reales.

## Datos y alcance

`Churn Prediction.csv` contiene 110,023 identificadores y puntuaciones `Exited` entre 0 y 1, pero no variables explicativas ni etiquetas históricas observadas. El notebook usa la media de esas puntuaciones **solo como supuesto de escala** y genera 8,000 clientes sintéticos con variables de actividad, soporte, pagos y contrato. No interpreta `Exited` como abandono real ni usa atributos demográficos para entrenar.

## Modelos y evaluación

Se comparan Regresión Logística y Random Forest Classifier. La selección se hace en validación con F1 y Recall; la prueba reservada informa Accuracy, Precision, Recall, F1-score y matriz de confusión. Se revisan multicolinealidad (VIF), atípicos y riesgos de sesgo. Las métricas describen únicamente la simulación.

## Archivos del caso

- [Notebook del Caso A](clinica_diagnostico_negocio_GrupoC_CasoA.ipynb)
- `Churn Prediction.csv`: archivo base que lee el notebook; debe permanecer en la misma carpeta.

## Ejecución

Siga la clonación, instalación y apertura de Jupyter descritas en [README general](README.md). Desde la carpeta del repositorio, abra el notebook del Caso A, seleccione el kernel con las dependencias y ejecute todas las celdas desde el inicio. El CSV del Caso B no interviene. La primera celda puede instalar dependencias faltantes en el entorno del kernel.

## Limitaciones

Los clientes, las variables y la etiqueta de abandono usados para entrenar son sintéticos. Antes de cualquier aplicación real se necesitan datos históricos etiquetados, evaluación de sesgos, costos de intervención y validación de privacidad.
