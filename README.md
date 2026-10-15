# Análisis de la Relación entre Indicadores Socioeconómicos y el PIB per cápita

## Descripción del proyecto

Este proyecto analiza la relación entre diferentes indicadores socioeconómicos y el PIB per cápita, utilizando datos del Banco Mundial (World Bank).

Se exploran asociaciones entre la esperanza de vida, el uso de internet y el desempleo, con el objetivo de identificar patrones estadísticos relacionados con las diferencias en los niveles de ingreso entre países y períodos.

## Objetivo

Evaluar las asociaciones entre indicadores socioeconómicos y el PIB per cápita mediante:

- Análisis exploratorio de datos (EDA).
- Pruebas estadísticas de correlación.
- Regresión lineal múltiple.

## Dataset

Los datos proceden del Banco Mundial e incluyen los siguientes indicadores:

- PIB per cápita.
- Esperanza de vida.
- Uso de internet (% de la población).
- Tasa de desempleo.

El dataset depurado utilizado en el análisis contiene **3.752 observaciones correspondientes a 199 países y territorios**, con registros de diferentes años.

Durante la preparación se excluyeron agregados regionales y económicos para evitar tratarlos como países individuales.

## Proceso

### 1. Limpieza y transformación de datos

- Conversión de datos de formato ancho a largo mediante `melt`.
- Revisión y manejo de valores faltantes.
- Conversión de tipos de datos.
- Integración de múltiples datasets mediante `merge`.
- Exclusión de agregados regionales y económicos.
- Verificación de duplicados por país y año.

### 2. Análisis exploratorio (EDA)

- Análisis de distribuciones, incluyendo la transformación logarítmica del PIB per cápita.
- Visualización de relaciones entre variables.
- Exploración de patrones y valores extremos.
- Análisis de correlaciones entre indicadores socioeconómicos.

### 3. Análisis estadístico

- Cálculo de correlaciones de Pearson.
- Evaluación de valores p.
- Interpretación de la dirección y fuerza de las asociaciones.

### 4. Modelado

Se construyó un modelo de regresión lineal múltiple mediante mínimos cuadrados ordinarios (OLS).

**Variable dependiente:** logaritmo del PIB per cápita (`log_gdp`).

**Variables independientes:**

- Esperanza de vida.
- Uso de internet.
- Desempleo.

## Resultados clave

Las correlaciones de Pearson con el logaritmo del PIB per cápita fueron:

- **Esperanza de vida:** correlación positiva fuerte (r ≈ 0,822).
- **Uso de internet:** correlación positiva (r ≈ 0,661).
- **Desempleo:** correlación negativa muy débil (r ≈ -0,106).

En el modelo de regresión múltiple:

- La esperanza de vida presentó un coeficiente positivo y estadísticamente significativo.
- El uso de internet presentó un coeficiente positivo y estadísticamente significativo.
- El desempleo no presentó un coeficiente estadísticamente significativo (p = 0,829).
- El modelo obtuvo un **R² de 0,719**, equivalente al 71,9 % de la variabilidad observada en `log_gdp` dentro de la muestra.

Estos resultados describen asociaciones estadísticas y no permiten establecer relaciones causales.

## Conclusiones

Los resultados muestran una asociación positiva entre la esperanza de vida y el logaritmo del PIB per cápita, así como entre el uso de internet y dicha variable.

El desempleo presenta una correlación negativa muy débil en el análisis individual y no resulta estadísticamente significativo al considerar simultáneamente las demás variables en el modelo de regresión.

En conjunto, el análisis evidencia relaciones entre los indicadores socioeconómicos seleccionados y los niveles de ingreso, aunque estas asociaciones deben interpretarse dentro de las limitaciones metodológicas del estudio.

## Limitaciones

- No se incluyeron otros indicadores potencialmente relevantes, como educación, desigualdad o inversión.
- El análisis es observacional y no permite establecer causalidad.
- Puede existir multicolinealidad entre las variables independientes.
- Los datos incluyen observaciones repetidas de países a lo largo de diferentes años.
- Las pruebas de correlación y el modelo OLS convencional no consideran explícitamente la dependencia entre observaciones de un mismo país, lo que puede afectar la interpretación de la significación estadística.
- No se modelaron explícitamente los efectos temporales ni las diferencias estructurales entre países.
- El ajuste del modelo se evaluó dentro de la muestra, sin demostrar su capacidad de generalización a datos nuevos.

## Próximos pasos

Como posibles extensiones futuras se consideran:

- Incorporar indicadores adicionales, como educación, desigualdad e inversión.
- Explorar modelos estadísticos que consideren la estructura temporal de los datos.
- Construir visualizaciones interactivas en Power BI o Tableau.
- Realizar análisis comparativos por regiones.

## Herramientas utilizadas

- Python.
- Pandas.
- NumPy.
- Matplotlib y Seaborn.
- SciPy.
- Statsmodels.
- Jupyter Notebook.

## Autor

Alfredo Javier Arnez Valdés

Proyecto desarrollado como parte de la formación y práctica profesional en análisis de datos y estadística aplicada.

Alfredo Javier Arnez Valdés 

Proyecto desarrollado como parte de formación en análisis de datos enfocado en estadística aplicada.

\-\--
