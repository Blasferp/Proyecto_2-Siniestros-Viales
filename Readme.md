<h1 align='center'>
 <b>PROYECTO INDIVIDUAL Nº2</b>
</h1>

# <h1 align="center">**`Siniestros viales`**</h1>

<p align='center'>
<img src ="Imagen\Siniestros Viales.png" width="11000px" height="450px">
<p>

# Índice

1. [Introduccion](#introduccion)
2. [Contexto y Rol a Desarrollar](#contexto-y-rol-a-desarrollar)
3. [Fuente de Datos](#fuente-de-datos)
4. [ETL y EDA](#etl-y-eda)
5. [KPIs](#KPIs)
6. [Conclusiones](#Conclusiones)
7. [Medidas](#Medidas)
8. [Tecnologías Utilizadas](#tecnologías-utilizadas)


## **Introduccion:**
Los siniestros viales representan un desafío global en términos de seguridad pública y salud, dejan 1,3 millones de personas muertas y 50 millones más heridas de gravedad en el mundo cada año. Los accidentes de tránsito son una de las principales causas de muerte en todos los grupos etarios.Es una de las principales causas de muertes en Argentina segun informes del ``Sistema Nacional de Información Criminal (SNIC)``. Estos pueden tener diversas causas tales como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Este proyecto tiene como objetivo realizar un análisis detallado de las causas de los siniestros viales en Ciudad Autonoma de Buenos Aires (CABA) entre los años 2016-2022. Al entender las causas subyacentes, podemos desarrollar estrategias efectivas para mejorar la seguridad vial y reducir las consecuencias devastadoras de estos incidentes.


## **Contexto y Rol a desarrollar**

Los Siniestro vial o siniestro de circulación con víctimas son cualquier hecho de tránsito con implicación de al menos un vehículo en movimiento, que tenga lugar en una vía pública o en una vía privada a la que la población tenga derecho de acceso, y que tenga como
consecuencia al menos una persona herida o muerta. Se incluyen: las colisiones entre vehículos; entre vehículos y peatones; entre vehículos y animales u obstáculos fijos; los siniestros viales con la intervención de sólo un vehículo; y las colisiones entre vehículos
y trenes. Las colisiones múltiples se contabilizan como un solo hecho de tránsito si las colisiones se suceden en un periodo de tiempo muy corto.

Se excluyen los hechos de tránsito con sólo daños materiales.

Se excluyen los actos terroristas

En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, esta sigue siendo la principal causa de muertes violentas en el país. Los informes del Sistema Nacional de Información Criminal (SNIC), del Ministerio de Seguridad de la Nación, revelan que entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Estas cifras equivalen a 11 personas por día que resultaron víctimas fatales por accidentes de tránsito.

Algunas de las principales causas de muertes en hechos de tránsito señaladas por la entidad, continúan siendo el exceso de velocidad, las bebidas alcohólicas y la falta de uso del cinturón de seguridad, entre otras. 

Buenos Aires es la capital y ciudad más poblada de la República Argentina. Sus nombres oficiales son Ciudad de Buenos Aires o Ciudad Autónoma de Buenos Aires (CABA). Oficialmente la ciudad se encuentra dividida en 15 comunas que agrupan a 48 barrios.
La población de la ciudad, según el Censo de 2022([**Indec**](https://www.indec.gob.ar/ftp/cuadros/poblacion/cnphv2022_resultados_provisionales.pdf)), es de 3 120 612 habitantes. La superficie de la Ciudad es algo superior a los 200 km2 y su perímetro, 60 km.

El Observatorio de Movilidad y Seguridad Vial (OMSV), centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires, nos solicita la elaboración de un proyecto de análisis de datos, con el fin de generar información que les permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales

## **Fuente de Datos**
El dataset sobre homicidios en siniestros viales acaecidos en la Ciudad de Buenos Aires durante el periodo 2016-2021, se encuentra en formato xlsx y contiene dos hojas llamadas: **`hechos`** y **`víctimas`**. Asimismo, observarán que incluye otras dos hojas adicionales de diccionarios de datos. 

Se agrega un Anexo que contine 2 archivos de tipo .PDF , que continen las definiciones para una mejor compresion de los datos.
Los datos se encuentran en el siguiente [**Diccionarios Homicidios**](Anexos\NOTAS_HOMICIDIOS_SINIESTRO_VIAL.pdf) y [**Diccionarios Lesiones**](Anexos\NOTAS_LESIONES_SINIESTRO_VIAL.pdf)

Los datos utilizados en este proyecto provienen del sitio web oficial de [**Ciudad de Buenos Aires**](https://www.buenosaires.gob.ar/datosabiertos).

## **ETL Y EDA**

`ETL` (Extract, Transform, Load)

Se realizó un proceso de extracción, transformación y carga de los datos (ETL) y un análisis exploratorio exhaustivo primario (EDA), primero para los datos de "HECHOS" y luego para los de "VÍCTIMAS", donde se estandarizaron nombres de las variables, se analizaron nulos y duplicados de los registros, se eliminaron columnas redundantes se imputaron valores faltantes, entre otras tareas. 

Los procesos realizados en el ETL se encuentran en los archivo [**Sineistros_Viales**](Sineistros_Viales.ipynb), [**Victimas_Homicidios**](Victimas_Homicidios.ipynb), [**Hechos_Homicidios**](Hechos_Homicidios.ipynb).

`EDA` (Exploratory Data Analysis)

Una vez finalizado este proceso de ETL se genero un Dataframe denominado [**EDA**](Eda.ipynb) que contiene todos los datos necesarios para su analisis posterior.

El Analisis consiste en: 

- **Ingesta de datos**

- **Inspección preliminar**

- **Duplicados**

- **Valores faltantes** 

- **Outliers**

- **Gráficos (variables cuantitativas)** 

- **Gráficos (variables cualitativas)**

- **Observaciones**

- **Creación xlsx**


### **Distribución de Víctimas por Año**

<img src ="Imagen\Distribución de Víctimas por Año.png" >

**Observaciones:**

- La suma total de víctimas ha experimentado algunas variaciones a lo largo de los años es de 761.
- El año 2018 tiene la mayor suma total de víctimas (161), sugiriendo que fue un año con un mayor número de siniestros viales.
- El año 2020 tiene la menor suma total de víctimas (87), indicando que fue un año con un menor número de víctimas en comparación con otros años debido a la Pandemia producida por el COVID-19, lo que llevo al Aislamiento de loa ciudadanos.

### **Relación entre Número de Víctimas por Horas y Días de la Semana**

<img src ="Imagen\Relación entre Número de Víctimas por Horas y Días de la Semana.png" width="1000px" height="450px">

**Observacion:**
- Se observa una alta relacion entre los dias Domingos entre el rango horario de las (04:00 - 07:00), Sabados entre el rango horario de las (06:00 - 08:00), el dia Jueves se observa un pico entre (04:00 05:00) como el dia viernes a las horas(11:00 y 17:00) como se vio anteriormente que estos dias y a esas horas son los que se registras mayores Numeros de Incidentes. Se puede relacionar con la horaria de salida de zonas de entretenimiento y con el horario de inicio del dia de otros ciudadanos.

### **Correlación entre Poblacion, Densidad_Poblacion, N°_Victimas**

<img src ="Imagen\Correlación entre Poblacion, Densidad_Poblacion, N°_Victimas'.png">

**Observaciones:**
- La correlación entre la población y el número de víctimas es muy alta (0.971730). Esto sugiere una fuerte relación positiva: a medida que aumenta la población de una comuna, tiende a haber un aumento en el número de víctimas.
- Es probable que las comunas más grandes tengan más eventos y actividades, lo que podría aumentar las oportunidades de incidentes y, por lo tanto, el número de víctimas.
- La correlación entre la densidad de población y el número de víctimas también es significativa (0.623628), aunque menos fuerte que la correlación con la población.
- Esto sugiere que, además del tamaño de la población, la densidad de la población también puede tener un impacto en el número de víctimas. Comunas más densamente pobladas podrían enfrentar desafíos adicionales en términos de seguridad o recursos disponibles.


### **Top 5 comunas y numero de victimas**

<img src ="Imagen\Top 5 comunas y numero de victimas.png">


### **Distribución del Tipo de Calle en los Siniestros**

<img src ="Imagen\Distribución del Tipo de Calle en los Siniestros.png" width="950px" height="450px">

***Observaciones:**

Los siniestros viales ocurren con una gran frecuencia en Avenidas, superando a la suma de calle y autopistas juntas.
Se agreago Av Gral PAZ a autopista, como figura en la pagina oficial de la Ciudad de Buenos Aires.


### **Mapa con numero de Victimas CABA**

<img src ="Imagen\Mapa con numero de Victimas CABA.png" width="950px" height="450px">

***Observaciones:**

Se puede acceder al mapa a traves de [**Mapa**](mapa_incidentes_buenos_aires.html)


### **Distribución del Rol de las Víctimas**

<img src ="Imagen\Distribución del Rol de las Víctimas.png">

**Observacion:**

- El rol más común es el de conductor, seguido por peatón.
- La frecuencia de pasajeros o acompañantes es significativamente menor en comparación con conductores y peatones.
- La categoría de ciclistas tiene una frecuencia más baja en comparación con los demás roles.


`Dashboard`

Ingresar al [**Dashboard Interactivo**](Data\Siniestros_Viales.pbix) , creado en Power bi, para abordar los datos y hacer Analisis . De manera que se puedas consultar los datos en diversos Graficos. 

***<img src ="Imagen\Portada.PNG" width="950px" height="450px">***


***<img src ="Imagen\General.PNG" width="950px" height="450px">***


***<img src ="Imagen\KPI's.PNG" width="950px" height="450px">***


***<img src ="Imagen\Victmas.PNG" width="950px" height="450px">***


**<img src ="Imagen\Ubicacion.PNG" width="950px" height="450px">***


***<img src ="Imagen\Temporal.PNG" width="950px" height="450px">***


`KPIs`

Debes graficar y medir los 2 KPIs propuestos a continuación, representándolos adecuadamente en el dashboard. A su vez, tambíen tienes que proponer, medir y graficar un tercer KPI que consideres relevante para la temática. 
Los dos KPIs propuestos son:

- *Reducir en un 10% **tasa de homicidios en siniestros viales** de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior*.
  
  Definimos a la **tasa de homicidios en siniestros viales** como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico.
  Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000
  
- *Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior*.
  
  Definimos a la **cantidad de accidentes mortales de motociclistas en siniestros viales** como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal.
  Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

- *Reducir en un 10% la Cantidad siniestros viales que ocurren en Avenidas en el último año, en CABA, respecto al año anterior**.

    Definimos a la **Cantidad siniestros viales que ocurren en Avenidas** como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que ocurrieron en Avenidas en un determinado periodo temporal.
    Su fórmula para medir la evolución de los accidentes mortales que ocurrieron en Avenidas es: (Número de accidentes mortales que ocurrieron en Avenidas en el año anterior - Número de accidentes mortales que ocurrieron en Avenidas en el año actual) / (Número de accidentes mortales que ocurrieron en Avenidas en el año anterior) * 100
 
<img src ="Imagen\KPI'S_ corte.PNG">



## **Conclusiones**

Basándonos en las observaciones y datos analizados sobre los Siniestros Viales, se pueden derivar conclusiones significativas. Estas conclusiones ofrecen una comprensión completa de la situación y podrían desempeñar un papel crucial en la toma de decisiones y la creación de políticas destinadas a mejorar la seguridad vial en la Ciudad Autónoma de Buenos Aires(CABA).


`Numero de Victimas e Incidentes:`

- La Variable 'N°_Victimas' posee 717 observaciones , todas tienen valores no nulos, siendo el Total de Victimas igual a 761 de las cuales se tiene  registradas como Fallecidas a un Total de 688
- La gran mayoría de los incidentes (más del 94%) involucran a una única víctima, lo que indica que la mayoría de los siniestros viales registrados afectan a una sola persona


`Relacion Temporal:`

- La suma total de víctimas ha experimentado algunas variaciones a lo largo de los años es de 761.
- El año 2018 tiene la mayor suma total de víctimas (161), sugiriendo que fue un año con un mayor número de siniestros viales.
- Siendo diciembre el mes con la mayor cantidad de víctimas (87)
- Los días con mayor cantidad de víctimas son Domingo, Sábado y Viernes.
-  La distribución de víctimas por día de la semana muestra que los días con mayor cantidad de víctimas son Domingo, Sábado y Viernes.
- La media de víctimas por día es de aproximadamente 108.7.
- El día con la menor cantidad de víctimas es Miércoles (101 víctimas).
- La hora con la mayor cantidad de víctimas es 5:00 AM, seguida por 7:00 AM y 6:00 AM. Estas horas podrían ser consideradas como períodos críticos en los cuales ocurren más siniestros viales. La hora que menos Victimas posee es la 13 hora.

`Caracteristica de las victimas:`

- Edad Promedio de las Víctimas es de aproximadamente 42.17 años.
- La mayoría de las víctimas parecen concentrarse en rangos de edad más bajos, ya que los percentiles 25% y 50% son relativamente bajos. Sin embargo, el percentil 75% indica que hay algunas víctimas mayores de 56.25 años. No se observan valores 'Outliers'
- Se puede observar que la mayoría de las víctimas involucradas en los Siniestros Viales son del sexo masculino, superando al femenino en tres veces mas.
- El rol más Freacuente de Victima en incidentes es el de conductor, seguido por peatón.


`Relacion Victimas y Poblacion de Comunas:`
- La correlación entre la población y el número de víctimas es muy alta (0.971730). Esto sugiere una fuerte relación positiva: a medida que aumenta la población de una comuna, tiende a haber un aumento en el número de víctimas.
- La correlación entre la densidad de población y el número de víctimas también es significativa (0.623628), aunque menos fuerte que la correlación con la población.


`Participantes:`

- Combinaciones frecuentes: La combinación más frecuente es "PEATON-PASAJEROS" seguida de cerca por "MOTO-AUTO" y "MOTO-CARGAS". Estas combinaciones sugieren situaciones en las que peatones interactúan con pasajeros, motocicletas con automóviles, y motocicletas con vehículos de carga.

- La mayoria de victimas que sufren Siniestros Viales son las motos, seguido de peatones, lo que nos indica que en la movilidad sin carroceria es mas peligroso el transito por la ciudad.

`Ubicacion geografica:`

- Las 5 primeras comunas con mas incidentes son la 1, 4, 9, 8 y 7.
- Los siniestros viales ocurren con una gran frecuencia en Avenidas, superando a la suma de calle y autopistas juntas.
- Se agrego Av Gral PAZ a autopista, como figura en la pagina oficial de la Ciudad de Buenos Aires.


## **Medidas**

- La identificación de años y meses críticos (2018 y diciembre) proporciona oportunidades para implementar intervenciones específicas durante esos períodos, los cuales se involucran las festividades.

- La identificación del perfil de las víctimas (edad promedio, predominio masculino) permite dirigir estrategias de concientización y educación hacia grupos demográficos específicos.

- La predominancia de conductores de motocicletas como víctimas indica la necesidad de medidas de seguridad específicas para este grupo.

- La alta correlación entre población y número de víctimas destaca la importancia de considerar la densidad de población al asignar recursos para mejorar la seguridad vial.
La correlación con la densidad de población sugiere que la concentración de personas puede ser un factor que contribuye a los siniestros viales.

- La identificación de combinaciones frecuentes de participantes sugiere áreas clave para campañas de seguridad y regulación del tráfico.
El enfoque en las víctimas de motocicletas y peatones indica la necesidad de medidas específicas para mejorar la seguridad de estos participantes vulnerables.

- La concentración de incidentes en ciertas comunas señala la importancia de enfoques localizados para abordar problemas específicos de seguridad vial.

- La frecuencia de siniestros viales en avenidas destaca la necesidad de medidas específicas para mejorar la seguridad en estas áreas de alta circulación.


## **Contacto**

### Blas Fernando Pacios

[![LinkedIn](Imagen/linkedin.png)](https://www.linkedin.com/in/blas-fernando-pacios-14a46a280/) [![WhatsApp](Imagen/whatsapp.png)](https://wa.me/5493815467488)

## **Tecnologías utilizadas**

![Static Badge](https://img.shields.io/badge/PowerBI-gray?style=flat&logo=powerbi)
![Static Badge](https://img.shields.io/badge/Python-gray?style=flat&logo=python)
![Static Badge](https://img.shields.io/badge/-Pandas-gray?style=flat&logo=pandas)
![Static Badge](https://img.shields.io/badge/-Matplotlib-gray?style=flat&logo=matplotlib)
![Static Badge](https://img.shields.io/badge/-Seaborn-gray?style=flat&logo=seaborn)
![Static Badge](https://img.shields.io/badge/-Jupyter_Notebook-gray?style=flat&logo=jupyter)
![Static Badge](https://img.shields.io/badge/Visual_Studio_Code-gray?style=flat&logo=visual%20studio%20code&logoColor=white)

---