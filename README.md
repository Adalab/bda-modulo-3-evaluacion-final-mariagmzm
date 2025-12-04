# ✈️ Análisis de Lealtad de Clientes de Aerolínea (EDA)

Este proyecto se centra en el Análisis Exploratorio de Datos (EDA) del comportamiento de los clientes de un programa de lealtad de una aerolínea. El objetivo es consolidar la información transaccional y demográfica para extraer insights clave sobre los patrones de vuelo, la segmentación de clientes y la relación entre la actividad y el nivel de lealtad.

# 📂 Conjuntos de Datos (Datasets)

Se trabajaron con dos archivos CSV, unidos mediante el identificador Loyalty Number:

**Customer Loyalty History.csv**: Perfil demográfico del cliente (Salario, Educación, Estado Civil, Tipo de Tarjeta, CLV).

**Customer Flight Analysis.csv**: Actividad de vuelo del cliente por mes (Vuelos Reservados, Distancia, Puntos Acumulados y Redimidos).

# 🛠️ Fase 1: Limpieza y Preparación de Datos (Criterios Clave)

El proceso de limpieza y gestión de nulos fue crítico para asegurar la calidad de los datos, cubriendo los siguientes puntos:

**Unión de Datos**: Los dos datasets se unieron de forma eficiente mediante la columna Loyalty Number.

**Gestión de Nulos**: Se trataron los valores nulos en las fechas de cancelación (cancellation year/month) asumiendo que representan clientes activos (imputados con valores sentinel como 9999 y 0).

**Corrección Salarial**: Se aplicó la función de valor absoluto (np.abs) a los salarios negativos, asumiendo un error de tipeo en la entrada de datos.

**Imputación de Salario**: Se imputaron los salarios nulos restantes (ej., para la categoría 'College') utilizando la mediana condicional específica para cada nivel educativo.

**Estandarización**: Se aplicó el formato snake_case (flights_booked) a todas las columnas para mejorar la legibilidad del código.

# 📊 Fase 2: Visualización y Insights Clave

Utilizando visualizaciones con Matplotlib y Seaborn, se respondieron preguntas clave del negocio:

## 💡 Insights Obtenidos

**Distribución mensual de vuelos**: Se confirmó una fuerte estacionalidad, con picos de reservas en los meses de verano y diciembre. (Gráfico de Líneas).

**Relación Distancia vs. Puntos**: Se observó una correlación positiva muy clara. El análisis segmentado demostró que la tasa de acumulación de puntos es directamente determinada por el tipo de tarjeta de fidelidad. (Gráfico de Dispersión).

**Salario vs. Educación/Tarjeta**: Se confirmó que el salario promedio aumenta con el nivel educativo. Además, las tarjetas de nivel superior ('Gold', 'Platinum') están asociadas a un salario mediano significativamente mayor (demostrado con Boxplots). (Gráfico de Barras y Boxplot).

**Proporción de Tarjetas**: La tarjeta 'Star' es la categoría más común en la base de clientes. (Gráfico de Tarta).

**Distribución Geográfica**: Ontario es la provincia con la mayor concentración de clientes, lo que indica un mercado principal. (Gráfico de Barras).

## 🎯 Criterios Adicionales
**Legibilidad del Código**: Se priorizó el uso de código limpio y funciones vectorizadas de Pandas/NumPy.

**Gestión de Git**: Se realizaron commits descriptivos a lo largo del proceso de EDA y visualización.

**Archivos de Salida**: Se generó un DataFrame limpio (df.csv) para la fase de análisis