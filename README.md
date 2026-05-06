\# Análisis de Factores Socioeconómicos y su Impacto en el PIB per
cápita

\## Descripción del Proyecto

Este proyecto analiza los factores que influyen en el nivel de vida de
los países, utilizando el PIB per cápita como variable principal.

Se exploran relaciones entre indicadores socioeconómicos como la
esperanza de vida, el acceso a internet y el desempleo, con el objetivo
de identificar cuáles tienen mayor poder explicativo sobre el desarrollo
económico.

\-\--

\## Objetivo

Identificar y evaluar qué variables socioeconómicas están más asociadas
al PIB per cápita mediante:

\* Análisis exploratorio de datos (EDA) \* Pruebas estadísticas \*
Modelos de regresión

\-\--

\## Dataset

Los datos fueron obtenidos del World Bank, incluyendo los siguientes
indicadores:

\* PIB per cápita \* Esperanza de vida \* Uso de internet (% población)
\* Tasa de desempleo

\-\--

\## Proceso

\### 1. Limpieza y transformación de datos

\* Conversión de datos de formato wide a long (\`melt\`) \* Manejo de
valores faltantes \* Conversión de tipos de datos \* Integración de
múltiples datasets mediante \`merge\`

\-\--

\### 2. Análisis Exploratorio (EDA)

\* Análisis de distribuciones (incluyendo transformación logarítmica del
PIB) \* Visualización de relaciones entre variables \* Identificación de
patrones y outliers

\-\--

\### 3. Análisis estadístico

\* Correlación de Pearson entre variables \* Evaluación de significancia
estadística (p-values)

\-\--

\### 4. Modelado

Se construyó un modelo de regresión lineal múltiple para explicar el PIB
per cápita (log-transformado) en función de:

\* Esperanza de vida \* Uso de internet \* Desempleo

\-\--

\## Resultados Clave

\* La \*\*esperanza de vida\*\* mostró la relación más fuerte con el PIB
per cápita (r ≈ 0.82) \* El \*\*uso de internet\*\* presentó una
relación positiva moderada (r ≈ 0.66) \* El \*\*desempleo\*\* mostró una
relación débil (r ≈ -0.10)

En el modelo de regresión:

\* Esperanza de vida y uso de internet fueron \*\*estadísticamente
significativos\*\* \* El desempleo \*\*no resultó significativo\*\* \*
El modelo explicó aproximadamente el \*\*72% de la variabilidad del
PIB\*\* (R² ≈ 0.72)

\-\--

\## Conclusiones

Los resultados sugieren que:

\* Factores estructurales como la salud (esperanza de vida) tienen un
mayor impacto en el desarrollo económico \* El acceso a tecnología
(internet) también contribuye, aunque en menor medida \* Variables más
volátiles como el desempleo tienen menor poder explicativo en este
contexto

\-\--

\## Limitaciones

\* No se incluyeron variables relevantes como educación o inversión \*
El análisis es correlacional (no implica causalidad) \* Posible
multicolinealidad entre variables \* Uso de datos agregados a nivel país
\* No se consideraron dinámicas temporales

\-\--

\## Próximos pasos

\* Incluir variables adicionales (educación, desigualdad, inversión) \*
Aplicar modelos más avanzados \* Construir dashboards interactivos
(Power BI / Tableau) \* Realizar análisis por regiones

\-\--

\## Herramientas utilizadas

\* Python \* Pandas \* NumPy \* Seaborn / Matplotlib \* Statsmodels

\-\--

\## Autor

Alfredo Javier Arnez Valdés 

Proyecto desarrollado como parte de formación en análisis de datos enfocado en estadística aplicada.

\-\--
