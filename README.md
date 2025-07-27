# Proyecto_Fundamentos_IA_Entrenamiento

# Repositorio de Entrenamiento - Modelo Predictivo de Actividad Financiera Sospechosa

Este repositorio contiene todo el código y los recursos necesarios para el **entrenamiento y la evaluación** de modelos de Machine Learning destinados a predecir actividades financieras sospechosas (UAFE).

**El objetivo principal de este repositorio es producir los artefactos del modelo (`.pkl`) que serán utilizados en el despliegue.**

## 1. Descripción del Proyecto

El proyecto se enfoca en el desarrollo de un sistema de clasificación para identificar patrones de comportamiento financiero potencialmente ilícito. El proceso documentado en el notebook abarca:

- **Análisis Exploratorio de Datos (EDA)**: Inspección y limpieza del dataset.
- **Preprocesamiento de Datos**: Imputación de nulos y codificación de variables categóricas.
- **Balanceo de Datos**: Aplicación de submuestreo (undersampling) para corregir el desbalance de clases.
- **Entrenamiento de Modelos**: Implementación de Regresión Logística y Árboles de Decisión.
- **Evaluación de Rendimiento**: Uso de métricas como AUC-ROC, KS y matrices de confusión para validar los modelos.
- **Exportación de Artefactos**: Guardado de los pipelines de modelo entrenados para su uso en producción.

## 2. Estructura del Repositorio de Entrenamiento

- **`/` (raíz)**:
  - **`Modelo Predictivo De Actividad Licita Usando Machine Learning.ipynb`**: El Jupyter Notebook central con todo el flujo de trabajo de análisis y entrenamiento.
  - **`challengeUafe.csv`**: El conjunto de datos crudo utilizado para el proyecto.
  - **`requirements.txt`**: Un listado de las dependencias de Python necesarias para ejecutar el notebook.
  - **`README.md`**: Este archivo.
- **`/artifacts/` (Opcional, pero recomendado)**:
  - Directorio donde se guardarán los modelos exportados (`.pkl`).

## 3. Guía de Inicio y Replicación del Entrenamiento

### Prerrequisitos
- Python 3.8 o superior.
- Se recomienda un entorno virtual (`venv`).

### Pasos para la Instalación
1.  **Clonar el repositorio:**
    ```bash
    git clone [URL-DEL-REPOSITORIO-DE-ENTRENAMIENTO]
    cd [NOMBRE-DEL-REPOSITORIO]
    ```
2.  **Crear y activar un entorno virtual:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
    ```
3.  **Instalar las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```

### Ejecutar el Entrenamiento
Para replicar el proceso de entrenamiento y generar los artefactos del modelo, ejecuta el Jupyter Notebook:

```bash
jupyter notebook "Modelo Predictivo De Actividad Licita Usando Machine Learning.ipynb"
```
Markdown
Al ejecutar todas las celdas, el notebook realizará el análisis completo y guardará los siguientes archivos en el directorio raíz (o en /artifacts/ si se configura así):
pipeline_regresion_logistica.pkl
pipeline_arbol_decision.pkl
Estos archivos son el resultado final de este repositorio y deben ser transferidos al repositorio de despliegue.
4. Resumen del Proceso Técnico
El notebook utiliza Pipelines de scikit-learn para encapsular los pasos de preprocesamiento y el modelo. Esto garantiza que el mismo proceso se aplique de manera consistente tanto en el entrenamiento como en la predicción, evitando la fuga de datos. Los modelos se entrenan con una muestra balanceada para mejorar su capacidad de detectar la clase minoritaria (actividades sospechosas).
