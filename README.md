# Proyecto Accidentalidad

Este repositorio alberga varios scripts vinculados al proyecto Accidentalidad. En el archivo .zip se incluyen los archivos .csv utilizados como base del proyecto, los archivos .pkl generados tras la limpieza y el análisis exploratorio de datos (EDA), así como diversos mapas de los accidentes por distritos en Madrid, creados con la librería Folium. Debido a su tamaño, los archivos .pkl se encuentran en un archivo comprimido.

## Descripción

Predicción Diaria de Accidentes de Tráfico en Madrid utilizando Redes Neuronales Recurrentes: Un Enfoque de Deep Learning para Análisis de Series Temporales.

## Objetivo

Este proyecto se enfocó en el desarrollo de un modelo de red neuronal recurrente (RNN) para predecir la cantidad diaria de accidentes de tráfico en Madrid. Aplicando técnicas de deep learning para el análisis de series temporales, el objetivo es proporcionar una herramienta que permita anticipar y mitigar riesgos, contribuyendo así a la implementación de medidas proactivas para mejorar la seguridad vial y reducir el número de accidentes.

## Archivos

- `01 - Limpieza.ipynb`: Script para limpieza de datos.
- `02 - EDA`: Script para análisis de datos.
- `03 - Deep Learning Regresion`: Script para aplicar técnicas de regresión mediante deep learning. Este script utiliza modelos de aprendizaje profundo para realizar predicciones basadas en los datos procesados.

Dentro del archivo `.zip` incluido en el repositorio, encontrarás los siguientes elementos:

- **Archivos CSV**: Datos utilizados como base para el proyecto, dentro de la carpeta de Data.
- **Archivos PKL**: Archivos resultantes después de la limpieza y el análisis exploratorio de datos (EDA). Estos archivos contienen los datos procesados y limpios.
- **Mapas de Accidentes**: Mapas interactivos creados con la librería Folium, que muestran la distribución de accidentes por distritos en Madrid.

## Instalación

Para ejecutar los scripts en este proyecto, asegúrate de tener instaladas las siguientes librerías:

- `pandas` (para manipulación y análisis de datos)
- `numpy` (para operaciones numéricas)
- `re` (para operaciones con expresiones regulares)
- `plotly` (para visualización interactiva de datos)
  - `plotly.express` (para crear gráficos interactivos de forma sencilla)
  - `plotly.graph_objects` (para crear gráficos personalizados)
  - `plotly.subplots` (para crear subgráficos)
- `matplotlib` (para visualización de datos estática)
- `seaborn` (para visualización de datos estadísticos)
- `keras` (para construir y entrenar modelos de deep learning)
  - `keras.callbacks` (para callbacks durante el entrenamiento de modelos)
  - `keras.layers` (para diferentes capas de redes neuronales)
  - `keras.optimizers` (para optimizadores en redes neuronales)
- `tensorflow` (para crear y entrenar redes neuronales con Keras)
  - `tensorflow.keras.layers` (para capas en redes neuronales)
  - `tensorflow.keras.models` (para definir y entrenar modelos de redes neuronales)

## Uso

Sigue las instrucciones en los notebooks para ejecutar los scripts.
