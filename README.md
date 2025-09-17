# Proyecto de Ciencia de Datos: Análisis de Contrataciones SECOP II

Este repositorio contiene el análisis de datos realizado para el proyecto **"Aplicando lo aprendido: Ciencia de Datos en Acción"**. El objetivo es demostrar la capacidad de análisis, el manejo de herramientas y la aplicación de conceptos de ciencia de datos en un escenario realista, utilizando un conjunto de datos públicos de Colombia.

## Integrantes del Equipo:

* Lina Juliana Moreno
* Camila Ramos
* Javier L. Pinto

---

## Estructura del Proyecto

El análisis está dividido en tres etapas principales, que corresponden a los módulos del curso. El trabajo completo y reproducible se encuentra en el archivo de Jupyter Notebook (`.ipynb`).

---

### Etapa 1: Preparación y Limpieza de Datos

**Responsable:** Lina Juliana Moreno

**Objetivo:** Obtener, limpiar y preparar los datos para el análisis.

**Acciones Realizadas:**

* Carga del conjunto de datos "SECOP II - Contratos Electrónicos" desde **Datos Abiertos Colombia**.
* Identificación de tipos de variables (numéricas, categóricas, fechas).
* Estandarización de los nombres de las columnas.
* Manejo de valores nulos y eliminación de filas duplicadas para asegurar la calidad de los datos.

**Evidencia Adicional:** Se desarrolló una página interactiva para visualizar los hallazgos de esta etapa, disponible en este [enlace de Hugging Face](https://huggingface.co/spaces/LinaJMR/SECOP-II).

---

### Etapa 2: Análisis Exploratorio y Visualización

**Responsable:** Camila Ramos

**Objetivo:** Explorar los datos para encontrar patrones y relaciones mediante visualizaciones.

**Acciones Realizadas:**

* Cálculo de medidas de tendencia central (**media**, **mediana**, **moda**) y de dispersión (**rango**, **desviación estándar**).
* Creación de visualizaciones para resumir los hallazgos:
    * Gráficos de barras para identificar las entidades con más contratos.
    * Gráficos de pastel para mostrar la distribución de los tipos de contrato.
    * Histogramas y boxplots para analizar la distribución de valores numéricos.
* Análisis de correlación entre variables numéricas.

---

### Etapa 3: Modelo Predictivo y Conclusiones

**Responsable:** Xavier L. Pinto

**Objetivo:** Desarrollar un modelo predictivo simple, comunicar los hallazgos y proponer una aplicación profesional.

**Acciones Realizadas:**

* **Desafío Inicial:** Se intentó predecir el `valor_total_adjudicacion` mediante un modelo de regresión, pero el análisis reveló que la mayoría de los datos en esta columna no eran numéricos o eran cero, lo que hacía inviable el modelo.
* **Solución y Mejora:** Se cambió el enfoque para predecir el `tipo_de_contrato` usando un modelo de clasificación (**Árbol de Decisión**). Para mejorar su rendimiento, se agruparon las categorías de contratos minoritarias en una sola clase (**"Otro"**), una técnica común para manejar datos desbalanceados.
* **Evaluación del Modelo:** Se entrenó el modelo y se evaluó su rendimiento utilizando métricas como la **precisión** (`accuracy`) y una **matriz de confusión** para visualizar sus aciertos y errores.
* **Narrativa y Aplicación:** Se desarrolló una narrativa basada en los resultados del modelo, explicando cómo este análisis podría ser utilizado por entidades gubernamentales para optimizar la gestión y supervisión de procesos de contratación.

---

## Cómo Ejecutar este Proyecto

1.  Clona este repositorio.
2.  Asegúrate de tener un entorno de Python con librerías como `pandas`, `numpy`, `matplotlib`, `seaborn` y `scikit-learn`.
3.  Abre el archivo `.ipynb` en un entorno como Jupyter Notebook o Google Colab.
4.  Ejecuta las celdas en orden para reproducir todo el análisis.
