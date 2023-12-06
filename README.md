 ## Observatorio de Movilidad y Seguridad Vial 

En respuesta a la solicitud del Observatorio de Movilidad y Seguridad Vial, órgano adscrito a la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, se nos encomendó la tarea de analizar datos relacionados con las estadísticas de homicidios en siniestros viales. Este análisis tiene como objetivo principal mejorar la seguridad vial y la calidad de vida ciudadana.

Recibimos un archivo en formato Excel que contiene dos conjuntos de datos: uno referido a los incidentes de siniestros en la Ciudad Autónoma de Buenos Aires y otro referido a las víctimas fatales. Estos datos abarcan el periodo comprendido entre los años 2016 y 2021.

#### Estructura de los Archivos Resultantes

Los archivos resultantes de nuestro análisis están estructurados de la siguiente manera:

- `homicidios.xlsx`: Es el dataset de origen facilitado por el organismo.

- `ETL_homicidios_hechos.ipynb`: Es un archivo en formato Jupyter Notebook que abarca todo el proceso de Extracción, Transformación y Carga (ETL) relacionado con el conjunto de datos de HECHOS.

- `ETL_homicidios_victimas.ipynb`: Contiene todo el proceso de ETL referido al conjunto de datos de VICTIMAS.

- `EDA.ipynb`: Este archivo incluye todo el estudio, gráficos y análisis de nuestro estudio exploratorio de datos.

- `dataset.csv`: Este es el archivo resultande del EDA, con este dataset trabajaremos en nuestro Dashboard.

- `carpeta src`: Esta carpeta contiene todas las imagenes adjuntas al README.

- `mapa_homicidios.html`: Archivo HTML con las hubicaciones de los siniestros.

A continuación, presentaremos nuestros análisis y hallazgos:

#### Análisis de Víctimas Mortales por Accidente

Comenzaremos analizando el número de víctimas mortales por accidente. Se observa que el 5,72% de los siniestros con víctimas fatales involucran más de una víctima. Además, cabe destacar que el año 2017 fue el único en el periodo analizado con más de 2 víctimas fatales en un mismo incidente.

La tabla presenta un resumen detallado de las estadísticas relacionadas con los incidentes ocurridos en cada año, específicamente en lo que respecta a las características del dataset. Aquí se destacan algunos puntos clave:

Count: La cantidad total de eventos registrados para cada año.
Mean: El promedio de la variable analizada indica la tendencia central de los datos.
Std (Desviación Estándar): Mide la dispersión de los datos, proporcionando una perspectiva de la variabilidad.
Min: El valor mínimo observado en el año.
25%, 50%, 75% (Cuartiles): Estos percentiles indican la distribución de los datos, mostrando los valores por debajo de los cuales cae un porcentaje específico de observaciones.
Max: El valor máximo registrado en el año.
Esta información proporciona una visión integral de la variabilidad y distribución de los datos a lo largo de los años, facilitando la identificación de patrones o tendencias significativas en el estudio.
Uno de lso datos a considerar es que la reducción de fatalidad entre en 2018 y 2020 es del 54%, 


| AÑO  | count | mean     | std      | min | 25% | 50% | 75% | max |
|------|-------|----------|----------|-----|-----|-----|-----|-----|
| 2016 | 146   | 1.027397 | 0.163800 | 1   | 1   | 1   | 1   | 2   |
| 2017 | 140   | 1.142857 | 0.408038 | 1   | 1   | 1   | 1   | 3   |
| 2018 | 149   | 1.080537 | 0.273040 | 1   | 1   | 1   | 1   | 2   |
| 2019 | 104   | 1.019231 | 0.138000 | 1   | 1   | 1   | 1   | 2   |
| 2020 | 81    | 1.074074 | 0.263523 | 1   | 1   | 1   | 1   | 2   |
| 2021 | 97    | 1.000000 | 0.000000 | 1   | 1   | 1   | 1   | 1   |


#### Análisis de Distribución Mensual de Homicidios por Año

El siguiente gráfico muestra la distribución mensual por año de los homicidios. Se destaca que el mes de diciembre exhibe la ocurrencia más alta en la distribución. Curiosamente, a pesar de la reducción general en los homicidios debido a la pandemia, diciembre de 2020 presenta una de las tasas más altas en comparación con ese mismo mes en otros años.

<p align="center">
<img src ="src\distribucion_mensual_homicidios_año.png">
<p>

Aquí mostramos de manera gráfica que el mes de diciembre tiene una media mas alta que el resto de los meses

<p align="center">
<img src ="src\prom_mensual_homicidios.png">
<p>

El mes de diciembre comprende la media mensual mas alta.


| MM | 0      |
|----|--------|
| 1  | 10.33  |
| 2  | 9.83   |
| 3  | 9.33   |
| 4  | 8.66   |
| 5  | 10.00  |
| 6  | 9.66   |
| 7  | 8.50   |
| 8  | 11.16  |
| 9  | 8.50   |
| 10 | 8.66   |
| 11 | 11.33  |
| 12 | 13.50  |


#### Distribución por día del mes

Al desglosar nuestro análisis, observamos a través del siguiente gráfico que el día 20 del mes es el único que presenta una distribución mayor a 30 homicidios.

Este hallazgo nos permite comprender patrones específicos y concentraciones inusuales de incidentes en una fecha particular del mes.

<p align="center">
<img src ="src\prom_dia_del_mes.png">
<p>



#### Análisis de Ocurrencia de Siniestros por Hora

Al examinar las horas de mayor ocurrencia de siniestros, notamos que las horas pico son las 5, 6 y 7. Curiosamente, estas no son horas laborables, lo que sugiere que estos eventos pueden ser el resultado de la imprudencia, como conducir bajo la influencia de sustancias o condiciones adversas.

Este patrón horario podría ser fundamental para orientar estrategias de prevención y concienciación, enfocándose en la promoción de conductas seguras durante estas horas específicas del día.

<p align="center">
<img src ="src\distribucion_hora_del_dia.png">
<p>


#### Análisis de Día de la Semana con respecto a la Hora

Hemos contrastado el día de la semana y la hora en un mapa de calor, revelando un dato notable: a las 6 horas de los sábados y domingos, observamos un incremento en la ocurrencia de siniestros. Esta tendencia sugiere la posibilidad de que este aumento esté relacionado con el consumo de alcohol a altas horas de la noche durante el fin de semana.

La asociación entre la hora específica y el día de la semana puede proporcionar valiosas percepciones para la implementación de medidas preventivas y estrategias de concienciación, especialmente dirigidas a reducir los siniestros relacionados con el consumo de alcohol en esos momentos específicos.

<p align="center">
<img src ="src\heatmap_hora_dia_semana.png">
<p>


#### Análisis del Tipo de Arteria Vial y Número de Siniestros

El siguiente conteo revela que el número de siniestros en avenidas es considerablemente mayor en comparación con otros tipos de arterias viales:

- **Avenida:** 442 siniestros
- **Calle:** 138 siniestros
- **Gral Paz:** 69 siniestros
- **Autopista:** 68 siniestros

Este hallazgo destaca la importancia de considerar el tipo de vía al desarrollar estrategias de seguridad vial y medidas preventivas, especialmente enfocándose en la mitigación de siniestros en avenidas.

Para complementar lo dicho anteriormente, el siguiente gráfico de torta ilustra la distribución de homicidios según el tipo de arteria vial. Los resultados son los siguientes:

- **Avenida:** 61.6%
- **Calle:** 19.2%
- **Gral Paz:** [Porcentaje correspondiente]
- **Autopista:** [Porcentaje correspondiente]

Este gráfico refuerza la observación de que las avenidas presentan un porcentaje considerablemente alto de homicidios en comparación con otros tipos de arterias viales. Esta información puede ser crucial al desarrollar estrategias específicas para mejorar la seguridad en estas áreas de la ciudad.

<p align="center">
<img src ="src\homicidios_tipo_calle.png">
<p>

#### Analisis por Comuna

La tabla presenta el porcentaje de homicidios por comuna, destacando que la Comuna 1 tiene el porcentaje más alto con un 12.97%, seguida por la Comuna 4 con un 11.02%. Esto nos permite focalizar esfuerzos de seguridad y prevención en las comunas con mayores porcentajes de homicidios.

| COMUNA | Porcentaje |
|--------|------------|
| 0      | 0.27       |
| 1      | 12.97      |
| 2      | 3.48       |
| 3      | 6.41       |
| 4      | 11.01      |
| 5      | 3.06       |
| 6      | 3.06       |
| 7      | 8.64       |
| 8      | 9.34       |
| 9      | 10.46      |
| 10     | 4.18       |
| 11     | 4.60       |
| 12     | 5.43       |
| 13     | 5.57       |
| 14     | 5.16       |
| 15     | 6.27       |

#### Relación entre Tipo de Calle y Comuna: Homicidios

En el siguiente gráfico, exploramos la relación entre el tipo de calle y la comuna en términos de homicidios. La visualización confirma que las Avenidas, especialmente en la Comuna 1, concentran una parte significativa de los homicidios.

Este hallazgo refuerza la importancia de implementar medidas específicas de seguridad y prevención en las Avenidas de la Comuna 1, con el objetivo de reducir la incidencia de homicidios en estas áreas específicas.

<p align="center">
<img src ="src\homicidios_comuna_tipo_calle.png">
<p>

#### Arterias viales con mayor incidencia.

La tabla presenta el top 10 de las arterias viales con mayor cantidad de siniestros. La Avenida Gral. Paz encabeza la lista con 61 siniestros, seguida por la Avenida Rivadavia con 20 y la Avenida del Libertador con 19. Este análisis es crucial para priorizar intervenciones y medidas preventivas específicas en estas arterias viales con mayores incidencias de siniestros.


| Calle                                     | Cantidad |
|-------------------------------------------|----------|
| PAZ, GRAL. AV.                            | 61       |
| RIVADAVIA AV.                             | 20       |
| DEL LIBERTADOR AV.                        | 19       |
| AUTOPISTA 1 SUR PRESIDENTE ARTURO FRONDIZI | 14       |
| AUTOPISTA PERITO MORENO                   | 13       |
| ALBERDI, JUAN BAUTISTA AV.                | 13       |
| AUTOPISTA 25 DE MAYO                      | 12       |
| SAN MARTIN AV.                            | 11       |
| CORRIENTES AV.                            | 11       |
| CORDOBA AV.                               | 10       |


#### Frecuencia de Homicidios en Función de la Dirección

El análisis de las direcciones normalizadas más comunes muestra que ciertos puntos de la ciudad tienen una mayor incidencia de homicidios. Aquí algunos hallazgos clave:

27 DE FEBRERO AV. y ESCALADA AV. (5 homicidios): Este cruce de avenidas parece ser un lugar de mayor riesgo, con una concentración significativa de incidentes.

PAZ, GRAL. AV. y DEL LIBERTADOR AV. (4 homicidios): Este cruce de dos avenidas importantes también muestra una incidencia considerable de homicidios.

ALCORTA, AMANCIO AV. y BONAVENA, OSCAR NATALIO (3 homicidios): Otro cruce que registra una cantidad significativa de incidentes.

INDEPENDENCIA AV. y CEVALLOS, VIRREY (3 homicidios): Una intersección en la que se han producido múltiples homicidios.

DEL LIBERTADOR AV. y RAMOS MEJIA, JOSE MARIA, DR. AV. (3 homicidios): Otro cruce de avenidas importantes con una presencia notoria en el recuento.

Estos hallazgos sugieren que ciertos puntos específicos de la ciudad pueden requerir una atención especial en términos de seguridad pública y medidas preventivas. Además, podría ser valioso explorar más detalles sobre la naturaleza de estos incidentes para comprender mejor las circunstancias y tomar medidas adecuadas para abordar el problema.


| Dirección Normalizada                                     | Count |
|------------------------------------------------------------|-------|
| 27 DE FEBRERO AV. y ESCALADA AV.                           | 5     |
| PAZ, GRAL. AV. y DEL LIBERTADOR AV.                        | 4     |
| PAZ, GRAL. AV. y BALBIN, RICARDO, DR. AV.                  | 4     |
| ALCORTA, AMANCIO AV. y BONAVENA, OSCAR NATALIO             | 3     |
| ACHAVAL RODRIGUEZ, T., DR. AV. y VILLAFLOR, AZUCENA        | 3     |
| INDEPENDENCIA AV. y CEVALLOS, VIRREY                       | 3     |
| DEL LIBERTADOR AV. y RAMOS MEJIA, JOSE MARIA, DR. AV.      | 3     |
| PAZ, GRAL. AV. y DE LOS CORRALES AV.                       | 3     |
| CASTILLO, RAMON S., PRES. AV. y CALLE 12 (NO OFICIAL)      | 3     |
| SALGUERO, JERONIMO y RIVADAVIA AV.                         | 2     |
| RABANAL, FRANCISCO, INTENDENTE AV. y SAENZ AV.             | 2     |
| DEL LIBERTADOR AV. 4100                                    | 2     |
| PAZ, GRAL. AV. y DONADO                                    | 2     |
| AUTOPISTA 25 DE MAYO y BOEDO AV.                           | 2     |
| LAS HERAS GENERAL AV. y DIAZ, CNEL. AV.                    | 2     |
| RIESTRA AV. y CAÑADA DE GOMEZ                              | 2     |
| AUTOPISTA PERITO MORENO y BARRAGAN                         | 2     |
| AUTOPISTA 1 SUR PRESIDENTE ARTURO FRONDIZI y CASEROS AV.   | 2     |
| OLIVERA AV. y FALCON, RAMON L.,CNEL.                       | 2     |


#### Frecuencia de Homicidios

Hemos creado un mapa de calor que representa la distribución de homicidios según el año y la comuna. Este mapa confirma las tendencias observadas en los datos numéricos recientemente presentados. Es notable el aumento de incidentes en la comuna 1, con especial énfasis en los años 2016, 2017 y 2018 en comparación con otras categorías. Este análisis visual resalta la importancia de estas áreas y períodos en particular en relación con los homicidios registrados.

<p align="center">
<img src ="src\heatmap_hom_comuna_año.png">
<p>

#### Victimas según su genero

El genero masculino presenta un indice de mortalidad en siniestros viales del 76,4%

<p align="center">
<img src ="src\genero.png">
<p>


####  Relación entre COMUNA y SEXO

Realizamos una tabla de frecuencia relacionando el género con la comuna. Observamos que las víctimas masculinas tienen su pico en la comuna 1, mientras que las víctimas femeninas fueron más numerosas en la comuna 9.

<p align="center">
<img src ="src\comuna_sexo.png">
<p>


#### Relción entre tipo de calle y sexo


En los datos ajustados y analizados recientemente sobre la variable "EDAD" en relación con el "TIPO_DE_CALLE" y el "SEXO" de las víctimas, podemos destacar varias conclusiones significativas:

Distribución por Tipo de Calle:

Las edades de las víctimas varían considerablemente según el tipo de calle.
En general, las avenidas tienen una mayor variabilidad en las edades, mientras que en las calles la variabilidad es moderada.
Diferencias entre Géneros:

En todos los tipos de calles, las mujeres tienden a tener edades promedio más altas en comparación con los hombres.
La variabilidad en las edades de las mujeres es más pronunciada, especialmente en avenidas y calles.
Género y Tipo de Calle:

Las mujeres que son víctimas en avenidas tienen un promedio de edad más alto (50.68 años), mientras que las mujeres en calles tienen el promedio más alto en comparación con otros tipos de calle.
Los hombres que son víctimas en avenidas tienen un promedio de edad más alto (40.77 años), mientras que los hombres en autopistas tienen el promedio más alto entre los tipos de calle.
Generalidad en las Calles:

Independientemente del tipo de calle, se observa que las mujeres tienden a tener edades más altas en comparación con los hombres.


#### Distribución de roles por genero

Este gráfico de barras ilustra la distribución de roles de las víctimas según su género. Se destaca que la mayoría de las víctimas masculinas desempeñaban el rol de conductor, mientras que en el caso de las mujeres, predominaba el rol de peatón. Esta disparidad en la distribución resalta la importancia de abordar medidas de seguridad específicas para conductores y peatones, considerando las diferencias de género y los patrones de incidencia en roles específicos.

<p align="center">
<img src ="src\roles_genero.png">
<p>



#### Muertes el mismo día

El gráfico de torta siguiente revela que un significativo 78,8% de las víctimas perdieron la vida el mismo día del accidente, en marcado contraste con el 21,2% de los casos en los que la muerte ocurrió en fechas posteriores. Este hallazgo resalta la agudeza de las consecuencias mortales en la mayoría de los incidentes, enfatizando la importancia de medidas inmediatas y eficaces en términos de atención médica y prevención de accidentes viales.

<p align="center">
<img src ="src\muertes_mismo_dia.png">
<p>


#### Relación entre muertes el mismo dia y genero


En el gráfico que sigue, se examina la relación entre las muertes ocurridas el mismo día y el género de las víctimas. Los datos muestran que el 80.47% de las mujeres fallecen el mismo día del accidente, mientras que en el caso de los hombres, esta cifra es ligeramente menor, alcanzando un 78.28%. Estas estadísticas revelan una tendencia común entre ambos géneros en cuanto a la rapidez de las consecuencias mortales tras un accidente vial.

<p align="center">
<img src ="src\genero_muerte_mismo_dia.png">
<p>

Hemos utilizado la biblioteca Folium para generar un mapa de geolocalización que permite visualizar de manera precisa la ubicación de los siniestros. El archivo correspondiente se encuentra adjunto en el repositorio

#### Conclusiones

A lo largo de este análisis exhaustivo de los homicidios relacionados con accidentes de tránsito en Buenos Aires, hemos identificado patrones significativos y tendencias que ofrecen una visión más clara de la problemática. Algunos hallazgos clave incluyen:

Participantes Predominantes: Los participantes más afectados son peatones y conductores de motocicletas, siendo estos últimos los más propensos a sufrir consecuencias mortales en accidentes de tránsito.

Ubicaciones Críticas: Se han identificado áreas críticas con una mayor incidencia de homicidios, destacando cruces de avenidas y ciertas comunas, especialmente la Comuna 1.

Incidencia por Género: La mayoría de las víctimas son hombres, y se observa una distribución de roles diferente entre los géneros, donde los hombres son principalmente conductores y las mujeres son más propensas a ser peatones.

Tiempo de Respuesta: La mayoría de las víctimas fallecen el mismo día del accidente, destacando la rapidez de las consecuencias mortales en estos incidentes.

Recomendaciones para Futuras Investigaciones: Se sugiere incluir más detalles sobre la causa del siniestro y explorar regulaciones específicas para mejorar la seguridad en áreas críticas.

Este análisis proporciona información valiosa para las autoridades locales, permitiéndoles tomar medidas preventivas y desarrollar estrategias efectivas para reducir la incidencia de homicidios en accidentes de tránsito. La combinación de datos numéricos, gráficos visuales y análisis detallados ofrece una comprensión completa de la situación, allanando el camino para futuras investigaciones y acciones proactivas.