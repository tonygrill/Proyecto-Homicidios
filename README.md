 ## Observatorio de Movilidad y Seguridad Vial 

En respuesta a la solicitud del Observatorio de Movilidad y Seguridad Vial, órgano adscrito a la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, se nos encomendó la tarea de analizar datos relacionados con las estadísticas de homicidios en siniestros viales. Este análisis tiene como objetivo principal mejorar la seguridad vial y la calidad de vida ciudadana.

Recibimos un archivo en formato Excel que contiene dos conjuntos de datos: uno referido a los incidentes de siniestros en la Ciudad Autónoma de Buenos Aires y otro referido a las víctimas fatales. Estos datos abarcan el periodo comprendido entre los años 2016 y 2021.

#### Estructura de los Archivos Resultantes

Los archivos resultantes de nuestro análisis están estructurados de la siguiente manera:

- `ETL_homicidios_hechos.ipynb`: Es un archivo en formato Jupyter Notebook que abarca todo el proceso de Extracción, Transformación y Carga (ETL) relacionado con el conjunto de datos de HECHOS.

- `ETL_homicidios_victimas.ipynb`: Contiene todo el proceso de ETL referido al conjunto de datos de VICTIMAS.

- `EDA.ipynb`: Este archivo incluye todo el estudio, gráficos y análisis de nuestro estudio exploratorio de datos.

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


<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
      <th>mean</th>
      <th>std</th>
      <th>min</th>
      <th>25%</th>
      <th>50%</th>
      <th>75%</th>
      <th>max</th>
    </tr>
    <tr>
      <th>AÑO</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2016</th>
      <td>146.0</td>
      <td>1.027397</td>
      <td>0.163800</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2017</th>
      <td>140.0</td>
      <td>1.142857</td>
      <td>0.408038</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2018</th>
      <td>149.0</td>
      <td>1.080537</td>
      <td>0.273040</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2019</th>
      <td>104.0</td>
      <td>1.019231</td>
      <td>0.138000</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2020</th>
      <td>81.0</td>
      <td>1.074074</td>
      <td>0.263523</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>2021</th>
      <td>97.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>

#### Análisis de Distribución Mensual de Homicidios por Año

El siguiente gráfico muestra la distribución mensual por año de los homicidios. Se destaca que el mes de diciembre exhibe la ocurrencia más alta en la distribución. Curiosamente, a pesar de la reducción general en los homicidios debido a la pandemia, diciembre de 2020 presenta una de las tasas más altas en comparación con ese mismo mes en otros años.


![Distribución Mensual de Homicidios](src\distribucion_mensual_homicidios_año.png)

Aquí mostramos de manera gráfica que el mes de diciembre tiene una media mas alta que el resto de los meses

![Media mensual de homicidios](src\prom_mensual_homicidios.png)

El mes de diciembre comprende la media mensual mas alta.

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>0</th>
    </tr>
    <tr>
      <th>MM</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>10.333333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>9.833333</td>
    </tr>
    <tr>
      <th>3</th>
      <td>9.333333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8.666667</td>
    </tr>
    <tr>
      <th>5</th>
      <td>10.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>9.666667</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8.500000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>11.166667</td>
    </tr>
    <tr>
      <th>9</th>
      <td>8.500000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>8.666667</td>
    </tr>
    <tr>
      <th>11</th>
      <td>11.333333</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13.500000</td>
    </tr>
  </tbody>
</table>
</div>


#### Distribución por día del mes

Al desglosar nuestro análisis, observamos a través del siguiente gráfico que el día 20 del mes es el único que presenta una distribución mayor a 30 homicidios.

Este hallazgo nos permite comprender patrones específicos y concentraciones inusuales de incidentes en una fecha particular del mes.


![Distribución por dia del mes](src\prom_dia_del_mes.png)


#### Análisis de Ocurrencia de Siniestros por Hora

Al examinar las horas de mayor ocurrencia de siniestros, notamos que las horas pico son las 5, 6 y 7. Curiosamente, estas no son horas laborables, lo que sugiere que estos eventos pueden ser el resultado de la imprudencia, como conducir bajo la influencia de sustancias o condiciones adversas.

Este patrón horario podría ser fundamental para orientar estrategias de prevención y concienciación, enfocándose en la promoción de conductas seguras durante estas horas específicas del día.


![Distribución hora del dia](src\distribucion_hora_del_dia.png)


#### Análisis de Día de la Semana con respecto a la Hora

Hemos contrastado el día de la semana y la hora en un mapa de calor, revelando un dato notable: a las 6 horas de los sábados y domingos, observamos un incremento en la ocurrencia de siniestros. Esta tendencia sugiere la posibilidad de que este aumento esté relacionado con el consumo de alcohol a altas horas de la noche durante el fin de semana.

La asociación entre la hora específica y el día de la semana puede proporcionar valiosas percepciones para la implementación de medidas preventivas y estrategias de concienciación, especialmente dirigidas a reducir los siniestros relacionados con el consumo de alcohol en esos momentos específicos.

![Día de la semana con hora](src\heatmap_hora_dia_semana.png)


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

![Homicidios por tipo de calle](src\homicidios_tipo_calle.png)

#### Analisis por Comuna

La tabla presenta el porcentaje de homicidios por comuna, destacando que la Comuna 1 tiene el porcentaje más alto con un 12.97%, seguida por la Comuna 4 con un 11.02%. Esto nos permite focalizar esfuerzos de seguridad y prevención en las comunas con mayores porcentajes de homicidios.

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>COMUNA</th>
      <th>Porcentaje</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0.27</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>12.97</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>3.48</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>6.41</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>11.01</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5</td>
      <td>3.06</td>
    </tr>
    <tr>
      <th>6</th>
      <td>6</td>
      <td>3.06</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>8.64</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8</td>
      <td>9.34</td>
    </tr>
    <tr>
      <th>9</th>
      <td>9</td>
      <td>10.46</td>
    </tr>
    <tr>
      <th>10</th>
      <td>10</td>
      <td>4.18</td>
    </tr>
    <tr>
      <th>11</th>
      <td>11</td>
      <td>4.60</td>
    </tr>
    <tr>
      <th>12</th>
      <td>12</td>
      <td>5.43</td>
    </tr>
    <tr>
      <th>13</th>
      <td>13</td>
      <td>5.57</td>
    </tr>
    <tr>
      <th>14</th>
      <td>14</td>
      <td>5.16</td>
    </tr>
    <tr>
      <th>15</th>
      <td>15</td>
      <td>6.27</td>
    </tr>
  </tbody>
</table>
</div>

#### Relación entre Tipo de Calle y Comuna: Homicidios

En el siguiente gráfico, exploramos la relación entre el tipo de calle y la comuna en términos de homicidios. La visualización confirma que las Avenidas, especialmente en la Comuna 1, concentran una parte significativa de los homicidios.

Este hallazgo refuerza la importancia de implementar medidas específicas de seguridad y prevención en las Avenidas de la Comuna 1, con el objetivo de reducir la incidencia de homicidios en estas áreas específicas.

![Comuna y tipo de calle](src\homicidios_comuna_tipo_calle.png)

#### Arterias viales con mayor incidencia.

La tabla presenta el top 10 de las arterias viales con mayor cantidad de siniestros. La Avenida Gral. Paz encabeza la lista con 61 siniestros, seguida por la Avenida Rivadavia con 20 y la Avenida del Libertador con 19. Este análisis es crucial para priorizar intervenciones y medidas preventivas específicas en estas arterias viales con mayores incidencias de siniestros.

<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Calle</th>
      <th>Cantidad</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>PAZ, GRAL. AV.</td>
      <td>61</td>
    </tr>
    <tr>
      <th>1</th>
      <td>RIVADAVIA AV.</td>
      <td>20</td>
    </tr>
    <tr>
      <th>2</th>
      <td>DEL LIBERTADOR AV.</td>
      <td>19</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AUTOPISTA 1 SUR PRESIDENTE ARTURO FRONDIZI</td>
      <td>14</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AUTOPISTA PERITO MORENO</td>
      <td>13</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ALBERDI, JUAN BAUTISTA AV.</td>
      <td>13</td>
    </tr>
    <tr>
      <th>6</th>
      <td>AUTOPISTA 25 DE MAYO</td>
      <td>12</td>
    </tr>
    <tr>
      <th>7</th>
      <td>SAN MARTIN AV.</td>
      <td>11</td>
    </tr>
    <tr>
      <th>8</th>
      <td>CORRIENTES AV.</td>
      <td>11</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CORDOBA AV.</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
</div>


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

![Homicidios por comuna y año](src\heatmap_hom_comuna_año.png)

#### Victimas según su genero

El genero masculino presenta un indice de mortalidad en siniestros viales del 76,4%

![victimas por genero](src\genero.png)

####  Relación entre COMUNA y SEXO

Realizamos una tabla de frecuencia relacionando el género con la comuna. Observamos que las víctimas masculinas tienen su pico en la comuna 1, mientras que las víctimas femeninas fueron más numerosas en la comuna 9.

![comuna sexo](src\comuna_sexo.png)

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

![roles genero](src\roles_genero.png)


#### Muertes el mismo día

El gráfico de torta siguiente revela que un significativo 78,8% de las víctimas perdieron la vida el mismo día del accidente, en marcado contraste con el 21,2% de los casos en los que la muerte ocurrió en fechas posteriores. Este hallazgo resalta la agudeza de las consecuencias mortales en la mayoría de los incidentes, enfatizando la importancia de medidas inmediatas y eficaces en términos de atención médica y prevención de accidentes viales.

![muertes](src\muertes_mismo_dia.png)

#### Relación entre muertes el mismo dia y genero


En el gráfico que sigue, se examina la relación entre las muertes ocurridas el mismo día y el género de las víctimas. Los datos muestran que el 80.47% de las mujeres fallecen el mismo día del accidente, mientras que en el caso de los hombres, esta cifra es ligeramente menor, alcanzando un 78.28%. Estas estadísticas revelan una tendencia común entre ambos géneros en cuanto a la rapidez de las consecuencias mortales tras un accidente vial.

![mertes y genero](src\genero_muerte_mismo_dia.png)




#### Conclusión: Análisis de Homicidios en Accidentes de Tránsito en Buenos Aires

A lo largo de este análisis exhaustivo de los homicidios relacionados con accidentes de tránsito en Buenos Aires, hemos identificado patrones significativos y tendencias que ofrecen una visión más clara de la problemática. Algunos hallazgos clave incluyen:

Participantes Predominantes: Los participantes más afectados son peatones y conductores de motocicletas, siendo estos últimos los más propensos a sufrir consecuencias mortales en accidentes de tránsito.

Ubicaciones Críticas: Se han identificado áreas críticas con una mayor incidencia de homicidios, destacando cruces de avenidas y ciertas comunas, especialmente la Comuna 1.

Incidencia por Género: La mayoría de las víctimas son hombres, y se observa una distribución de roles diferente entre los géneros, donde los hombres son principalmente conductores y las mujeres son más propensas a ser peatones.

Tiempo de Respuesta: La mayoría de las víctimas fallecen el mismo día del accidente, destacando la rapidez de las consecuencias mortales en estos incidentes.

Recomendaciones para Futuras Investigaciones: Se sugiere incluir más detalles sobre la causa del siniestro y explorar regulaciones específicas para mejorar la seguridad en áreas críticas.

Este análisis proporciona información valiosa para las autoridades locales, permitiéndoles tomar medidas preventivas y desarrollar estrategias efectivas para reducir la incidencia de homicidios en accidentes de tránsito. La combinación de datos numéricos, gráficos visuales y análisis detallados ofrece una comprensión completa de la situación, allanando el camino para futuras investigaciones y acciones proactivas.
=======
# Proyecto-Homicidios
>>>>>>> 43b6b1f4ee270b8565b4cd9e2913431e9f6b92f5
