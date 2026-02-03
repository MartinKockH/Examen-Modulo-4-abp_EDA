# Examen-Modulo-4-abp_EDA

Este repositorio contiene un análisis exploratorio de datos (EDA) y un modelado base (regresión lineal simple y múltiple) sobre un dataset de clientes de e-commerce. El objetivo es entender patrones generales de comportamiento y evaluar si algunas variables explican el **monto gastado (USD)**.

## Contexto del dataset
El dataset incluye variables numéricas y categóricas relacionadas con clientes, por ejemplo:
- `edad`
- `numcompras` (número de compras)
- `montogastadousd` (monto gastado)
- `numvisitas`
- `numdevoluciones`
- `calificacionpromedio`
- `categoriapreferida`, `canalcompra`, `clientefrecuente`

> Nota: el dataset se generó/usa con fines académicos para practicar EDA, correlación y modelos simples.

## Qué se hizo (pasos)
1. **Carga y preparación**
   - Revisión de estructura, tipos de datos y tamaños.
   - Imputación básica (ej.: `calificacionpromedio` con mediana, `numdevoluciones` con 0).

2. **EDA (estadística descriptiva)**
   - Métricas resumen: media, mediana, desviación estándar, percentiles.
   - Visualizaciones: histogramas, boxplots y distribuciones de variables categóricas.

3. **Análisis de correlación (Pearson)**
   - Matriz de correlación para variables numéricas.
   - Heatmap y scatterplots para pares de interés.

4. **Modelos de regresión**
   - **Regresión lineal simple:** `montogastadousd ~ numcompras`
   - **Regresión lineal múltiple:** `montogastadousd ~ numcompras + numvisitas + edad + numdevoluciones`
   - Evaluación con métricas: \(R^2\), MSE, MAE y gráficos comparativos.

## Resultados principales
- **Correlación:** Las correlaciones entre las variables evaluadas fueron **muy cercanas a 0**, sin evidencia de asociaciones lineales relevantes.
- **Regresión simple:** \(R^2 = 0.0035\). El número de compras explica una fracción mínima del monto gastado.
- **Regresión múltiple:** \(R^2 = 0.0054\). La mejora es marginal, por lo que el poder explicativo sigue siendo muy bajo.

## Conclusión
En este dataset, las variables analizadas **no explican de forma relevante** el monto gastado usando correlación de Pearson ni regresión lineal (simple/múltiple). Estos modelos se interpretan como **baseline**; para mejorar el desempeño se requerirían más variables, transformaciones, segmentación de clientes o modelos no lineales.

## Cómo ejecutar
1. Clona el repositorio.
2. Abre el notebook en Jupyter/Colab.
3. Ejecuta las celdas en orden.

## Archivos principales
- `abp4_v02-1.ipynb`: Notebook con EDA, correlación y regresiones.
- `06_regresion_simple.*`: gráfico del modelo simple.
- `07_comparacion_modelos.*`: comparación de modelos.
- Otros `.png/.jpg`: visualizaciones del EDA.

## Requisitos
- Python 3.x
- pandas, numpy, matplotlib, seaborn
- scikit-learn, statsmodels (opcional según el notebook)
