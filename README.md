# Proyecto Accidentalidad

Este repositorio alberga varios scripts vinculados al proyecto Accidentalidad.

## Descripción

Predicción Diaria de Accidentes de Tráfico en Madrid utilizando Redes Neuronales Recurrentes: Un Enfoque de Deep Learning para Análisis de Series Temporales.

## Objetivo

Este proyecto se enfocó en el desarrollo de un modelo de red neuronal recurrente (RNN) para predecir la cantidad diaria de accidentes de tráfico en Madrid. Aplicando técnicas de deep learning para el análisis de series temporales, el objetivo es proporcionar una herramienta que permita anticipar y mitigar riesgos, contribuyendo así a la implementación de medidas proactivas para mejorar la seguridad vial y reducir el número de accidentes.

## Archivos

- `01 - Limpieza.ipynb`: Script para limpieza de datos.
- `02 - EDA`: Script para análisis de datos.
- `03 - Deep Learning Regresion`: Script para aplicar técnicas de regresión mediante deep learning. Este script utiliza modelos de aprendizaje profundo para realizar predicciones basadas en los datos procesados.
- `Complemento - Folium`: para limpiar datos y generar mapas interactivos de accidentes.
- **Archivos CSV**: Datos utilizados como base para el proyecto, dentro de la carpeta de Data (Se explica en Uso).


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

Los archivos CSV, utilizados como base del proyecto, deben estar organizados en una carpeta específica llamada Data. Como GitHub no permite subir carpetas vacías, es necesario que los usuarios creen esta carpeta manualmente y coloquen los archivos CSV correspondientes dentro de ella. 

El script de limpieza cargará los archivos de la carpeta `Data` utilizando la siguiente ruta: 

`ubicacion = f"Data/{year}_Accidentalidad.csv"`

El archivo `Limpieza.ipynb` se encarga de procesar y limpiar los datos de los archivos CSV ubicados en la carpeta `Data`. Tras la limpieza, los datos son almacenados en un archivo binario llamado `accidentes.pkl`, que se puede utilizar en futuras fases del proyecto para evitar tener que procesar los datos desde cero cada vez.

A continuación se abre el archivo `EDA.ipynb` para visualizar los datos, detectar valores nulos y anomalías, y explorar relaciones y patrones mediante estadísticas descriptivas y gráficos, sacando algunas conclusiones de ellos. 

En el archivo `Deep Learning Regresion.ipynb` se crea un archivo `accidentes_series_temporales.pkl` que contiene los datos procesados para el modelo de predicción. Este archivo incluye lo siguiente:

- La variable objetivo (`target`) ya está guardada para iniciar el modelo.
- Se han añadido nuevos días con cero accidentes en Madrid para mejorar la precisión del modelo.
- Se han creado nuevas columnas que enriquecen el modelo.
- Las columnas originales han sido convertidas a formato numérico para facilitar su uso en el modelo de aprendizaje profundo.

Por último, `Complemento - Folium` limpia los datos para generar diversos mapas de los accidentes por distritos en Madrid, utilizando la librería Folium.
