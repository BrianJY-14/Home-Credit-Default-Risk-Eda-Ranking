# Home Credit Default Risk: análisis exploratorio, limpieza y ranking predictivo de atributos

## Descripción

Proyecto académico de ciencia de datos desarrollado sobre el dataset `application_train.csv` del caso **Home Credit Default Risk**. El trabajo se centra en comprender la estructura del dataset, analizar la variable objetivo `TARGET`, evaluar la calidad de los datos, realizar limpieza y transformación de variables, balancear las clases y construir un ranking de atributos según su calidad predictiva.

El objetivo principal es identificar qué variables tienen mayor capacidad para distinguir entre clientes que incumplen y no incumplen el pago del crédito.

## Objetivos

- Describir la estructura general del dataset.
- Analizar la distribución de la variable objetivo `TARGET`.
- Evaluar la calidad de los datos mediante nulos, duplicados, columnas constantes y valores extremos.
- Limpiar el dataset y preparar una versión más consistente para el análisis.
- Convertir atributos categóricos en variables numéricas.
- Balancear las clases del target.
- Estimar la calidad predictiva de los atributos mediante distintos indicadores.
- Identificar visualmente los atributos con mejor capacidad de separación entre clases.

## Dataset

Se trabaja exclusivamente con el archivo `application_train.csv`, perteneciente al dataset **Home Credit Default Risk**. En el notebook se utiliza la variable `TARGET` como atributo objetivo, donde:

- `TARGET = 0`: cliente que no incumple
- `TARGET = 1`: cliente que incumple

## Metodología

El proyecto se desarrolla en las siguientes etapas:

1. **Descripción general del dataset**
   - número de filas y columnas
   - tipos de datos
   - rangos de valores
   - valores únicos

2. **Análisis del TARGET**
   - proporción de clases
   - gráficos de distribución
   - análisis de desbalance

3. **Calidad de datos**
   - columnas con valores nulos
   - porcentaje de nulos
   - filas con nulos
   - duplicados
   - columnas con una sola categoría
   - detección inicial de outliers

4. **Limpieza de datos**
   - eliminación de columnas con demasiados nulos
   - imputación por tipo de variable
   - tratamiento de outliers

5. **Conversión de categóricas a numéricas**
   - One-Hot Encoding
   - verificación del número de columnas generadas
   - conservación de atributos transformados

6. **Balanceo y ranking predictivo**
   - balanceo con SMOTE
   - correlación absoluta con `TARGET`
   - Mutual Information
   - diferencia de tasas de default
   - ranking final normalizado
   - histogramas por clase para los atributos más importantes

## Resultados principales

El ranking final identificó como atributos más relevantes a:

- `EXT_SOURCE_3`
- `EXT_SOURCE_2`
- `DAYS_BIRTH`

Los histogramas por clase mostraron que estos atributos presentan diferencias visibles entre `TARGET = 0` y `TARGET = 1`, reforzando su capacidad predictiva.

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- imbalanced-learn
- category_encoders
- SciPy
- Jupyter Notebook / Google Colab

## Archivos del proyecto

- `mainProcess.ipynb`: notebook principal con el desarrollo completo.
- `application_train_preparado.csv`: dataset procesado y listo para etapas posteriores.
- `requirements.txt`: dependencias del entorno.
- `.gitignore`: exclusiones para control de versiones.
- `README.md`: descripción general del proyecto.

## Instalación

Instala las dependencias con:

```bash
pip install -r requirements.txt