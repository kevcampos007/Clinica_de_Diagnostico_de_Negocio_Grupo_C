# Clínica de Diagnóstico de Negocio
## Grupo C — Caso A: Predicción de Abandono de Clientes (Churn Prediction)

Este repositorio contiene la solución desarrollada por el **Grupo C** para el **Caso A: Predicción de abandono de clientes (*Churn Prediction*)**, correspondiente a la actividad evaluada de la Clínica de Diagnóstico de Negocio.

---

## 1. Descripción del Problema de Negocio

En empresas basadas en modelos de suscripción y servicios recurrentes, la pérdida de clientes (*customer churn*) representa una fuga crítica de ingresos y eleva los costos de adquisición para compensar las bajas.

- **Objetivo de negocio:** Anticipar qué clientes se encuentran en alto riesgo de cancelar su servicio para enfocar de manera proactiva campañas y esfuerzos de retención (atención preferencial de soporte, planes de fidelización o ajustes contractuales).
- **Tipo de problema analítico:** Clasificación supervisada binaria donde la variable objetivo es:
  - `Churn = 1`: El cliente cancela o abandona el servicio.
  - `Churn = 0`: El cliente permanece activo.
- **Variables consideradas:** Señales operativas y de comportamiento anteriores a la decisión de baja (antigüedad, frecuencia de uso, llamadas a soporte técnico, retrasos en pagos, tipo de suscripción, duración del contrato y gasto acumulado). Los atributos demográficos o personales se excluyen del entrenamiento para evitar sesgos discriminatorios.
- **Modelos evaluados:** 
  - **Regresión Logística:** Modelo base interpretable y rápido, verificado frente a supuestos de multicolinealidad (VIF).
  - **Random Forest Classifier:** Modelo basado en ensamble de árboles capaz de capturar relaciones no lineales e interacciones complejas.
- **Criterio de evaluación:** Priorización de **Recall** (cobertura de clientes en riesgo) y **F1-Score** (balance armónico entre precisión y recall), complementados con matriz de confusión y análisis de sobreajuste.

---

## 2. Estructura del Repositorio

```text
├── clinica_diagnostico_negocio_equipo.ipynb   # Notebook principal con EDA, modelado y evaluación
├── submission.csv                             # Archivo base de IDs y probabilidades de referencia
└── README.md                                  # Documentación e instrucciones de ejecución
```

---

## 3. Instrucciones para Ejecutar el Notebook

### Prerrequisitos
- **Python** 3.10 o superior (compatible con Python 3.14).
- Gestor de paquetes **pip**.
- Editor compatible con Jupyter Notebooks (VS Code, JupyterLab o Jupyter Notebook).

### Paso 1: Clonar el repositorio
Abre una terminal o consola y clona el proyecto:
```bash
git clone https://github.com/kevcampos007/Cl-nica-de-Diagn-stico-de-Negocio---Grupo-C.git
cd "Cl-nica-de-Diagn-stico-de-Negocio---Grupo-C"
```

### Paso 2: Instalar las dependencias
Instala las librerías necesarias ejecutando el siguiente comando:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn ipykernel
```

*(Nota: La primera celda del notebook también incluye una rutina de comprobación que instalará automáticamente cualquier dependencia faltante en el entorno del kernel).*

### Paso 3: Verificar archivos
Asegúrate de que el archivo `submission.csv` se encuentre en la misma carpeta que el notebook [clinica_diagnostico_negocio_equipo.ipynb](file:///c:/Users/kcampos/OneDrive%20-%20AirSupport%20Group/Documentos/Cl%C3%ADnica%20de%20Diagn%C3%B3stico%20de%20Negocio/clinica_diagnostico_negocio_equipo.ipynb).

### Paso 4: Ejecutar el Notebook
1. Inicia Jupyter Notebook o abre el proyecto en tu IDE preferido (como VS Code):
   ```bash
   jupyter notebook
   # o
   jupyter lab
   ```
2. Abre el archivo [clinica_diagnostico_negocio_equipo.ipynb](file:///c:/Users/kcampos/OneDrive%20-%20AirSupport%20Group/Documentos/Cl%C3%ADnica%20de%20Diagn%C3%B3stico%20de%20Negocio/clinica_diagnostico_negocio_equipo.ipynb).
3. Selecciona el kernel de Python correspondiente.
4. Ejecuta las celdas de forma secuencial mediante el botón **Run All** (o `Shift + Enter` celda por celda).
