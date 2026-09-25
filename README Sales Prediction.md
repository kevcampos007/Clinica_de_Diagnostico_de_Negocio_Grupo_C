# Caso B — Predicción de ingresos mensuales

**Tipo de tarea:** regresión (`ingresos_mensuales_UM` por sucursal y mes, en unidades monetarias simuladas).

## Objetivo

Estimar los ingresos de una sucursal con un mes de anticipación para apoyar la planificación comercial. El modelo es una demostración académica; sus predicciones no deben emplearse para aprobar presupuestos ni decisiones económicas reales.

## Datos y alcance

Según una auditoría previa, el archivo de clientes originalmente considerado tenía 2,240 registros y gastos acumulados, pero no ventas mensuales ni históricos de marketing, precios, competencia o macroeconomía. Ese archivo ya no se adjunta, por lo que la auditoría y su mediana de gasto de 396 no son reproducibles con esta entrega. El valor 396 se usa solo como parámetro ilustrativo de escala. El notebook genera 360 observaciones **sintéticas** de 15 sucursales durante 24 meses en `Sales Prediction.csv`. No exporta identificadores ni atributos demográficos individuales.

## Modelos y evaluación

Se comparan Ridge y Random Forest Regressor con el pronóstico ingenuo del ingreso del mes anterior. Se usan 14 meses para ajuste inicial, 4 para validación y 6 meses futuros para prueba; las métricas son MAE, RMSE y R². La simulación es principalmente lineal y puede favorecer a Ridge. El diagnóstico de validación muestra subpredicción, de modo que las métricas no demuestran rendimiento con ventas reales.

## Archivos del caso

- [Notebook del Caso B](clinica_diagnostico_negocio_GrupoC_CasoB.ipynb)
- `Sales Prediction.csv`: único CSV del caso, generado y leído por el notebook.

## Ejecución

Siga la clonación, instalación y apertura de Jupyter descritas en [README General](README%20General.md). Desde la carpeta del repositorio, abra el notebook del Caso B, seleccione el kernel con las dependencias y ejecute todas las celdas desde el inicio. La celda de construcción **sobrescribe `Sales Prediction.csv`** con la misma simulación determinista (semilla 42). No necesita el archivo original de clientes ni el CSV del Caso A.

## Limitaciones

No hay ventas mensuales observadas ni costos de error para validar utilidad comercial. Antes de cualquier aplicación real se necesitan datos transaccionales representativos, validación temporal adicional y revisión comercial, técnica y de privacidad para El Salvador.
