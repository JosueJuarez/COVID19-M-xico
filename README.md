# COVID19 en México
## Josué Júarez
------
Actualizado: 29 de octubre 2020

Fuente: https://datos.gob.mx/busca/dataset/informacion-referente-a-casos-covid-19-en-mexico

~~~
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 2365584 entries, 0 to 2365583
Data columns (total 38 columns):
 #   Column               Dtype 
---  ------               ----- 
 0   FECHA_ACTUALIZACION  object
 1   ID_REGISTRO          object
 2   ORIGEN               int64 
 3   SECTOR               int64 
 4   ENTIDAD_UM           int64 
 5   SEXO                 int64 
 6   ENTIDAD_NAC          int64 
 7   ENTIDAD_RES          int64 
 8   MUNICIPIO_RES        int64 
 9   TIPO_PACIENTE        int64 
 10  FECHA_INGRESO        object
 11  FECHA_SINTOMAS       object
 12  FECHA_DEF            object
 13  INTUBADO             int64 
 14  NEUMONIA             int64 
 15  EDAD                 int64 
 16  NACIONALIDAD         int64 
 17  EMBARAZO             int64 
 18  HABLA_LENGUA_INDIG   int64 
 19  INDIGENA             int64 
 20  DIABETES             int64 
 21  EPOC                 int64 
 22  ASMA                 int64 
 23  INMUSUPR             int64 
 24  HIPERTENSION         int64 
 25  OTRA_COM             int64 
 26  CARDIOVASCULAR       int64 
 27  OBESIDAD             int64 
 28  RENAL_CRONICA        int64 
 29  TABAQUISMO           int64 
 30  OTRO_CASO            int64 
 31  TOMA_MUESTRA         int64 
 32  RESULTADO_LAB        int64 
 33  CLASIFICACION_FINAL  int64 
 34  MIGRANTE             int64 
 35  PAIS_NACIONALIDAD    object
 36  PAIS_ORIGEN          object
 37  UCI                  int64 
dtypes: int64(31), object(7)
memory usage: 685.8+ MB
~~~

## Casos acumulados confirmados positivos

Los individuos considerados como positivos estan indicados por un valor de 1, 2, 3 en la columna de CLASIFICACION_FINAL. En total van 912811 confirmados.

![Casos positivos acumulados](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivosacum.png "Casos positivos acumulados")

### Por sexo
Los positvivos confirmados los podemos agrupar por sexo. Un individuo femenino es representado en los datos por un 1 y uno masculino por un 2 en la columna de SEXO.

![Casos positivos acumulados por sexo](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivoscum-hm.png "Casos positivos acumulados por sexo")

Se observa como la enfermedad no discrimina entre hombres ni mujeres.

### Por comorbilidades
La base de datos provee información sobre las comorbilidades que un individuo pueda tener. Un valor de 1 representa "Sí", y un valor de $2$ es un "No". Mientras que un valor de 98 representa "SE IGNORA". Para estos casos se considera como un valor faltante.

![Casos positivos acumulados por comorbilidades](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivivos_comorbilidades.png "Casos positivos acumulados por comorbilidades")

De las nueve comorbilidades de las que hay información, se observa que las más presentes entre los casos positivos son las de hipertensión, diabetes y obesidad.

### Por edad
Un histograma es de utilidad para ver la distribución de la edad en los individuos infectados.

![Casos positivos acumulados por edad](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivos_edad.png "Casos positivos acumulados por edad")

Por el perfil que se observa del histograma pareciera que la edad sigue una distribución normal centrada en la media de 44 años, con una desviación estándar de 16 años.

### Por municipio
En la dirección https://datos.covid-19.conacyt.mx/#DownZCSV, se tiene acceso a una base de datos que tiene registros de los casos diarios por municipio. Esta es de ayuda para poder visualizar como esta distribuida la epidemia geográficamente.

![Casos positivos por municipio](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/M%C3%A9xico.png "Casos positivos por municipio")

(Por alguna razón los conteos no coinciden con los de la otra base de datos.) Además de eso, también podemos visualizar tanto el desplazamiento geográfico y temporal:

![Desplazamiento geográfico y temporal](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/MapaNacional.gif "Desplazamiento geográfico y temporal")

Se observa como la epidemia comienza en municipios con alta densidad poblacional y se esparce a los municipios vecinos.

## Defunciones por casos acumulados confirmados positivos

Las defunciones las obtenemos filtrando a los individuos con resultado positivo a COVID-19 y con fecha de defunción válida. A la fecha van 90773 defunciones acumuladas.

![Defunciones por casos positivos](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defuncionescum.png "Defunciones por casos positivos")

### Por sexo

Filtrado de defunciones por sexo:

![Defunciones filtrado por sexo](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defuncionescum-hm.png "Defunciones filtrado por sexo")

Han fallecido al rededor de un 20% más de individuos masculinos debido a la enfermedad.

### Por comorbilidades principales

Filtrado por comorbilidades principales:

![Defunciones filtradas por comorbilidades principales](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defunciones_comorbilidades.png "Defunciones filtradas por comorbilidades principales")

Se hace más notable que las comorbilidades más presentes entre los individuos fallecidos debido a la enfermedad son las de hipertensión, diabetes y obesidad.

### Por edad

Filtrado por edad:

![Defunciones filtradas por edades](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defunciones_edad.png "Defunciones filtradas por edades")

Se sigue notando el perfil de la distribución normal, solamente que desplazada a una media de 62 años.


# COVID19 en Veracruz
Actualizado: 29 de octubre 2020

Se filtran los casos con el número de estado (30) en la columna de "ENTIDAD_UM"

## Casos acumulados confirmados positivos

En total van 36123 confirmados.
![Casos positivos acumulados en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivosacum_ver.png "Casos positivos acumulados en Veracruz")

### Por sexo

![Casos positivos acumulados por sexo en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivoscum-hm_ver.png "Casos positivos acumulados por sexo en Veracruz")

### Por comorbilidades

![Casos positivos acumulados por comorbilidades en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivivos_comorbilidades_ver.png "Casos positivos acumulados por comorbilidades en Veracruz")

### Por edad

![Casos positivos acumulados por edad en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/positivos_edad_ver.png "Casos positivos acumulados por edad en Veracruz")

El perfil de la distribución normal se nota menos. En el estado la media esta centrada en 47 años.

### Por municipio

![Casos positivos por municipios de Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/Veracruz.png "Casos positivos por municipios de 
Veracruz")

(Por alguna razón los conteos no coinciden con los de la otra base de datos.)

## Defunciones por casos acumulados confirmados positivos en Veracruz

A la fecha van 90773 defunciones acumuladas.

![Defunciones por casos positivos en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defuncionescum_ver.png "Defunciones por casos positivos en Veracruz")

### Por sexo

![Defunciones filtrado por sexo en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defuncionescum-hm.png "Defunciones filtrado por sexo en Veracruz")

De igual manera ha fallecido un 20% más de individuos masculinos debido a la enfermedad.

### Por comorbilidades principales

![Defunciones filtradas por comorbilidades principales en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defunciones_comorbilidades_ver.png "Defunciones filtradas por comorbilidades principales en Veracruz")

Siguen estando las tres mismas comorbilidades presentes en los individuos fallecidos.

### Por edad

![Defunciones filtradas por edades en Veracruz](https://github.com/JosueJuarez/COVID19-M-xico/blob/main/Figuras/defunciones_edad_ver.png "Defunciones filtradas por edades en Veracruz")

Se sigue notando el perfil de la distribución normal, solamente que desplazada a una media de 63 años.
