# AMUNDI-MSCI-World-Investment-Fund-EDA

**Objetivo del proyecto**

Este notebook realiza un Análisis Exploratorio de Datos (EDA) sobre el fondo Amundi MSCI World (ISIN LU0996182563), que replica el comportamiento del índice global MSCI World.

El propósito es entender la evolución histórica del precio, su distribución, tendencia, volatilidad y estructura temporal mediante técnicas estadísticas y visuales.

**Fuente de datos**

Los datos históricos se obtienen desde Yahoo Finance, utilizando la librería yfinance de Python para descargar precios de cierre ajustados en un rango temporal definido.

**Proceso analítico**

El flujo del notebook sigue una estructura típica de análisis financiero de series temporales:

**Extracción de datos**

-Descarga de precios históricos del fondo Amundi MSCI World

-Selección de rango de fechas para el análisis

**Carga y preparación**

-Importación a pandas DataFrame

-Selección de variables relevantes

## **Análisis Exploratorio (EDA)**

**Estadísticos descriptivos**

Se calculan métricas básicas:

-Media

-Mediana

-Desviación estándar

-Valores mínimos y máximos



**Distribución de precios**

Se analizan histogramas y curvas de densidad.

La distribución no es normal (no sigue una campana de Gauss). Presenta asimetría y concentración de observaciones en rangos de precios recientes más altos, reflejando crecimiento a largo plazo.

**Detección de valores atípicos**

Mediante boxplots se identifican posibles outliers.

Los valores extremos corresponden a periodos de alta volatilidad de mercado (crisis, correcciones), no a errores de datos.

**Análisis de tendencia (Medias móviles)**

Se calcula una media móvil (ej. 30 días) para suavizar la serie.

Se observa una tendencia alcista estructural a largo plazo

El suavizado permite distinguir ciclos de mercado frente al ruido diario

**Autocorrelación (Lag Plot)**

Se compara el precio de un día con el del día anterior.

Existe alta autocorrelación positiva, típica en series financieras con fuerte dependencia temporal. El precio pasado tiene poder explicativo sobre el precio inmediato siguiente.

**Descomposición de la serie temporal**

Se descompone la serie en:

Tendencia

-Estacionalidad

-Residuo

-Hallazgos:

La tendencia domina el comportamiento del activo

La estacionalidad es débil o poco relevante (esperable en fondos globales diversificados)

Los residuos reflejan shocks de mercado y eventos macroeconómicos

**Tecnologías utilizadas**

-Python

-pandas

-yfinance

-matplotlib / seaborn

-statsmodels (descomposición de series)


## **Conclusiones generales**

El fondo muestra un crecimiento de largo plazo, interrumpido por caídas asociadas a ciclos bajistas globales.

La volatilidad es consistente con un ETF/fondo de renta variable mundial.

La serie presenta:

No normalidad en la distribución

Dependencia temporal significativa

Tendencia clara y dominante

No se detectan anomalías estructurales en los datos, solo fluctuaciones propias del mercado.


