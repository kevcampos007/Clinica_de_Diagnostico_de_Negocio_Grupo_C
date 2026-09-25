# Clínica de Diagnóstico de Negocio — Grupo C

Este proyecto contiene dos ejercicios independientes de aprendizaje supervisado. Cada caso tiene su propio notebook, CSV y README específico. Ejecute cada notebook con su CSV correspondiente; no intercambie los archivos entre casos.

| Caso | Tarea | Notebook | CSV requerido | README del caso |
|---|---|---|---|---|
| A | Predicción de abandono de clientes (*churn*): clasificación binaria | [Caso A](clinica_diagnostico_negocio_GrupoC_CasoA.ipynb) | `Churn Prediction.csv` | [README Churn Prediction](README%20Churn%20Prediction.md) |
| B | Predicción de ingresos mensuales por sucursal: regresión | [Caso B](clinica_diagnostico_negocio_GrupoC_CasoB.ipynb) | `Sales Prediction.csv` | [README Sales Prediction](README%20Sales%20Prediction.md) |

Los resultados de ambos casos proceden de simulaciones con fines académicos; no son predicciones operativas verificadas con datos reales.

## 1. Obtener el repositorio

Necesita Git y Python 3 con `pip`. Clone el repositorio y entre en la carpeta creada:

```bash
git clone https://github.com/kevcampos007/Cl-nica-de-Diagn-stico-de-Negocio---Grupo-C.git clinica-diagnostico-negocio
```

Después de clonar, compruebe que aparezcan los notebooks y CSV de la tabla anterior. Si aún no están publicados en el repositorio remoto, use la carpeta de entrega que contiene estos archivos. Si ya los tiene descargados, omita la clonación y abra una terminal en esa carpeta. Los notebooks buscan sus datos desde el directorio de trabajo del kernel.

## 2. Instalar dependencias y abrir Jupyter

Instale las bibliotecas en el mismo entorno de Python que seleccionará como kernel:

```bash
python -m pip install numpy pandas matplotlib seaborn scikit-learn ipython jupyter ipykernel
```

Desde la carpeta del repositorio, inicie Jupyter con `python -m jupyter lab`. También puede abrir esta carpeta en VS Code con soporte para notebooks. Seleccione el kernel donde instaló las dependencias. Mantenga los dos notebooks y los dos CSV en esta carpeta; ejecute cada caso en un kernel separado y use **Ejecutar todas** desde la primera celda.

## 3. Ejecutar el Caso A

1. Compruebe que `Churn Prediction.csv` esté en la misma carpeta; el CSV del Caso B no interviene.
2. Abra [el notebook del Caso A](clinica_diagnostico_negocio_GrupoC_CasoA.ipynb) y seleccione el kernel preparado.
3. Ejecute todas las celdas desde el inicio. El notebook valida el CSV, simula clientes, compara Regresión Logística y Random Forest, y muestra métricas de clasificación.
4. Revise los resultados y las limitaciones en [README Churn Prediction](README%20Churn%20Prediction.md).

## 4. Ejecutar el Caso B

1. Compruebe que `Sales Prediction.csv` esté en la misma carpeta; no necesita el archivo original de clientes ni el CSV del Caso A.
2. Abra [el notebook del Caso B](clinica_diagnostico_negocio_GrupoC_CasoB.ipynb) y seleccione el kernel preparado.
3. Ejecute todas las celdas desde el inicio. La celda de construcción **sobrescribe `Sales Prediction.csv`** con 360 observaciones simuladas reproducibles (semilla 42); luego compara Ridge y Random Forest con el ingreso del mes anterior.
4. Revise los resultados y las limitaciones en [README Sales Prediction](README%20Sales%20Prediction.md).

## 5. Si aparece un error de archivo

Ejecute `Path.cwd()` en una celda para verificar el directorio de trabajo y vuelva a iniciar el notebook desde la carpeta que contiene los CSV. Si una celda del Caso B solicita columnas como `ID` o `Dt_Customer`, cierre esa copia antigua y abra el notebook del Caso B enlazado arriba: el CSV actual es mensual y no contiene esas columnas.
