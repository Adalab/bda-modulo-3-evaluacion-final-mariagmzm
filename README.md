# Análisis de Lealtad de Clientes de Aerolínea

Este proyecto analiza el comportamiento de los clientes de un programa de lealtad de una aerolínea para extraer información sobre sus actividades de vuelo y características demográficas.

## Descripción

El objetivo de este proyecto es realizar un análisis exploratorio de datos (EDA) a partir de dos conjuntos de datos de clientes de una aerolínea. El análisis incluye la limpieza de los datos, el tratamiento de valores nulos y la creación de visualizaciones para responder a preguntas clave del negocio.

## Datos

Se utilizaron dos archivos CSV:

*   `Customer Loyalty History.csv`: Contiene información demográfica de los clientes, como su ubicación, educación, ingresos y estado de su membresía.
*   `Customer Flight Activity.csv`: Contiene información sobre la actividad de vuelo de los clientes, incluyendo vuelos, distancia, y puntos acumulados y redimidos.

## Análisis Realizado

El análisis se llevó a cabo en un Jupyter Notebook (`Eval_Mod03_MariaGomez.ipynb`) y se divide en las siguientes fases:

### 1. Exploración y Limpieza de Datos

*   Se cargaron y exploraron los dos conjuntos de datos.
*   Se unieron los datos en un único DataFrame.
*   Se realizó una limpieza de datos que incluyó la corrección de valores negativos en salarios y la imputación de valores nulos.
*   El dataset limpio se guardó en `df.csv`.

### 2. Visualización

En el notebook `Visualizacion de archivo.ipynb` se generaron diversas visualizaciones para responder a preguntas como:

*   La distribución de vuelos a lo largo del año.
*   La relación entre la distancia de vuelo y los puntos acumulados.
*   La distribución demográfica de los clientes por provincia, estado civil y género.
*   La relación entre el nivel educativo y el salario.

## Cómo usar

Para replicar el análisis, se pueden ejecutar los Jupyter Notebooks en el siguiente orden:

1.  `Eval_Mod03_MariaGomez.ipynb`: Para la limpieza y preparación de los datos.
2.  `Visualizacion de archivo.ipynb`: Para generar las visualizaciones.