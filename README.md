<h1 align=center> **PROYECTO INDIVIDUAL Nº3**</h1>
<h1 align=center> **DATA ANALYST** </h1>

<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

## **Introducción**

Este proyecto consiste en la elaboración de un _"dashboard"_ para analizar los datos suministrados por [Enancom][1], de la penetración del internet en las diferentes provincias de Argentina, tomando como base la media de penetración por hogares, la velocidad de descarga y las tecnologías utilizadas para su acceso.

## Exploración de los datos

Se realiza la descarga de los [datos abiertos de acceso a internet](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/ "datos abiertos") en formato "csv" y se etiquetan los mismos. Posteriormente, se verifica el contenido de los dataset por medio de la libreria de python [Pandas Profiling](https://pypi.org/project/pandas-profiling/ "Pandas Profiling"),análisis que es exportado en formato "html" para su posterior consulta, como se puede evidenciar en la carpeta "Reportes_EDA".

Una vez realizado los pasos previos se determina que los dataset a utilizar seran los contenidos en las tablas 2, 7, 10, 14 y 15 teniendo en cuenta la utilidad persivida de la información suministrada por estos.

El proceso de ETL necesario para la realización de los análisis se realizar con la herramienta de [Power Querry](https://support.microsoft.com/es-es/office/acerca-de-power-query-en-excel-7104fbee-9e62-4cb9-a02e-5bfb1a6c536a "Power Querry") presente en Power BI.

## KPI

El análisis tomará como base 4 [KPI](https://es.wikipedia.org/wiki/Indicador_clave_de_rendimiento "KPI"), con los cuales se va a desarrollar el _history telling_ de los datos que se analaizan.

Los KPI son los siguientes:

- **Recuento de Penetración promedio para 2022:** Tomamos como base la penetración de cada uno de las provincias en el último trimestre (trimestre 1 de 2022), para medir a nivel promedio de cuantos de cada 100 hogares argentinos cuentan con internet fijo.

- **Media de bajada y Media Sur América:** comparamos la velocidad promedio de bajada de en [Mbps](https://es.wikipedia.org/wiki/Megabit_por_segundo "Mbps") respecto al [promedio de Sur América](https://www.cable.co.uk/broadband/speed/worldwide-speed-league/#regions "promedio de Sur América") .

- **Fibra vs Conexiones en 2022:** comparamos el número total de conexiones de internet por medio de fibra optica respecto al total de conexiones de internet con las que cuenta Argentina.

- **Conexiones menores que 30 Mbps del Total de conexiones:** comparamos el número total de conexiones de internet que cuentan con una velocidad de descarga menor a 30Mbps, teniendo en cuenta que la media de [Sur América es de 29,24 Mbps](https://www.cable.co.uk/broadband/speed/worldwide-speed-league/#regions "Sur América es de 29,24 Mbps"), respecto al total de conexiones del país.

## Que encontrarás en este repositorio

1. **Dataset**: contiene los archivos que se descargaron de la [fuente utilizada para el proyecto](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/ "fuente utilizada para el proyecto").
2. **Reportes_EDA**: contiene los archivos html resultados del análisis exploratorio de datos
3. **Dashboard Mejorado.pbix:** Es el archivo de Power BI donde se encuentra el Dashboard.
4. **EDA.ipynb:** Es el archivo donde se realizo todo el proceso exploratorio y la exportación de los resportes del EDA.

## Conclusiones.

- Argentina aún cuenta con regiones que se encuentran altamente rezagadas respecto al resto del país en cuento a penetración de interntet.
- En muchas provincias del pais la velocidad del internet está muy por debajo de la media nacional, con velocidades de hasta 11 Mbps.
- Aunque las conexiones de internet de fibra optica han crecido, el rey de las conexiones es el [cablemodem](https://es.wikipedia.org/wiki/Cablem%C3%B3dem "cablemodem"), el cual limita la velocidad maxima de descarga.
- Todas las provincias (13) que se encuentran con una penetración menor a la Penetración promedio para 2022 tambien cuentan con velocidades de navegación por debajo de la media nacional (5).
