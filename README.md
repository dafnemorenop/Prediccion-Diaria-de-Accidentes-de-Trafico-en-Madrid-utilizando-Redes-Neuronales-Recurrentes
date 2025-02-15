# Proyecto Accidentalidad

Este repositorio contiene varios scripts relacionados con el proyecto Accidentalidad. Los datos utilizados para el desarrollo del proyecto han sido obtenidos del Portal de Datos Abiertos del Ayuntamiento de Madrid.

[Accidentes de tráfico de la Ciudad de Madrid - Portal de datos abiertos del Ayuntamiento de Madrid
](https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default)

## Descripción

Predicción Diaria de Accidentes de Tráfico en Madrid utilizando Redes Neuronales Recurrentes: Un Enfoque de Deep Learning para Análisis de Series Temporales.

## Objetivo

Este proyecto se enfocó en el desarrollo de un modelo de red neuronal recurrente (RNN) para predecir la cantidad diaria de accidentes de tráfico en Madrid. Aplicando técnicas de deep learning para el análisis de series temporales, el objetivo es proporcionar una herramienta que permita anticipar y mitigar riesgos, contribuyendo así a la implementación de medidas proactivas para mejorar la seguridad vial y reducir el número de accidentes.

## Archivos

- `01 - Limpieza`: Script para limpieza de datos.
- `02 - EDA`: Script para análisis de datos.
- `03 - Deep Learning Regresion`: Script para aplicar técnicas de regresión mediante deep learning. Este script utiliza modelos de aprendizaje profundo para realizar predicciones basadas en los datos procesados.
- `Complemento - Folium`: para limpiar datos y generar mapas interactivos de accidentes.
- `Data`: Esta carpeta contiene los **archivos CSV** que se utilizan como datos base para el proyecto. Todos los archivos de datos necesarios para el análisis se encuentran dentro de esta carpeta. Los datos corresponden a los registros de accidentes de tráfico ocurridos en la Comunidad de Madrid, abarcando el periodo desde 2010 hasta la fecha de realización del proyecto en 2024.

## Uso

Los archivos CSV, utilizados como base del proyecto, están dentro de la carpeta Data. El script de limpieza cargará los archivos de la carpeta `Data` utilizando la siguiente ruta: 

`ubicacion = f"Data/{year}_Accidentalidad.csv"`

El archivo `01 - Limpieza.ipynb` se encarga de procesar y limpiar los datos de los archivos CSV ubicados en la carpeta `Data`. Tras la limpieza, los datos son almacenados en un archivo binario llamado `accidentes.pkl`, que se utilizará en futuras fases del proyecto para evitar tener que procesar los datos desde cero cada vez.

A continuación se abre el archivo `02 - EDA.ipynb` para visualizar los datos, detectar valores nulos y anomalías, y explorar relaciones y patrones mediante estadísticas descriptivas y gráficos, sacando algunas conclusiones de ellos. 

En el archivo `03 - Deep Learning Regresion.ipynb` se crea un archivo `accidentes_series_temporales.pkl` que contiene los datos procesados para el modelo de predicción. Este archivo incluye lo siguiente:

- La variable objetivo (`target`) ya está guardada para iniciar el modelo.
- Se han añadido nuevos días con cero accidentes en Madrid para mejorar la precisión del modelo.
- Se han creado nuevas columnas que enriquecen el modelo.
- Las columnas originales han sido convertidas a formato numérico para facilitar su uso en el modelo de aprendizaje profundo.

Por último, `Complemento - Folium.ipynb` limpia los datos para generar diversos mapas de los accidentes por distritos en Madrid, utilizando la librería Folium.

- Mapa de Accidentes en Madrid

![image](https://github.com/user-attachments/assets/a479b56e-4ebf-4d68-970b-d5137c2dfb4f)


- Mapa por distritos en Madrid

![image](https://github.com/user-attachments/assets/331cb134-ba9b-4f2b-993a-e520e9831624)


- Mapa de accidentes recurrentes en Madrid

![image](https://github.com/user-attachments/assets/c06d6985-7242-455f-a824-2ab68a3b3bb2)

## Instalación de librerías

Para ejecutar los scripts en este proyecto, asegúrate de tener instaladas las librerías que aparecen en `requirements.txt`. Puedes instalarlas todas ejecutando el siguiente comando:

```bash
pip install -r requirements.txt

